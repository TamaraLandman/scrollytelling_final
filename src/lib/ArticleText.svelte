<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 50%;
        background-color: #03084ee0;
        color: #C2C1C2;
        /* border: solid #561B36 3px; */
        /* border-radius: 20px; */
        padding: 20px;
        /* box-shadow: 16px 16px #221749; */
    }
</style>
