<script>

    import Item from './Item.svelte';

    export let items = {};

</script>

<main>

    <ul>
        {#each items as item}
            <li>

                <Item {item} />

            </li>
        {/each}
        {#each items as item}
            <li>

                <Item {item} />

            </li>
        {/each}
    </ul>

</main>

<style>

    main {
        margin: 0.5rem;
    }

</style>
