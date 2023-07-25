<script lang="ts">
    export let title: string;
    export let text: string;
    
</script>

<div class="h-44 max-w-xs bg-gray-600 rounded-lg border-2 border-gray-800 p-3">
    <span class="font-inherit text-white text-xl border-b-2 border-gray-600 w-full flex justify-center">{title}</span>
    <div class="w-full  text-l text-white ">
        {text}<slot name="image"></slot>
    </div>
</div>