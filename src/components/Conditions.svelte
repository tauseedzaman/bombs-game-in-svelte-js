<script>
 let comments=[
    {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     }, {
         'message':"wow this is greate jobe",
         'created_at':'1 min ago'
     },
 ];

 function addComment() {
     let comment = document.getElementById("newComment").value;
     let date=new Date()
     
     comments = [{
         'message':comment,
         'created_at':date.toDateString()
     },
    ...comments
];
document.getElementById("newComment").value="";
 }

function removeComment(index) {
    comments = comments.filter((r,i)=> i != index )
}
</script>
<input type="text" id="newComment" placeholder="Enter Your Comment">
<button on:click={addComment}>Add New</button>
<h1>Comments </h1>
{#if comments.length == 0}
    <p style="color:red">No Comment Found</p>
{/if}

{#each comments as comment,index}
<div style="background:lightgreen;padding:2px;">
    <p>{comment.message} <small><b><i>{comment.created_at}</i></b></small></p>
    <button on:click={()=> removeComment(index)} >X</button>
</div>
{/each}
<style>
</style>