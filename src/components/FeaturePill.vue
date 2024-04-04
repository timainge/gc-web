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
  padding: 1rem;
  background-color: #f0f0f0;
  height: 320px;
  border-radius: 160px;
  margin: 8rem 0;
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
