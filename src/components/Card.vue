<template>
      <div class="card" >
            <div class="card-title">
                <h1>{{post.node.title}}</h1>
            </div>
            <div class="card-body">
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Saepe at totam hic odio earum ad veniam enim animi eveniet praesentium quidem, velit libero esse itaque architecto dolorum quo amet perspiciatis!</p>
            </div>
            <div class="author">
                <h2>-John Doe</h2>
            </div>
            <g-link :to="post.node.path">
              More
            </g-link>
      </div>
</template>


<script>
export default {
  name: 'Card',
  props: {
      post : Object
  }
}
 
</script>

<style s>
    .card{
        background-color: white;
        padding: 1em;
        border-radius: 20px;
        box-shadow: 0 20px 30px rgba(0, 0, 0, 0.2);
    }

    .card-title{
        margin-bottom: 1em;
    }

    .card-body{
        margin-bottom: 1em;
    }

    @media screen and (max-width: 700px) {
    .card{
      margin-bottom: 30px;
    }
  }
</style>
