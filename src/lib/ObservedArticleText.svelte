<script>
    import { onMount } from "svelte";

    let { children, callback, options } = $props();

    // this uniqueId just lets us target the element 
    // with `document.getElementById(uniqueId)` later on.
    // it's a little hacky, but it works. 
    let uniqueId = Math.random().toString();

    // here we define the onMount() function for this component.
    // svelte handles calling the onMount() function *after* all of the HTML in this
    // component has been mounted to the DOM. we have to put the intersection observer
    // stuff in onMount() because we need to target the <div> we create below,
    // but it won't actually exist in the DOM until it's been mounted. 
    onMount(() => {
        let intersectionObserver = new IntersectionObserver(callback, options);

        const observedElement = document.getElementById(uniqueId);
        intersectionObserver.observe(observedElement);
    });
</script>

<!-- assign the containing div the id `uniqueId` so we can target it -->
<div id={uniqueId} class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 50vh auto;
        width: 57%;
        background-color: #03084ee0;
        color: #C2C1C2;
        border: solid #C2C1C2 3px;
        /* border: solid #561B36 3px; */
        /* border-radius: 20px; */
        padding: 30px;
        /* box-shadow: 16px 16px #221749; */
    }
</style>
