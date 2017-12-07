<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
            <div class="columns">
              <div class="column is-three-fifths">
              <h2 class="subtitle">{{subheading}}</h2>
              </div>
              </div>
              <a href="" class="button is-larg is-primary">Learn More</a>
        </div>
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <div class="column is-1">
              <i class="fa fa-cog primary" style="font-size:70px"></i>
          </div>
          <div class="column is-4">
            <p style="font-size:20px">
              <strong>We provide superior logistic so that your business can succeed in a crazy world !  </strong>
            </p>
          </div>
          <div class="column is-5 is-offset-1">
            <p style="font-size:20px">
              Lorem ipsumdolors itamet,cons eteturs adipsci ng elitr, sed dia nonumy eirmod tempor invid unt u t labo re et dolore magna aliquyam   
            </p>
          </div>
        </div>
      </div>
      <div class="container" style="margin-top:40px">
      <div class="columns">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="" style="font-weight:bold; font-size:20px">" I think it's an absolutely excellent tool for your business i cannot survive without this things "</p>
              <br>
              <p>- Seyed Alireza</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="" style="font-weight:bold; font-size:20px">" I think it's an absolutely excellent tool for your business i cannot survive without this things "</p>
              <br>
              <p>- Seyed Alireza</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="" style="font-weight:bold; font-size:20px">" I think it's an absolutely excellent tool for your business i cannot survive without this things "</p>
              <br>
              <p>- Seyed Alireza</p>
            </div>
          </div>
        </div>
      </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data(){
    return{
      heading: 'Soaring to new heights ',
      subheading: 'Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed dia nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam   '
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='sass' scoped>
@import '../mq'

.hero
  background: url('../assets/clouds.jpg')
  background-size: cover
.title
  +mobile
    font-weight: bold
  +tablet
    font-size: 2.5rem
  +desktop
    font-size: 4rem
    margin-top: 2rem
h2
  margin: 1.5rem 0 2rem 0 !important
.primary
  color: $primary
.card-content p
  padding: 10px
  color: gray
</style> 
