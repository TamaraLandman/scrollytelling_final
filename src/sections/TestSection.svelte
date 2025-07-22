<script>
import Scroller2 from "../lib/Scroller2.svelte";
import ArticleText2 from "../lib/ArticleText2.svelte";
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


    <Scroller2>

        {#snippet scrolly()}
        <ArticleText2>
        <p class="intro-text">The city of Cleveland is loacted within Cuyahoga County, Ohio.
        <br /> <br />
         The city and its surrounding
            areas have a large Black population.
        </p>
        </ArticleText2>

        <ArticleText2>
        <p class="intro-text">I spent most of my childhood in Cleveland, however, I was young and unaware about
         challenges that the Black community was facing.
         <br /><br />
          Therefore, I wanted to look back at some data reflecting the Black
            communtiy there to learn about some of the inequalities they may face, specically in the realm of education.
            <br />
        </p>
        </ArticleText2>

        <ArticleText2>
        <p class="intro-text">Although the demographic I chose to focus on is Cuyahoga County, OH, I hope these findings
            will shed light on the broader issue of  a lack of higher education and collge degrees for Black people.
        </p>
        </ArticleText2>
        {/snippet}


        {#snippet sticky()}
       <img class="cleveland-img" src="cleveland.jpg" alt="City of Cleveland" />
        {/snippet}



    </Scroller2>

</div>

<style>

    @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Inclusive+Sans:ital,wght@0,300..700;1,300..700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Inclusive+Sans:ital,wght@0,300..700;1,300..700&family=Lexend:wght@100..900&display=swap');
    .cleveland-img {
        width: 200%;
        height: 200%;
        margin: 0px auto;
        margin-left: -100%;
    }

    .intro-text{
        font-size: 25px;
        font-family: "Lexend", sans-serif;
        font-optical-sizing: auto;
        font-weight: 400;
        font-style: normal;
        
    }
</style>