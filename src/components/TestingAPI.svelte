<script>
    let blog=''
    fetch('https://jsonplaceholder.typicode.com/posts/')
      .then(response => response.json())
      .then(posts => {
        //   console.log(posts)
          posts.forEach(post => {
          console.log(post)

              blog +=`
                <div class="post">
                    <h1>${post.title}</h1>
                    <p>${post.body}</p>
                </div>
              `
          });
      })
    // let src="https://media.istockphoto.com/photos/suitcase-packing-for-travel-covid19-picture-id1255431778?s=612x612"
    let posts = `
        <h1>Way to learn svelt js</h1>
        <p>Royalty-free licenses let you pay once to use copyrighted <b><i>images</i></b> and <b>video</b> clips</p>`
    
    </script>


<h1 class="posts_tage">Posts</h1>
<!-- <div class="post"> -->
    {@html blog}
    <!-- <h1>Hello world post title</h1> -->
    <!-- <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates, culpa iure blanditiis, eaque, animi qui consequuntur facilis dignissimos deleniti commodi corporis nostrum voluptatem voluptas corrupti inventore quas. Ea, possimus similique.</p> -->
<!-- </div> -->

<style>
    .posts_tage{
        color:blue;
        text-align: left;
        border-bottom: 2px solid purple;
    }
    .post{
        width: 100%;
        margin: auto;
        background-color: rgb(148, 192, 192);
        border:1px solid gray;
        border-radius:10px;
        box-shadow: 5px 5px 8px gray;
    }
    .post h1{
        text-align: left;
        padding-left: 10px;
        color: springgreen;

    }
    .post p{
        text-align: left;
        padding-left: 10px;

    }
    .post:hover{
        background-color: turquoise;
    }
</style>