<script>
import Scroller2 from "../lib/Scroller2.svelte";
import ArticleText from "../lib/ArticleText.svelte";
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
        <ArticleText>
        <h1>Testing this out!!!</h1>
        </ArticleText>
        {/snippet}


        {#snippet sticky()}
       <img class="duck-img" src="duck.png" alt="KWK rubber duck!" />
        {/snippet}



    </Scroller2>

</div>