<script>
    // `layout` can be either "right" or "left"
    // `sticky` and `scrolly` are the snippets passed in (see one of the examples)
    let { scrolly, sticky } = $props(); 
</script>



    <!-- <div class="scrolly">
        {@render scrolly()}
    </div>
     <div class="sticky">
        {@render sticky()}
    </div>

<style>
      .wrapper {
        background-color: #f7f5eb;
        padding: min(100vh, 30rem) 1rem;
        border-style: solid;
        border-color: #4096fa;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: flex-start;
    }  

      .scrolly {
        order: 0;
    }
     .sticky {
        order: 1;
    }

     .scrolly {
        order: 1;
    }
     .sticky {
        order: 1;
    } 

     .sticky, 
    .scrolly {
        display: flex;
        flex-direction: column; 
        flex: 1 1; /* Allows growing, shrinking */
    }

    .sticky {
        position: sticky;
        top: 50vh;
        transform: translateY(-100%);
         display: flex; 
        align-items: center;
        justify-content: center;
        z-index: -3;
    }

    .scrolly {
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
    
</style> -->


<div class="wrapper">


     <div class="sticky">
        {@render sticky()}
    </div>

     <div class="scrolly">
        {@render scrolly()}
    </div>
</div>

<style>
    .wrapper {
        /* background-color: #E3E3DD ; */
        /* background-color: #616D7E; */
        /* background-color: #383f49; */
        background-color: #1c1a35;
        padding: min(100vh, 30rem) 1rem;
        border-style: solid;
        border-color: #3d344d;
        /* display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        align-items: flex-start; */
    }

    .scrolly {
        order: 1;
    } 
      .sticky {
        order: 0;
    }

    /* .right .scrolly {
        order: 1;
    }
    .right .sticky {
        order: 0;
    } */

     .sticky,
    .scrolly { 
        display: flex; 
        flex-direction: column;
        flex: 1 1; /* Allows growing, shrinking */
    }

     .sticky {
        position: sticky;
        top: 50vh;
        transform: translateY(-50%);
        margin-left: 50%;
        margin-right: 15%;
        /* transform: translateX(200%); */
        /* display: flex; */
        /* align-items: center; */
        display: flex;
        align-items: center;
        justify-content: center;
        z-index: 1;

    }
    

    .scrolly {
        justify-content: center;
        z-index: 3;
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
