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
        as seen in the example of Cleveland and its suburbs.
        <br><br>
        As shown by the CNN report above, this local data can be extrapolated to the broader Black population of the United States.
        </h3>
        </ArticleText3>

        <ArticleText3>
        <h3>Furthermore, because of a lack of college degrees, Black people in Cuyahoga County are more 
            likely to have a lower-paying job, which may lead to problems financially and in other
            areas as well.
        </h3>
        </ArticleText3>

        <ArticleText3>
        <h1>After seeing the data, it is clear that a change needs to be made. Take a minute to think...</h1>
        </ArticleText3>

        <ArticleText3>
        <h1>How Can We Create - Not Only A Seat at the Table... </h1>
        </ArticleText3>
        {/snippet}


        {#snippet sticky()}
       <img class="library-img" src="library.jpg" alt="Black and white LIbrary" />
        {/snippet}



    </Scroller2>

</div>

<style>
     .library-img {
        width: 200%;
        height: 200%;
        margin: 0px auto;
        margin-left: -100%;
    }
   
</style>