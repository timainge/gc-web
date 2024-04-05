<template>
  <div class="pill-container">
    <slot></slot>
  </div>
</template>

<style lang="scss" scoped>
.pill-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  //padding: 1rem;
  background: color(display-p3 0.651 0.8863 0.9608);
  background-color: #94e4f8;
  height: 320px;
  border-radius: 160px;
  margin: 8rem 0;
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
</style>
