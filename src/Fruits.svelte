<script>
    //Props
    export let fruits;
    export let reverse;

    let computedFruits;
    let name;
    let slice;

    if (reverse) {
        computedFruits = [...fruits].reverse();
        name = 'reverse';
    } else if (slice) {
        computedFruits = [...fruits].slice(...slice.split(','));
        name = `slice ${slice}`;
    } else {
        computedFruits = fruits;
    }
</script>

<h2>`Fruits ${name}`</h2>
<ul>
    {#each computedFruits as fruit}
        <li>{fruit}</li>
    {/each}
</ul>