<script>

	import {onMount} from 'svelte';
	import {getChannel} from './getChannel.js';

	export let channelId;
	let load;

	onMount(()=>{
		load = getChannel(channelId);
	});

</script>

{#if load}
	{#await load}
		<p>Loading</p>
	{:then channel}

		<slot prop={channel}></slot>

	{:catch error}
		<p>Error</p>
	{/await}
{/if}

<style>

    p {
        margin: 0.5rem 0.75rem;
    }

</style>
