<script lang="ts">
    export let link: string;
    export let text: string;

</script>
<a href={link} class="m-3 flex items-center hover:border-b-3
 hover:border-green-600 cursor-pointer ">
    <h2 class="font-inherit text-white inline text-l p-1
     hover:text-green-600 ">{text}</h2>
</a>