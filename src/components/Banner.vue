<template>
  <div id="myHeader">
    <div id="menu">
      <Menu/>
    </div>
  </div>
</template>

<script>

import Menu from './Menu'

export default {
  name: 'Banner',
    components: {
    Menu,
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#myHeader {
  color: #000000;
  background-color: whitesmoke;
  height: 60px;
  width: 100%;
  position: relative;
  /*border-bottom: 5px solid grey;*/
  box-shadow: 0 5px 2px #888888;
}
</style>
