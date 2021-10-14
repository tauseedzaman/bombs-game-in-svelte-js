<script>
async function fetch(){
    let me = await fetch("https://api.github.com/users/tauseedzaman/");
    console.log(me);
    return me.json()
}
</script>

<h1>Working</h1>
{#await fetch()}
    <p>Loading...</p>
{:then me}
<img src="{me.avator_url}" alt="">
    <p>{me}</p>
{/await}

<style>
    h1{
        color:blueviolet;
    }
</style>