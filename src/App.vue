<script>
  export default {

    data() {
      return {
        authenticated: false
      }
    }

  }
</script>

<template>
  <div>
      <div class="author">
        <h3>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nesciunt, praesentium.</h3><br><br>
        <div class="text">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolor dolorum harum laudantium neque nobis placeat quia quo, ratione suscipit voluptates? Ad eaque expedita id laudantium numquam obcaecati porro qui, quo.
          <br>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Amet at commodi earum error harum id illum laborum maiores obcaecati omnis praesentium, totam veniam voluptas? Eaque facilis hic incidunt obcaecati perferendis porro quos repudiandae sunt voluptate?
        </div>
      </div>
    <div v-if="authenticated">
      <br><br><br><br>
      <h4>Reply to post</h4>
      <input type="text" placeholder="reply">
    </div>
    <div v-else>
      <p>login to participate</p>
    </div>


  </div>
</template>

<style scoped>

</style>
