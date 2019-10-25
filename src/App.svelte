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
		let:data
		let:title
>
<h1>{title}</h1>
<ul>
	{#each data as link}
		<li>
			<a href={link.url}>{link.title}</a>
		</li>
	{/each}
</ul>
</Fetch>
