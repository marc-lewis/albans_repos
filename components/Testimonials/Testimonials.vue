<template>
  <section class="testimonials">
    <div class="container">
      <p class="testimonials__title">But don't believe me!</p>
      <div
        v-for="(testimonial, name) in testimonials"
        :key="name"
        class="testimonial"
      >
        <div class="testimonial__avatar">
          <img
            :src="testimonial.img.src"
            :alt="testimonial.img.alt"
          />
        </div>
        <div class="testimonial__copy">
          <p class="testimonial__name">
            {{ name }}
          </p>
          <trustpilot-review-block
            class="testimonial__rating"
            :rating="testimonial.rating"
          />
          <p class="testimonial__review">
            {{ testimonial.review }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import TrustpilotReviewBlock from '../TrustpilotReviewBlock/TrustpilotReviewBlock'
export default {
  name: 'Testimonials',
  components: { TrustpilotReviewBlock },
  data: () => {
    return {
      testimonials: {
        'Boian Ivanov': {
          rating: 5,
          img: {
            src: '/images/testimonials/boian.jpeg',
            alt: 'Boian'
          },
          review: 'I was going to get him fired but then he offered me a cut of the profits!'
        },
        UZOR: {
          rating: 0,
          img: {
            src: '/images/testimonials/uzor.png',
            alt: 'UZOR'
          },
          review: 'You know I don\'t have to work with this guy anymore'
        },
        'Alban Kora': {
          rating: 5,
          img: {
            src: '/images/testimonials/alban.jpeg',
            alt: 'Alban Kora?'
          },
          review: 'I\'m so good that I rate myself!'
        },
        'Allan Mapletoft': {
          rating: 3,
          img: {
            src: '/images/testimonials/allan.jpeg',
            alt: 'Allan Mapletoft'
          },
          review: 'Is this still relevant? Hasn\'t this been resolved because we started leaving descriptions on repos?'
        },
        'Matlind Ruka': {
          rating: 5,
          img: {
            src: '/images/testimonials/matlind.png',
            alt: 'Matlind Ruka'
          },
          review: 'You know football is always better than basketball.'
        }
      }
    }
  }
}
</script>

<style lang="scss">
.testimonials {
  @include popFont;

  background: $light-grey;
}
.testimonials__title {
  @include header;

  color: $pink;
  text-align: center;
}
.container {
  padding: $padding-large $padding-small;
}
.testimonial {
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
}
.testimonial__avatar {
  clip-path: circle(40%);
  flex: 0 0 25%;

  img {
    max-width: 100%;
  }
}
.testimonial__copy {
  @include popFont;

  color: $git-black;
  display: flex;
  flex: 0 0 75%;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: center;
}

.testimonial__name {
  font-size: 30px;
  margin-top: $margin-tiny;
}
.testimonial__rating {
  margin-top: $margin-tiny;
}
.testimonial__review {
  font-size: 25px;
  margin-top: $margin-tiny;
}
</style>
