<template>
  <div class="searchWrapper">
<!--    <label for="search">Search</label>-->
    <input
      name="search"
      id="search"
      v-model="searchValue"
      @input="handleInput"
    />
    <!--      <ul>
            <li v-for="item in results" :key="item.data[0].nasaId">
              {{item.href}}
            </li>
          </ul>-->
  </div>
</template>

<script>
export default {
  name: 'SearchInput',
};
</script>

<style lang="scss" scoped>
.searchWrapper
{
  margin-top: 50px;
  display: flex;
  flex-direction: column;
  width: 250px;

  & label
  {
    font-family: Montserrat, sans-serif;
  }

  & input
  {
    height: 30px;
    border: none;
    background: none;
    border-bottom: 1px solid black;
    -webkit-appearance: initial;
  }

}
</style>
