<script>
export default {
  data() {
    return { 
      message: ''
    }
  },
}
</script>

<template>
    <div class="container flex py-5">
      <div>
        <img class="img" src="https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg" alt="Logo">
      </div>
        <h2>YU-GI-OH API</h2>
    </div>

</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *; 
.flex{
  display: flex;
  align-items: center;
}
.img{
  margin-right: 10px;
  height: 70px;
  width: 120px;
}
</style>