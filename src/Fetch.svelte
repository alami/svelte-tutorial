<script>
    import { onMount } from "svelte";
    export let url = "https://academy.valentinog.com/api/link/";
    export let title = "A list of links";
    let data = [];
    onMount(async function() {
        const response = await fetch(url);
        const json = await response.json();
        data = json;
    });
</script>
<slot {data} {title} />