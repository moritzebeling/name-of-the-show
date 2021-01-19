<script>

    export let item = {};

    function random( min, max ){
        return Math.floor(Math.random() * (max-min)) + min;
    }

    function top(){
        return Math.random() * window.innerHeight;
    }
    function left(){
        return Math.random() * window.innerWidth;
    }

</script>

<article style="top: {random(10,500)}vh; left: {random(10,70)}vw; width: {random(10,30)}vw; animation-duration:{random(10,30)}s; animation-delay:{random(1,5)}s;">

    <h3>{item.generated_title}</h3>

    {#if item.image}
        <img src={item.image.display.url} alt="" />
    {/if}
</article>

<style>

    article {
        position: absolute;
        width: 20vw;
        animation-name: fade;
        animation-duration: 4s;
        opacity: 0;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
    h3 {
        margin-bottom: 0.2em;
    }
    img {
        width: 100%;
        height: auto;
        box-shadow: 0px 0px 20px 0px rgba(0,0,0,0.3);
    }

</style>
