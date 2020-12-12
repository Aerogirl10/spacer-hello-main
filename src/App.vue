<template>
  <div class="app">
<!--    <div class="nav">
      <RouterLink to="/">spacer</RouterLink>
      <RouterLink to="/about">about</RouterLink>
    </div>-->
<RouterView></RouterView>
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;800&display=swap');
* {

  box-sizing: border-box;
}

body{
  font-family: 'Montserrat', sans-serif;
  margin: 0;
  padding: 0;
}
</style>
