<template>
  <section class="container">
    <div id="defaultForm">
    </div>
  </section>
</template>

<script>
import Vue from 'vue';
import InnerSearch from "../src/innerSearch.js";
import '../src/style.css';
import App from './App.vue'

Vue.use(InnerSearch);

window.addEventListener('load', function () {
  new Vue({
    el: '#defaultForm',

    created: function () {
      // ES server configuration
      this.setHost('http://es.yinyan.fr');
      this.setIndex('bank');
      this.setType('account');
    },

    render: h => h(App)
  });
});

export default {

}
</script>
