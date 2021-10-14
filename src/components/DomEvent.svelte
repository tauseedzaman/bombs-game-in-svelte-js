<script>
function handleform(e){
    console.log(e)
}
</script>

    <h1>Testing Dom Events</h1>
<form action="/something/something" on:submit|preventDefault={handleform}>
    <input type="text" placeholder="Enter what you want" name="name">
    <!-- <input type="text" placeholder="Enter what you want" on:keydown={handleform}> -->
<!-- <button typ="submit" on:click={handleform}>Submit</button> -->
</form>

<label for="test">Mouse Over & fucse</label>
<input type="text" placeholder="Don't Move" on:mouseover={e=>e.target.focus()}>

<style>

</style>