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
        background-color: #1c1a3573;
        color: #C2C1C2;
        /* border: solid #03084e54 40px; */
        border-radius: 7px;
        /* padding: 50px; */
        padding-left: 6.5%;
        padding-left: 6.5%;
        padding-top: 13%;
        padding-bottom: 13%; 
        /* box-shadow: 30px 30px #1a0468b4; */
        z-index: 5;
    }

    .text2{
        color: #C2C1C2;
        background-color: #1c1a35c7;
        padding-top: 1%;
        padding-bottom: 1%;
        padding-left: 1.75%;
        padding-right: 1.75%;
        margin-left: 10%;
        margin-right: 17%;
        text-align: center;
    }
</style>