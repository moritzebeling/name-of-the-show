<script>

	export let channel;

	function dateFormat( d ){
		d = new Date( Date.parse( d ) );
		return `${d.getFullYear()}-${d.getMonth()+1}-${d.getDate()} ${d.getHours()}:${d.getMinutes()}`;
	}

</script>

<footer>
	<div>
		<p>Updated {dateFormat(channel.updated_at)}</p>
		<p>{channel.contents.length} Contents</p>
		<p>{channel.follower_count} Followers</p>
	</div>
	<div>
		<a rel="noopener noreferrer" target="_blank" href="https://www.are.na/gif/{channel.slug}">Add content</a>
		<a rel="noopener noreferrer" target="_blank" href="https://github.com/moritzebeling/name-of-the-show">Contribute to website</a>
	</div>
</footer>

<style>

	footer {
		position: fixed;
		bottom: 0;
		left: 0;
		background-color: #000;
		color: #fff;
		width: 100%;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		padding: 0 0.5em;
	}
	p, a {
        display: inline-block;
        margin: 0.5em 0.25em;
	}

</style>
