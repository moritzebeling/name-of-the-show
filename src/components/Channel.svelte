<script>

	import List from './List.svelte';
	import Footer from './Footer.svelte';

	export let channel;
	console.log(channel);

</script>

<svelte:head>
	<title>{channel.title}</title>
</svelte:head>

<header>

	<h1>{channel.title}</h1>
	<h2>{channel.metadata.description}</h2>

</header>

<List items={channel.contents} />

<Footer {channel} />

<style>

	header {
		padding: 0.5rem 0.75rem;
	}

</style>
