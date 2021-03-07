<template>
  <nav>
      <ul>
          <li v-for="location in location" :key="location.id"><router-link to="/">Home</router-link></li>
          <!-- <li><router-link to="/about">About</router-link></li>
          <li><router-link to="contact">Contact</router-link></li> -->
      </ul>
  </nav>
</template>
<script>
import store from "@/store.js"
export default {
    name: 'Navbar',
    data(){
        return{
            location: store.location
        };
    }
};
</script>

<style>
nav {
    width: 100%;
    height: 65px;
    padding: 0 100px;
    background-color: #fff;
}
nav ul {
    height: 65px;
    display: flex;
    align-items: center;
    list-style: none;
}
 nav ul li a{
     text-decoration: none;
     padding: 0 15px;
     color: #42b983;
 }

</style>