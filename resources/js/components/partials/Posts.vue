<template>
  <main>
    <div class="container">
    
      <h1>I miei post</h1>

      <div class="posts">
        <PostItem />
      </div>
      
    </div>
  </main>
</template>

<script>
import PostItem from './PostItem';
export default {
  name: 'Posts',
  components:{
    PostItem,
  },
  data(){
    return{
      apiUrl: 'http://127.0.0.1:8000/api/posts',
      posts: null,
    }
  },
  mounted(){
    this.getPosts();
  },
  methods:{
    getPosts(){
      axios.get(this.apiUrl)
      .then(res => {
        this.posts = res.data;
        console.log(this.posts);
      })
    }
  }
}
</script>

<style lang="scss" scoped>

</style>