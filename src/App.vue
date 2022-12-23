<template>
  <div class="container m-x-auto">
    <RubricaList
      :data="fetchData"
    />
  </div>
</template>

<script>
import RubricaList from './components/RubricaList.vue'
import axios from 'axios'

export default {
  components: {
    RubricaList,
  },
  methods: {
    async fetchData() {
      try {
          const response = await axios.get('https://www.klerk.ru/yindex.php/v3/event/rubrics');
          this.data = response.data;
          console.log(this.data);
      } catch(e) {
          console.log(e);
      }
    },
  },
  mounted() {
      this.fetchData();
  },
}
</script>

<style>

</style>
