<template>
  <div id="app">
    <!-- Navbar start -->
    <nav class="navbar is-transparent has-shadow is-transparent">
     <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item logo-navbar" href="/">MyCompanyLogo</a>
      <div class="navbar-burger burger " v-on:click="toggleNav" v-bind:class="{'is-active' : isActive }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>  
  <div class="navbar-menu" v-bind:class="{'is-active' : isActive }">
    <div class="navbar-end">
        <router-link class="navbar-item" to='/'>Home</router-link>

        <router-link class="navbar-item" to='/'>Features</router-link>
      
        <router-link class="navbar-item" to='/'>About</router-link> 

        <router-link class="navbar-item" to='/faq'>FAQ</router-link>
    
      </div>
  </div>    
    <div class="navbar-end">
      <div class="navbar-item">
        <a href="" class="button is-primary is-outlined ">
          <span class="fa fa-download"> </span><span> </span>
          <span>  Join Now</span>
          </a>
      </div>
    </div>
  </div>
</nav>
    <!-- Navbar ended -->
    <router-view/>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>some text in the footer that we have it hahah some text in the footer that we have it hahah </p>
          </div>
          <div class="column has-text-right">
            <a href=""  class="icon"><i class="fa fa-facebook"></i></a>
            <a href="#" class="icon"><i class="fa fa-instagram"></i></a>
            <a href="#" class="icon"><i class="fa fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function(){
    return {
      isActive : false
    }
  },
  methods: {
      toggleNav: function(){
        this.isActive = !this.isActive
      }
  }
}
</script>
<style lang='sass'>
@import '../node_modules/bulma/bulma.sass'
@import 'mq'

.navbar
  background: #383838
  color: #fff
  .navbar-brand a
    font-weight: bold
    color: #fff
  a:hover
    color: gray
  .navbar-menu .navbar-end .navbar-item
    background: #383838
    color: #fff
    padding: 0.5rem 1.75rem
    &:hover
      color: gray
  .navbar-menu .navbar-end .navbar-item a.is-primary
    &:hover
      color: #fff

    +mobile
      .navbar
        background: #383838
      color: gray
      &:hover
        background-color: #f1f1f1
.footer
  background: $primary !important
  color: #fff
  .icon
    color: #fff
    margin-left: 20px
    font-size: 2.5rem
.logo-navbar
  font-size: 1.2rem
  font-weight: 100 !important
</style>
