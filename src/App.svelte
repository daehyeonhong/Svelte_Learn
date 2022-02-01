<script>
    let name = 'world';
    let age = 85;
    function assign() {
        name = 'Svelte';
        age = 31;
    }
</script>

<h1>Hello {name}!</h1>
<h2 class={age < 85? 'active' : '' }>
    {age}
</h2>
<img src="" alt={name} />
<input type="text" bind:value={name} />
<button on:click={assign}>
    Assign
</button>

<style>
    h1 {
        color: red;
    }
    .active {
        color: blue;
    }
</style>