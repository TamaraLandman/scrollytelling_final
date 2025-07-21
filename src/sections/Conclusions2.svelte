<script>
import Scroller2 from "../lib/Scroller2.svelte";
import ArticleText3 from "../lib/ArticleText3.svelte";
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
        <ArticleText3>
        <h3>As seen from the data above, Black people are underrepresented when it comes to obtaining a college degree, 
        and in the test case of Cleveland, Ohio and its suburbs, are disproportionatly so
        </h3>
        </ArticleText3>

        <ArticleText3>
        <h3>Furthermore, because of a lack of college degrees, _____ of Black people in Cuyahoga County, OH are _____
            and ________ are _________
        </h3>
        </ArticleText3>

        <ArticleText3>
        <h1>After seeing the data, its clear that a change needs to be made. Take a minute to think...</h1>
        </ArticleText3>
        {/snippet}


        {#snippet sticky()}
       <img class="cleveland-img" src="cleveland.jpg" alt="City of Cleveland" />
        {/snippet}



    </Scroller2>

</div>

<style>
   
</style>