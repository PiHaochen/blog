<template>
  <div id="app">
    <!-- <add-blog></add-blog> -->
    <show-blogs></show-blogs>
  </div>
</template>

<script>
import Addblog from "./components/Addblog"
import Showblogs from "./components/Showblogs"
export default {
  name: 'App',
  components:{
    "add-blog":Addblog,
    "show-blogs":Showblogs
  }
}
</script>

<style>

</style>
