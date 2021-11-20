<template>
  <div id="menu">
    <nav class="navbar navbar-expand-lg navbar-light">
      <div class="container-fluid">
        <a class="navbar-brand title" href="first">Lord Of The Rings</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="about" v-bind:class="{ active: isActive('about') }">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="first" v-bind:class="{ active: isActive('first') }">The Project</a>
            </li>
                        <li class="nav-item">
              <a class="nav-link" href="second" v-bind:class="{ active: isActive('second') }">Datasets</a>
            </li>
                        <li class="nav-item">
              <a class="nav-link" href="third" v-bind:class="{ active: isActive('third') }">Analysis</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="third" v-bind:class="{ active: isActive('third') }">Want to learn more?</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="third" v-bind:class="{ active: isActive('third') }">Our team</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
// import router from "../router";
export default {
  name: "Menu",
  methods: {
    isActive: function(route) {
      if (this.$route.name == route){
        return true
      }
      else {
        return false
      }
    }
  }
};
</script>

<style scoped>
.title {
  color: black;

}

.title{
  margin-left: 80px;
}

#navbar {
  /*background-color: blue;*/
  /*border-style: solid;
  height: 50px;
  width: 100%;*/
}
</style>
