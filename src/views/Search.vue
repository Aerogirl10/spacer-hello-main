<template>
  <div class="wrapper">
    <Claim/>
    <SearchInput/>
  </div>
</template>

<script>
import Vue from 'vue';
import axios from 'axios';
import debounce from 'lodash.debounce';
import VueAxios from 'vue-axios';
import Claim from '@/components/Claim.vue';
import SearchInput from '@/components/SearchInput.vue';

Vue.use(VueAxios, axios);

const API = 'https://images-api.nasa.gov/search';

export default {
  name: 'Search',
  components: { SearchInput, Claim },
  data() {
    return {
      searchValue: '',
      results: [],
    };
  },
  methods: {
    handleInput: debounce(function dupa() {
      axios.get(`${API}?q=${this.searchValue}&media_type=image`)
        .then((response) => {
          console.log(response.data.collection.items);
          this.results = response.data.collection.items;
        })
        .catch((error) => {
          console.log(error);
        });
    }, 500),
  },
};
</script>

<style lang="scss" scoped>
.wrapper
{
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  padding: 30px;
  width: 100%;
  background-image: url("../assets/bg.png");
  height: 100vh;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50% 0;
  justify-content: center;
}
</style>
