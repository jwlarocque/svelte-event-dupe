<script>
    export let data = [];

    function swap() {
        let temp = data[0];
        data[0] = data[1];
        data[1] = temp;
        data = data;
        console.log("swapped")
    }
</script>

<main>
    <div class="list">
        <button on:click={swap}>Swap Items</button>
        {#each data as datum (datum)}
            <div on:click|stopPropagation={function(ev) {console.log("mousedown!");}}>
                <p>{datum}</p>
            </div>
        {/each}
    </div>
</main>