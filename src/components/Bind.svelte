<script>
    let msg="hello world";
    let width=300;
    let image_url;
    let cars=[
        'http://127.0.0.1:8000/images/bg-1.jpeg',
        'http://127.0.0.1:8000/images/bg-2.jpeg',
        'http://127.0.0.1:8000/images/bg-3.jpeg'
    ];
    let locked=false;
</script>
<input type="text" bind:value={width}  disabled={locked}>
<br>
<input type="range" bind:value={width} min="0" max="1024" disabled={locked}>
<br>
<input type="radio" bind:group={image_url} value={cars[0]}  disabled={locked}>Car-1 <br>
<input type="radio" bind:group={image_url} value={cars[1]}  disabled={locked}>Car-2 <br>
<input type="radio" bind:group={image_url}  value={cars[2]}  disabled={locked}>Car-3 <br>
<div>
    <select name="" id="" bind:value={image_url}  disabled={locked}>
        <option value={cars[0]}>Car-1</option>
        <option value={cars[1]}>Car-2</option>
        <option value={cars[2]}>Car-3</option>
    </select>
</div>
<br>
<input type="checkbox" bind:checked={locked} > Lock This Car <br>
<img src={image_url} width={width} alt="">


<style>
    /* your styles go here */
</style>