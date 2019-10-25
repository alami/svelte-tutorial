<script>
    function handleSubmit(event) {
        // do stuff
    }
</script>
<form on:submit|preventDefault={handleSubmit}>
    <label for="search">Search:</label>
    <input type="search" id="search" required />
    <button type="submit">Search</button>
</form>