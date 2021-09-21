<script>
    export let book = {};
</script>

<style>
    #book {
        display: flex;
    }

    img {
        width: 10vw;
        margin-right: 2vw;
        margin-bottom: 5vh;
    }

    .borrowedWrap {
        display: flex;
        align-items: center;
    }

    input {
        margin-block-start: 1em;
        margin-block-end: 1em;
        margin-right: 1em;
        width: auto;
    }
</style>

<div id="book">
    <img src={book.img} alt="Cover of {book.title}" />
    <div id="info">
        <h3>{book.title}</h3>
        <p>Author: {book.author}</p>
        <p>Published in {book.year}</p>
        <div class="borrowedWrap">
            <input type="checkbox" />
            <p>Borrowed</p>
        </div>
    </div>
</div>