<script>
	import Library from './Library.svelte';
	import Form from './Form.svelte';
</script>

<style>
	div {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100vw;
	}
</style>

<div>
    <h1>Library of Classics</h1>
	<Form />
	<Library />
</div>