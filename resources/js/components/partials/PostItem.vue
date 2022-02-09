<template>
  <article>
    <h3>
      <a href="#">{{post.title}}</a>
    </h3>
    <p class="data">{{post.created_at}}</p>
    <p>{{truncateText}}</p>
  </article>
</template>

<script>
export default {

  name: 'PostItem',
  props:{
    'post': Object,
  },
  computed:{
    truncateText(){
      return this.post.description.substr(0, 50) + '...';
    }
  }

}
</script>

<style lang="scss" scoped>
  article{
    width: 44%;
    margin: 2%;
    padding: 15px;
    border-radius: 10px;
    background-color: black;
    border: 2px solid orangered;
    color: white;
    h3{
      margin: 5px 0px;
      a{
        text-decoration: none;
        color: white;
        &:hover{
          color: orangered;
        }
      }
    }
  }
</style>