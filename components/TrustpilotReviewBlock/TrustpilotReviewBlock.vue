<template>
  <section class="trustpilotReviewBlock">
    <div
      v-for="index in 5"
      :key="index"
      class="trustpilotReviewBlockStar"
    >
      <svg
        version="1.1"
        id="Layer_1"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
        x="0px"
        y="0px"
        viewBox="0 0 96 96"
        style="enable-background:new 0 0 96 96;"
        xml:space="preserve">
        <rect :fill="getStarColour(index)" width="100%" height="100%"></rect>
        <g>
          <path fill="#FFFFFF" d="M48,64.7L62.6,61l6.1,18.8L48,64.7z M81.6,40.4H55.9L48,16.2l-7.9,24.2H14.4l20.8,15l-7.9,24.2l20.8-15l12.8-9.2L81.6,40.4L81.6,40.4L81.6,40.4L81.6,40.4z"></path>
        </g>
      </svg>
    </div>
    <img
      class="trustpilotReviewBlock__logo"
      src="/images/trustpilot/trustpilot_logo.svg"
      alt="Trustpilot Logo"
    >
  </section>
</template>

<script>
export default {
  name: 'TrustpilotReviewBlock',
  data() {
    return {
      colours: ['#e5e5e5', '#ff3722', '#ff8622', '#ffce00', '#73cf11', '#00b67a']
    }
  },
  props: {
    rating: {
      type: Number,
      required: true
    }
  },
  methods: {
    getStarColour(index) {
      const colour = this.colours[this.rating]
      return ((index - 1) < this.rating) ? colour : this.colours[0]
    }
  }
}
</script>

<style lang="scss">
  $starHeight: 20px;
  .trustpilotReviewBlock {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
  }
  .trustpilotReviewBlockStar {
    height: $starHeight;
    margin: 1px;
    width: $starHeight;
  }
  .trustpilotReviewBlock__logo {
    height: $starHeight;
    margin-left: 10px;
    width: auto;
  }
</style>
