<template>
  <Layout> 
    <div class="content container" >
      <div v-html="$page.post.content"/>
    </div>

  </Layout>
</template>



<page-query>
query Post ($path: String!) {
  post: post (path: $path) { 
    title
    content
  }
}
</page-query>



<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
}
</script>

<style>
  .content{
    font-family: 'Roboto';
    margin: 2em;
  }
</style>
