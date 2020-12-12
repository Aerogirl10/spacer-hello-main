<template>
  <div class="claimWrapper">
    <h1 class="claim">SPACER</h1>
    <p class="subclaim">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      Alias cum, ea earum expedita inventore ipsa porro suscipit.
      Deleniti deserunt ducimus eveniet facilis, fuga fugit molestias mollitia,
      nemo pariatur quidem, veniam.
    </p>
    <p class="subclaim">
      Type anything space-related to start.
    </p>
  </div>
</template>
<script>
export default {
  name: 'Claim',
};
</script>
<style lang="scss" scoped>
.claimWrapper
{
  display: flex;
  text-align: center;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.claim
{
  font-size: 50px;
  margin: 0;
}

.subclaim{
  margin-top: 25px 0 0 0;
  font-size: 13px;
}
</style>
