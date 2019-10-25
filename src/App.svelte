<script>
	export let name;
	import Fetch from "./Fetch.svelte";
	const props = {
		url: "https://jsonplaceholder.typicode.com/todos",
		title: "A list of todos"
	};
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}!</h1>
<Fetch
		{...props}
/>
