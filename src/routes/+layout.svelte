<script lang="ts">
    import '../app.css';
    import Navbtn from '$lib/navbtn.svelte'
</script>


<header class="fixed border-b-2 border-gray-700 flex w-full h-auto overflow-clip top-0 bg-gray-900">
    <nav class="flex justify-left">
        <a href="/" class=" my-3 ml-7 mr-3 flex items-center cursor-pointer font-inherit text-white text-xl">
            <img src="1200px-Rock-paper-scissors.svg.png" alt="rock" class="w-10 inline mr-1">
            <b>my website built from scratch</b>
        </a>
        <Navbtn link="/rock" text="game"/>
        <Navbtn link="/about" text="about"/>
    </nav>
    <div class="flex justify-end items-center w-7/12">
        <a href="https://github.com/zesk6/repo" class="cursor-pointer bg-green-700 border-green-950 hover:bg-green-500 text-white p-2 rounded">
            star us on github
        </a>
    </div>
</header>



<slot />