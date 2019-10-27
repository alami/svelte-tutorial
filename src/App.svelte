<script>
	import A446026 from "./A4446026.svelte";
	import Fetch from "./Fetch.svelte";
	import Form from "./Form.svelte";
	import A4446026 from "./A4446026.svelte";

	let searchTerm;

	function handleSubmit() {
		const {value} = this.elements.search;
		searchTerm = value;
	}
</script>
<A4446026 /><hr/><hr/>
<Form {handleSubmit} />
<Fetch {searchTerm} let:data>
	<h1>A list of links</h1>
	<ul>
		{#each data as link}
			<li>
				<a href={link.url}>{link.title}</a>
			</li>
		{/each}
	</ul>
</Fetch>
