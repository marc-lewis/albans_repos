<template>
  <footer class="albansFooter">
    <p>Alban's Repos</p>
    <p>ⓒ 2019</p>
    <a href="https://twitter.com/albankora">@albanKora</a>
  </footer>
</template>

<script>
export default {
  name: 'AlbansFooter'
}
</script>

<style lang="scss">
.albansFooter {
  @include popFont;

  align-items: center;
  background: $git-black;
  color: $white;
  display: flex;
  flex-direction: column;
  padding: $padding-large 0 $padding-extra-large;

  // I'm lazy, sue me!
  > * {
    color: $white;
    font-size: 20px;
    margin-top: $margin-tiny;
  }
}
</style>
