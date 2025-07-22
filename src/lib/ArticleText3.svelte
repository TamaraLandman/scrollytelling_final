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
        width: 50.5%;
        background-color: #171625;
        color: #C2C1C2;
        /* border: solid #03084e54 40px; */
        border-radius: 0px;
        /* padding: 50px; */
        padding-right: 2%;
        padding-left: 2%;
        padding-top: 7%;
        padding-bottom: 7%; 
        /* box-shadow: 30px 30px #1a0468b4; */
        z-index: 5;
        text-align: center;
    } 

    /* .text2{
        color: #C2C1C2;
        background-color: #1c1a35c7;
        padding-top: 1%;
        padding-bottom: 1%;
        padding-left: 1.75%;
        padding-right: 1.75%;
        margin-left: 10%;
        margin-right: 17%;
        text-align: center;
    } */
</style>