<template>
  <div class="pill-container" :class="type">
    <slot></slot>
  </div>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: 'blue'
    }
  }
}
</script>

<style lang="scss" scoped>
.pill-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  height: 320px;
  border-radius: 160px;
  margin: 12rem 0;
  overflow: hidden;
}
@media screen and (min-width: 768px) {
  .pill-container {
    height: 420px;
    border-radius: 210px;
  }
}
@media screen and (min-width: 1280px) {
  .pill-container {
    height: 540px;
    border-radius: 270px;
  }
}
.blue {
  background: color(display-p3 0.651 0.8863 0.9608);
  background-color: #94e4f8;
}
.pink {
  background: color(display-p3 0.9608 0.651 0.8863);
  background-color: #f8a6e2;
}
.black {
  background: color(display-p3 0.2 0.2 0.2);
  background-color: #333;
  color: white;
}
</style>
