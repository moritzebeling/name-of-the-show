<script>

	import Arena from './utilities/Arena.svelte';
	import Channel from './components/Channel.svelte';

	const channelId = 'website-gve0-btbpnq';
	// const channelId = 'photo_class_websites';

</script>

<Arena {channelId} let:prop={channel}>
	<Channel {channel} />
</Arena>

<style>

	:global( html ){
		font-size: 16px;
	}
	:global( body ){
		background-color: #000;
		color: #fff;
		font-family: 'Arial', sans-serif;
		letter-spacing: 0.03em;
		line-height: 1.2;
	}

</style>
