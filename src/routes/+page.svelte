<script lang="ts">
  import Card from "$lib/card.svelte";
</script>
<main>
    <div class="pt-16">
        <div class="flex flex-col justify-center items-center">
            <div class="flex w-full justify-center m-5">
                <div class="flex flex-col w-7/12">
                    <h1 class="font-inherit text-6xl w-full">
                        <span class="text-white w-full flex justify-center">The one and only</span>
                        <span class="text-green-700 w-full flex justify-center">rock paper scissors game</span>
                    </h1>
                    <br class="w-2">
                    <p class="font-inherit w-full flex flex-col justify-center text-white text-l">
                            We are an open source rock paper scisor alterntive.
                            The age of playing rock paper in real life is over. 
                            Built only using open-source technology including Svelte, Tailwindcss 
                            and Node.js  
                    </p> 
                </div>
            </div>
            <div class="flex">
                <a href="/rock" class="bg-green-700 text-white m-3 flex items-center 
                cursor-pointer border-2 border-green-900 hover:bg-green-400 rounded p-2 text-xl">
                <img src="download (1).jpg" alt="waltuh" class="w-11 pr-1 rounded"> play the game</a>
                <a href="/docs" class="bg-gray-700 text-white m-3 flex items-center
                cursor-pointer border-2 border-gray-900 hover:bg-gray-500 rounded p-2 text-xl
                "> read the documentation</a>
            </div>
            <br class="w-8">
            <div>
                <small class="text-gray-300 font-inherit">Works seamlessly with 8+ browsers (i thought the images are transparent)</small>
                <div class="flex justify-center">
                    <img src="new-google-chrome-custom-google-chrome-incognito-logo-png-clipart.jpg" alt="chrome" class="w-11">
                    <img src="firefox-3-5-icon-mozilla-firefox-3-5-gray-png-clipart.jpg" alt="firefox" class="w-11">
                </div>
            </div>
            <section class="mt-16">
                <h3 class="text-white font-inherit text-2xl m-3 flex justify-center">Look at all the features:</h3>
                <div class="flex gap-2">
                    <Card title="speed" text="Build with the next gen post-beta Sveltekit which handles
                    Routing, state management and SSR. Blazingly fast and simple like you are using
                    Javascript by itself. Absolute awesome" />
                    <Card title="never lose my virginity" text="i never lose my virginity because i never lose (cant
                    fix this goddamn bug)" >
                    <img src="waltuh.jpg" alt="walter" class=" relative w-32" slot="image" /> </Card>
                    <Card title="fr*nch🤢" text="imagine not coding your entire website from scratch 
                    and having to use other applications to do it. You are a pussy until you spend 6 hours
                    of your life wondering how to center the text" />
                </div>
            </section>
            <section class="pt-72">  
                <p class="text-white text-2xl m-3"> subscribe to my youtube channel</p>
            </section>       
        </div>
    </div> 
</main>