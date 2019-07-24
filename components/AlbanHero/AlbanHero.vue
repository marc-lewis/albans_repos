<template>
  <section class="albanHero">
    <h1 class="albanHero__title">
      Alban's
      <br>Repos
    </h1>
    <img
      class="albanHero__logo"
      src="/images/octoalban.png"
      alt="octoalban"
    >
    <h2 class="albanHero__subtitle">
      I squat repos just incase!
    </h2>
    <p class="albanHero__pitch">
      Do you work for a big company? Did you want to create a repo and you’ve found that it’s already taken? Don’t be angry! Just buy it back from me!
    </p>
  </section>
</template>

<script>
export default {
  name: 'AlbanHero'
}
</script>

<style lang="scss">
  .albanHero {
    @include container;

    align-items: center;
    display: flex;
    flex-direction: column;
  }

  .albanHero__title {
    @include popFont;

    color: $git-black;
    font-size: 60px;
  }

  .albanHero__logo {
    margin-top: $margin-medium;
    position: relative;
    width: 50%;
  }

  .albanHero__subtitle {
    @include popFont;
    @include header;

    color: $pink;
    margin-top: $margin-small;
  }

  .albanHero__pitch {
    @include popFont;
    @include bodyCopy;

    color: $git-black;
    margin-top: $margin-small;
  }

  @media (min-width: 768px) {
    .albanHero {
      max-width: 600px;
    }
    .albanHero__title {
      font-size: 80px;
    }
  }
</style>
