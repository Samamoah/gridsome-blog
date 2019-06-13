<template>
  <Layout>
    <div class="main-container">
      <div v-for="post in $page.posts.edges" :key="post.node.id" >
        <Card v-bind:post="post"/>
      </div>
    </div>
  </Layout>
</template>


<page-query>
query Posts{
  posts: allPost{ 
    edges {
      node {
        id
        title
        path
      }
    }
  }
}
</page-query>



<script>

import Card from '../components/Card'
export default {
  metaInfo: {
    title: 'Welcome'
  },
  components: {
    Card
  }
}
</script>

<style s>
    .main-container{
    margin: 2em 100px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 30px;
  }

  @media screen and (max-width: 700px) {
    .main-container{
      display: block
    }
  }
</style>
