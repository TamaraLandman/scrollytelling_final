<script>
import Scroller from "../lib/Scroller.svelte";
import ArticleText from "../lib/ArticleText.svelte";
import { fade, fly } from "svelte/transition";
import ObservedArticleText from "../lib/ObservedArticleText.svelte";


let capIsVisible = $state(false);

const options = {
        threshold: [0.85, 0.95],
    };

const showCapCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                elem.style.backgroundColor = "#03084ee0";
                capIsVisible = true;
            } else if (entry.intersectionRatio < 0.9) {
                elem.style.backgroundColor = "##03084ee0";
            }
        });
    };
</script>

<div>
 <!-- <Scroller layout="left">
    {#snippet sticky()}
       <img class="duck-img" src="duck.png" alt="KWK rubber duck!" />
    {/snippet}

    {#snippet scrolly()}
        <ArticleText>
        <h1>Testing this out!!!</h1>
        </ArticleText>
    {/snippet}
 </Scroller> -->


    <Scroller layout="left">

        {#snippet scrolly()}
        <ObservedArticleText callback={showCapCallback} {options}>
        <p class="conclusion1-text">In an article by CNN, it was stated that 
        <strong>"Black college students have lower six-year completion rates for any type of degree or certificate program than any other racial or ethnic group."</strong></p>
        </ObservedArticleText>

        <ObservedArticleText callback={showCapCallback} {options}>
        <h1>"Only <strong>35%</strong> of Black Americans have associate degrees or higher" -CNN</h1>
        </ObservedArticleText>

        <ObservedArticleText callback={showCapCallback} {options}>
        <p class="conclusion1-text">Due to a lack of a college degree, Black people have to settle for lower-class jobs which means 
            a lower income and in some cases, more debt.</p>
            <br />
        <p class="conclusion1-text"><strong>Keep scrolling to see data about the outcomes potentially caused by the lack of a college degree</strong></p>
        </ObservedArticleText>
        {/snippet}


        {#snippet sticky()}
    
            {#if capIsVisible}
                    <div id="color-block">
                    <img
                        class="cap-img"
                        src="cap.png"
                        alt="Graduation Cap"
                        in:fly={{ y: 200, duration: 2000 }}
                        out:fade
                    />
                     </div>  
                {/if}
                    
    
        {/snippet}



    </Scroller>

</div>

<style>
     @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Inclusive+Sans:ital,wght@0,300..700;1,300..700&family=Lexend:wght@100..900&display=swap');
    /* #color-block {
        background-color: cadetblue;
        padding: 20px;
    } */

     /* .cap-img {
        width: 200%;
        height: 200%;
        margin: 0px auto;
        margin-left: -100%;
    } */

    .conclusion1-text{
        font-size: 20px;
        font-family: "Hind", sans-serif;
        font-weight: 400;
        font-style: normal;
    }

    #color-block{
        /* background-color: rgba(61, 26, 42, 0.363); */
        background-color: #c2c1c20c;
        padding-top: 150px;
        padding-bottom: 150px;
        padding-left: 25px;
        padding-right: 25px;
        z-index: -1;
        border-radius: 20px;
        border: solid #c2c1c22d;
    }

     

</style>