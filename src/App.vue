<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/chat">chat</router-link>
     
    </div>
    <div class="content">
        <router-view/>
    </div>
    <div class="footer">
    <footerr></footerr>
    </div>
  <!-- <div class="footer">
   
    <router-view/>

  </div> -->
   
  </div>
</template>
<script>
    import footerr from './views/footerr'
      export default {
        name:"app",
        methods:{
        },
        components:{
          'footerr':footerr,
        },
      }
</script>

<style lang="scss">
*{
  padding: 0;
  margin: 0 ;
}
#app {
  width: 100%;
  height: 80px;
  background-color: #be813b;
  text-align: center;
  color: #2c3e50;
}
.footer{
  height: 50px;
  background-color: #8b8b8b;
}
.content{
  background-color: #b9e2d0;
  height: 500px;
  // margin-top: -22px;
}

#nav {
  width: 50%;
  margin: 0 auto;
   display: flex;
    justify-content: space-between;
  padding: 30px;
  a {
    font-weight: bold;
    color: #080808;
    text-decoration: none;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
