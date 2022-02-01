<script>
    import {storeName} from './store.js';
    import Parent from './Parent.svelte';

    let name = 'World!';
    $storeName = name;
</script>
<Parent/>