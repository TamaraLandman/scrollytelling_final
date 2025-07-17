<script>
    // `layout` can be either "right" or "left"
    // `sticky` and `scrolly` are the snippets passed in (see one of the examples)
    let { scrolly } = $props(); 
</script>

<div class="wrapper">

    <div class="scrolly">
        {@render scrolly()}
    </div>
</div>

<style>

    .wrapper {
        background-color: #f7f5eb ;
        padding: min(100vh, 30rem) 1rem;
        border-style: solid;
        border-color: #4096fa;
        /* display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: flex-start; */
    }
    .scrolly {
        justify-content: center;
        z-index: 2;
    }

    @media (max-width: 768px) {
        .wrapper {
            flex-direction: column;
            padding: 2rem 1rem;
            width: 100vw;
        }

        .sticky,
        .scrolly {
            flex: 1 1 auto;
            min-width: 100%;
            position: static; /* remove sticky on mobile */
            transform: none;
        }

        .sticky {
            margin-bottom: 2rem;
        }
    }
</style>
