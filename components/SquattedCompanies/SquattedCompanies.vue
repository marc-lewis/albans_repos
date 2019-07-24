<template>
  <section class="squattedCompanies">
    <div class="container">
      <h1 class="squattedCompanies__title">
        Companies I squat
      </h1>
      <ul class="squattedCompanies__companies">
        <li
          v-for="(imageAttributes, company) in companyImages"
          :key="company"
          class="squattedCompanies__company"
        >
          <img
            :src="imageAttributes.src"
            :alt="imageAttributes.alt"
            :data-company="company"
          >
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SquattedCompanies',
  data: () => {
    return {
      companyImages: {
        duckDuckGo: {
          src: '/images/company_logos/DuckDuckGo Logo- Vertical@3x.png',
          alt: 'Duck Duck Go'
        },
        nationalBankOfGreece: {
          src: '/images/company_logos/1200px-National_Bank_of_Greece.svg.png',
          alt: 'National Bank of Greece'
        },
        asics: {
          src: '/images/company_logos/asicsi_logo.png',
          alt: 'Asics'
        },
        zava: {
          src: '/images/company_logos/zava_logo.png',
          alt: 'Zava'
        },
        hashicorp: {
          src: '/images/company_logos/hashicorp_logo.png',
          alt: 'Hashicorp'
        }
      }
    }
  }
}
</script>

<style lang="scss">
.squattedCompanies {
  background: $light-grey;
  margin-top: $margin-large;
  padding: $padding-large $padding-small;
}
.container {
  margin: 0 auto;
  max-width: 700px;
}
.squattedCompanies__title {
  @include header;
  @include popFont;

  color: $git-black;
  font-size: 30px;
  text-align: center;
}
.squattedCompanies__companies {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  margin-top: $margin-small;
}
.squattedCompanies__company {
  align-items: center;
  display: flex;
  flex: 0 0 calc(50% - #{$margin-small});
  margin: $margin-small $margin-tiny;
  img {
    max-width: 100%;
  }

  &:nth-child(odd):last-child {
    margin: $margin-tiny auto;
  }
}

@media (min-width: 768px) {
  .squattedCompanies__company {
    flex: 0 0 calc(33% - #{$margin-small});
    &:nth-child(odd):last-child {
      margin: $margin-small $margin-tiny;
    }
  }
}
</style>
