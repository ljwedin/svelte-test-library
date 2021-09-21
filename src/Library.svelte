<script>
    import Book from './Book.svelte';

    let books = [];

    fetch('http://localhost:3000/books')
    .then(res => res.json())
    .then(data => {
        books = data;
    })
</script>

<style>

</style>

<div>
    {#each books as book}
        <Book {book} />
    {/each}
</div>