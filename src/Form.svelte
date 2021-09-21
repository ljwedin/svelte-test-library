<script>
    const onSubmit = (e) => {
        e.preventDefault();
        
        let newBook = {
            "title": e.target.title.value,
            "author": e.target.author.value,
            "year": e.target.year.value,
            "img": e.target.imageUrl.value
        };

        fetch("http://localhost:3000/books", {
            method: "POST",
            headers: {
                "Content-type": "application/json",
            },
            body: JSON.stringify(newBook)
        })
        .then(res => res.json())
        .then(data => console.log("Data: ", data))
        .catch(err => console.log("Error: ", err))
    }
</script>

<style>
   form {
       display: block;
   }

   button {
       width: 400px;
       margin-top: 2vh;
       margin-bottom: 4vh;
   }
</style>

<h2>Add new book</h2>
<form on:submit={onSubmit}>
    <label for="title">Title</label>
    <input type="text" id="title" name="title" />
    <label for="author">Author</label>
    <input type="text" id="author" name="author" />
    <label for="year">Year published</label>
    <input type="number" id="year" name="year" />
    <label for="imageUrl">Image URL</label>
    <input type="text" id="imageUrl" name="imageUrl" />
    <br />
    <button type="submit">Add book</button>
</form>