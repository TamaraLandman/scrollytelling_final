<script>
    let { children } = $props();
</script>

<div class="article-text2">
    <p class="text2">
        {@render children()}
    </p>
</div>

<style>
    .article-text2 {
        margin: 50vh auto; 
        width: 63.5%;
        background-color: #03084e54;
        color: #C2C1C2;
        /* border: solid #03084e54 40px; */
        border-radius: 7px;
        padding: 50px;
        padding-top: 18%;
        padding-bottom: 18%; 
        /* box-shadow: 30px 30px #1a0468b4; */
        z-index: 5;
    }

    .text2{
        color: #C2C1C2;
        background-color: #03084ee0;
        padding-top: 18px;
        padding-bottom: 18px;
        padding-left: 10px;
        padding-right: 10px;
        margin-left: 10%;
        margin-right: 10%;
        text-align: center;
    }
</style>