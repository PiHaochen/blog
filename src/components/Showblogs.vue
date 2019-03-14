<template>
  <div id="show-blogs">
      <h1>博客总览</h1>
      <div v-for="blog in blogs">
          <h2>{{blog.title}}</h2>
          <article>{{blog.body}}</article>
      </div>
  </div>
</template>

<script>

export default {
  name: 'show-blogs',
  data(){
      return {
         blogs:[]
      }
  },
  created(){
      this.$http.get("http://jsonplaceholder.typicode.com/posts")
      .then(function(data){
          //console.log(data)
          this.blogs=data.body.slice(0,10);
          console.log(this.blogs);
      })
  }
}
</script>

<style>

</style>
