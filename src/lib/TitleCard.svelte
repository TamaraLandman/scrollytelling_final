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
        /* background-color: #4a4e69; */
         
    background: linear-gradient(-45deg, #820D42, #561B36, #221749, #03084E);
    background-size: 400% 400%;
    animation: gradient 8s ease infinite;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
    }

    @keyframes gradient {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}

    .content {
        /* max-width: 400px;
        height: 400px; */
        /* background-color: #C2C1C2;        
        padding: 8rem;
        border: 6px solid #561B36;
        border-radius: 400px; */
        /* box-shadow: 16px 16px #48a4e2; */
    }

    h1 {
        font-size: 4.5rem;
        margin: 0;
        color: #C2C1C2;
        /* text-shadow: 1px 1px 0 #221749; */
    }

    p {
        font-size: 2rem;
        color: #C2C1C2;
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
