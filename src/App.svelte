<script>
    import ItemComponent from "./ItemComponent.svelte";

    let data = ["Apples", "Butter"];
</script>

<main>
	<ItemComponent bind:data={data}/>
</main>

