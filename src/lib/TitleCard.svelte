<script>
    let { title, subtitle } = $props();
</script>

<div class="title-card">
    <div class="content">
        <h1>{title}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-color: #03084E;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
    }

    .content {
        max-width: 400px;
        height: 400px;
        background-color: #C2C1C2;        
        padding: 8rem;
        border: 6px solid #561B36;
        border-radius: 400px;
        /* box-shadow: 16px 16px #48a4e2; */
    }

    h1 {
        font-size: 2rem;
        margin: 0;
        color: #820D42;
        text-shadow: 1px 1px 0 #221749;
    }

    p {
        font-size: 1.3rem;
        color: #f7f5eb;
        margin-top: 1rem;
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.2rem;
        }

        p {
            font-size: 1.1rem;
        }
    }
</style>
