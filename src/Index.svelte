<script>

	import Arena from './utilities/Arena.svelte';
	import Channel from './components/Channel.svelte';

	// const channelId = 'website-gve0-btbpnq';
	const channelId = 'photo_class_websites';

</script>

<Arena {channelId} let:prop={channel}>
	<Channel {channel} />
</Arena>

<style>

</style>
