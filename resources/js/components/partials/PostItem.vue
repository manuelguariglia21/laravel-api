<template>
  <article>
    <h3>{{post.title}}</h3>
    <p class="data">{{post.created_at}}</p>
    <p>{{post.description}}</p>
  </article>
</template>

<script>
export default {

  name: 'PostItem',
  props:{
    'post': Object,
  }

}
</script>

<style lang="scss" scoped>
  article{
    width: 44%;
    margin: 2%;
    padding: 15px;
    border-radius: 10px;
    background-color: orangered;
    color: white;
  }
</style>