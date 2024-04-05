<template>
  <section :class="variant">
    <div class="jazz" v-if="variant != 'small'">
      <div class="placeholder-shape"></div>
    </div>
    <div class="heading">
      <slot name="heading"></slot>
    </div>
    <div class="text">
      <slot name="text"></slot>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CallToAction',
  props: {
    variant: {
      type: String,
      default: 'default',
      validator: (value) => {
        return ['large', 'default', 'small'].includes(value)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
section {
  // height: 320px;
  width: 100%;
  margin: 8rem 0;
  display: flex;
  justify-content: space-evenly;
  align-items: start;
  flex-direction: row;
  gap: 0rem;
  flex-wrap: wrap;
}

.jazz {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-grow: 0;
  flex-shrink: 0;
  flex-basis: 20%;
}

.heading {
  flex-grow: 0;
  flex-shrink: 0;
  flex-basis: 50%;
}

.text {
  flex-grow: 0;
  flex-shrink: 0;
  flex-basis: 30%;
}

.placeholder-shape {
  width: 200px;
  height: 200px;
  border-radius: 100px;

  background-color: #c0f0f0;
  border-radius: 100px;
}

@media (min-width: 1024px) {
  /* Styles for 1024px breakpoint */
}

@media (min-width: 1280px) {
  /* Styles for 1280px breakpoint */
}
</style>
