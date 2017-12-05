<template>
  <div id="app">
    <!-- Navbar start -->
    <nav class="navbar is-transparent has-shadow is-transparent">
     <div class="container">
      <div class="navbar-brand">
        <a class="navbar-item" href="/">MyCompany</a>
      <div class="navbar-burger burger " v-on:click="toggleNav" v-bind:class="{'is-active' : isActive }">
        <span></span>
        <span></span>
        <span></span>
      </div>
    </div>  
  <div class="navbar-menu" v-bind="{'is-active' : isActive }">
    <div class="navbar-end">
        <router-link class="navbar-item" to='/'>Home</router-link>
        <a href="" class="navbar-item">someshit</a>
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
    color: #fff
    padding: 0.5rem 1.75rem
    &:hover
      color: gray
  .navbar-menu .navbar-end .navbar-item a.is-primary
    &:hover
      color: #fff

    +mobile
      color: gray
      &:hover
        background-color: #f1f1f1


</style>
