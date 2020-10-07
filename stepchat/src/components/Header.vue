<template>
<header>
  <div class="logo"></div>
  <div class="search-bar"></div>
  <div class="Users">
      <span>{{Name}}</span>
  </div>
</header>
</template>

<script>
export default {

}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
header {
  display: flex;
  flex-direction: row;
  width: 100%;
  height: 60px;
  background-color: #0398e7;
  justify-content: space-between;
  align-items: center;
}
header .logo{
  background-color: #a0c5e8;
  width: 50px;
  height: 50px;
  border: 1px solid transparent;
  border-radius: 25px;
}
header .Users {
  float: right;
  margin-right: 75px;
 }
 header .Users {
  width: 40px;
  height: 40px;
  border: 1px solid transparent;
  border-radius: 25px;
  background-color: #a0c5e8;
 }
</style>
