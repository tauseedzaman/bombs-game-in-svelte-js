<script>
let total=0;
$: shipping=total*0.001;
$: grandtotal=total+shipping;

$: if(total >500){
    shipping=0;
}
function addtocard(){
    total =total+50;
}


</script>

<div class="blog">
    <div class="card">
        <img src="https://images.everydayhealth.com/images/diet-nutrition/34da4c4e-82c3-47d7-953d-121945eada1e00-giveitup-unhealthyfood.jpg?w=1110" width="100%" alt="">
        <h2 style="text-align:left;padding:5px">Title</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum at, nostrum asperiores </p>
        <button on:click={addtocard}>Add to card</button>
    </div>
    
    <div class="card">
        <img src="https://images.everydayhealth.com/images/diet-nutrition/34da4c4e-82c3-47d7-953d-121945eada1e00-giveitup-unhealthyfood.jpg?w=1110" width="100%" alt="">
        <h2 style="text-align:left;padding:5px">Title</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum at, nostrum asperiores </p>
        <button on:click={addtocard}>Add to card</button>
    </div>
    
    <div class="card">
        <img src="https://images.everydayhealth.com/images/diet-nutrition/34da4c4e-82c3-47d7-953d-121945eada1e00-giveitup-unhealthyfood.jpg?w=1110" width="100%" alt="">
        <h2 style="text-align:left;padding:5px">Title</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum at, nostrum asperiores </p>
        <button on:click={addtocard}>Add to card</button>
    </div>
    
    <div class="card">
        <img src="https://images.everydayhealth.com/images/diet-nutrition/cbbec0bf-949c-4ae0-b202-165a8f5a689801-giveitup-chips.jpg?w=1110" width="100%" alt="">
        <h2 style="text-align:left;padding:5px">Title</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum at, nostrum asperiores </p>
        <button on:click={addtocard}>Add to card</button>
    </div>
</div>

<h1>Total Price: {total}</h1>
<h1>Shepping: {shipping}</h1>
<h1>Grant Total Price: {grandtotal}</h1>

<style>
    .blog{
        display:inline-block;
    }
    .card{
        margin-top: 10px;
        display: block;
        width: 180px;
        background-color: cadetblue;
        border:1px solid greenyellow;
        box-shadow: 5px 5px 8px yellow;
        border-radius: 6px;
    }
    .card button{
        background-color: lightgreen;
        color: black;
        border:1px solid lightgreen;
        border-radius: 5px;
    }
    .card button:hover{
        background-color: green;
        color: white;

        box-shadow: 2px 3px 5px lightgrey;
    }

</style>