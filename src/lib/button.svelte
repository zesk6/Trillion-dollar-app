<script lang='ts'>
    export let name: string;
    export let middle: Function;
    function handleClick(){
        middle(name)
    }
</script>

<button on:click|preventDefault={handleClick} 
class="rounded border-2 border-green-400 bg-green-700 hover:bg-green-500 text-white p-2">
    {name}
</button>