<template>
    <center><div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/archive">Archive</router-link>
        <router-link to="/about">About</router-link>
    </div></center>
    <router-view/>
</template>

<script>
import { useStore } from 'vuex'
export default {
	beforeCreate() {
        const store = useStore()
		store.commit('loadStore');
	}
}
</script>

<style>
@font-face {
  font-family: 'Fonts';
  src: url('assets/font/Poppins-Regular.woff2') format('woff2'),
       url('assets/font/Poppins-Regular.woff') format('woff');
  /* Replace `fontname` with the actual name of the font files */
  font-weight: normal;
  font-style: normal;
}

#app {
    font-family: 'Fonts', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: 2rem;
}
#nav a {
    font-weight: bold;
    color: #000;
    margin: 0 1rem 0 0;
    background: #eee;
    border-radius: 14px;
    text-decoration: none;
    padding: 0.25rem 0.75rem;
}
#nav a.router-link-exact-active {
    color: #0275d8;
    background: #ddd;
}
</style>