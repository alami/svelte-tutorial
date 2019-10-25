<script>
	export let name;
	import Fetch from "./Fetch.svelte";
	const props = {
		url: "https://jsonplaceholder.typicode.com/todos",
		title: "A list of todos"
	};
	import Form from "./Form.svelte";

</script>
<h1>Real svelte {name}!</h1>
<Form />

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
