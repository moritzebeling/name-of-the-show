<script>

	import Footer from './Footer.svelte';

	export let channel;
	console.log(channel);

</script>

<svelte:head>
	<title>{channel.title}</title>
</svelte:head>

<Footer {channel} />

<style>
</style>
