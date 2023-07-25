<script lang="ts">
    import Button from '$lib/button.svelte';
    import { onMount } from 'svelte';

 
    let myChoice = "loading...";
    let yourChoice: any = "";
    let gameRunning = false;
    let winner = "";


    onMount(() => {
        setTimeout(() => {  // run the code 1 second after loading the page
            initializeGame();
        }, 1000)
    })
    function initializeGame(){
        gameRunning = true;
        myChoice = "";
        yourChoice = "";
        winner = "";
    }
    function middle(name: string){
        if (!gameRunning) return;
        yourChoice = name;
        meClick();
    }
    function meClick(){
        const number = Math.floor(Math.random() * 3)  // returns a random number from 0 to 2
        switch (number){
            case 0:
                myChoice = "rock";
                break;
            case 1:
                myChoice = "paper";
                break;
            case 2:
                myChoice = "scissors";
                break;
            default:
                throw new Error("my nigga you screwed up");
        }
        evaluate();
    }
    function evaluate(){
        if (myChoice === yourChoice) postGame(true, false); // the argument states that it is a draw
        else if (doIWin()) postGame(false, false);
        else postGame(false, true);
    }
    function doIWin(){
        switch (myChoice) {
            case 'paper':
                return (yourChoice === 'rock') ? true : false;
            case 'rock':
                return (yourChoice === "scissors") ? true : false;
            case 'scissors':
                return (yourChoice === 'paper') ? true : false;
            default:
                throw new Error('my nigga you screwed up again')
        }
    }
    function postGame(draw: boolean, youWin: boolean){
        gameRunning = false;
        if (draw) winner = ' draw';
        else if (youWin) winner = ' u';
        else winner = " me";
    }
    function restartGame(){
        if (gameRunning) return;
        initializeGame();
    }
    
</script>
<main>
    <section class="flex flex-col justify-center items-center">
        <h1 class="text-6xl text-white pt-24">rock paper scisoor</h1>
        <div class=" w-1/2 bg-gray-300 mt-7 rounded-lg h-auto">
            <span class="flex justify-center text-red-700 font-inherit">me: {myChoice}</span>
            <span class="flex justify-center text-green-700 font-inherit">you: {yourChoice}</span>
           
            <span class="flex justify-center text-xl font-inherit"> 
            who won is:{(winner === 'draw') ? "its a fuckin draw" : winner}</span>
            
            <div class="flex justify-between mb-3 mx-10 mt-20">
                <Button name="rock" {middle}/>
                <Button name="scissors" {middle}/>
                <Button name="paper" {middle} />
                <button class="rounded border-2 border-gray-400 bg-gray-700
                 hover:bg-gray-500 text-white p-2" on:click={restartGame}>restart????</button>
            </div>
        </div>
    </section>
</main>

