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
        <h1>The city of Cleveland has a population of approximately 362,656 residents</h1>
        </ArticleText2>

        <ArticleText2>
        <h1>Testing this out!!!</h1>
        </ArticleText2>

        <ArticleText2>
        <h1>Testing this out!!!</h1>
        </ArticleText2>
        {/snippet}


        {#snippet sticky()}
       <img class="cleveland-img" src="cleveland.jpg" alt="City of Cleveland" />
        {/snippet}



    </Scroller2>

</div>

<style>
    .cleveland-img {
        width: 200%;
        height: 200%;
        margin: 0px auto;
        margin-left: -100%;
    }
</style>