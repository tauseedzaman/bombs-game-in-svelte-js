<script>
    import {beforeUpdate, afterUpdate, onMount} from 'svelte';
    let attempts =0;
    let interval;
    let bombs = new Array(50);
    let randnum=0;
    let loose = false;
    let win = false;

    afterUpdate(()=>{
        if (attempts == 10) {
            clearInterval(interval);
            alert("You Loose 😞!");
            attempts=0;
            loose=true;
        }
        if (bombs.length == 0) {
            clearInterval(interval);
            alert("You Are The Winner! 😇");
            win=true;
        }
    })


    onMount(()=>{
        interval = setInterval(() => {
            randnum=Math.floor(Math.random()*bombs.length);
        }, 1000);

    })

    function handleClick(i){
        console.log(i,randnum);
        if (i == randnum) {
            bombs = [...bombs.slice(0,i), ...bombs.slice(i+1)]
        }else{
            attempts = attempts+1;
        }
    }
</script>
<h1>Bombs Game</h1>
<h5>Attempts: {attempts}</h5>
<div class="game">
    {#each bombs as _,i}
    <div class="bomb" style={i == randnum ? '': 'opacity:0.3'} on:click={()=>{handleClick(i)}}>💣</div >
{/each}
</div>
{#if loose==true}
    <center>
        <a href="/" >Try Again😎</a>
    </center>
{/if}
{#if win==true}
    <center>
        <h1>WOW! Contrage! 🎃</h1>
    </center>
{/if}
<style>
    .game{
        margin: 0 auto;
        width: 30%;
        display:flex !important;
        flex-wrap: wrap;
        justify-content: center;
    }
    .bomb{
        cursor: pointer;
    }
</style>