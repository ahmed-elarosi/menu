<template>
  <div class="container">
    <div class="card" v-for="item in list" v-bind:key="item.id">
      <li>{{ item.productName }}</li>
      <li>{{ item.image }}</li>
      <li>{{ `Category: ${item.category}` }}</li>
      <li>{{ `Country: ${item.from}` }}</li>
      <li>{{ `Price: ${item.price} €` }}</li>
      <li>{{ `Description: ${item.description}` }}</li>
    </div>
  </div>
</template>
<script>
import Vue from 'vue';
import axios from 'axios';
import VueAxios from 'vue-axios';
import '../styles/menu.css';

Vue.use(VueAxios, axios);

export default {
  name: 'Menu',
  data() {
    return {
      list: undefined,
      card: {},
    };
  },
  async mounted() {
    Vue.axios.get('http://127.0.0.1:9001/dishes').then((res) => {
      this.list = res.data.data;
      console.warn(res.data.data);
    });
  },
  methods: {
    async addItem() {

    },
  }
};
</script>
