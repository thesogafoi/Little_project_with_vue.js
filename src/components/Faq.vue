<template>
  <div class="faq">
    <div class="container">
      <section class="section">
        <h1 class="title">FAQ</h1>
        <h2 class="subtitle is-4">Lorem ipsum and all of that jaaz.</h2>
        <div class="columns" v-if="faqs && faqs.length">
          <div class="column" v-for="faq in faqs">
            <div class="card">
              <div class="card-content">
                <p style="font-size:20px;font-weight:bold">{{faq.title}}</p>
                <p class="answer">{{faq.body}}</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Faq',
  data: () => ({
    faqs: [],
    errors: []
  }),
  created(){
    axios.get('https://jsonplaceholder.typicode.com/posts')
    .then(response => {
      this.faqs = response.data.slice(0,10);
    })
    .catch(e=>{
      this.errors.push(e)
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='sass' scoped>
@import '../mq'
.columns
  padding: 2.5em 0 1.5em 0
.answer
  margin-top: 10px !important
  color: gray
.columns
  flex-wrap: wrap
</style>
