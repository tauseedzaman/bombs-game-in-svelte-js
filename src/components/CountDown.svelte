<script>
    import {onDestroy} from 'svelte';
    let count=0;
    let myinterval = setInterval(() => {
        count = count+1;   
        console.log(count);
}, 1000);

function removeInterval(){
    
    onDestroy(()=>{
        clearInterval(myinterval);
    });

}
removeInterval()
</script>
<h1>{count}</h1>
<style>
    
</style>