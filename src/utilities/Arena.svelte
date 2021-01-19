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
		Loading
	{:then channel}

		<slot prop={channel}></slot>

	{:catch error}
		Error
	{/await}
{/if}
