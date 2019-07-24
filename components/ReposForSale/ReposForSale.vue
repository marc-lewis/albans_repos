<template>
  <section class="reposForSale">
    <p class="reposForSale__title">
      What's for sale at good prices?
    </p>
    <ul class="repoList">
      <li
        v-for="repo in repos"
        :key="repo"
        class="repoList_repo"
      >
        {{ repo }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  name: 'ReposForSale',
  data() {
    return {
      repos: [
        'Zebra',
        'Alban Is The best',
        'Centaur',
        'Chimera',
        'Jigglypuff',
        'Kraken',
        'Medusa',
        'Mermaid',
        'Merman',
        'Baba Yaga',
        'Pegasus',
        'Yeti',
        'Warewolf',
        'Bigfoot',
        'Moon Rabbit',
        'Basilisk',
        'Chicken',
        'Grim Reaper',
        'Bogeyman',
        'Cyclops',
        'Goblin',
        'Griffin',
        'Gorgon',
        'Leprechaun',
        'Loch Ness Monster',
        'Ogre',
        'Pixie',
        'Goat'
      ].sort()
    }
  }
}
</script>

<style lang="scss">
  .reposForSale {
    @include container;
    @include popFont;

    margin: $margin-large $margin-small;
  }

  .reposForSale__title {
    @include header;

    color: $pink;
    text-align: center;
  }

  .repoList {
    column-count: 2;
    column-gap: $margin-tiny;
    margin-top: $margin-medium;
  }

  .repoList_repo {
    @include bodyCopy;

    color: $git-black;
  }

  @media (min-width: 768px) {
    .repoList {
      column-count: 3;
    }
  }
</style>
