<template>
  <div class="lockup">
    <div>
      <h1>Good</h1>
    </div>
    <div class="logo-container">
      <img alt="Vue logo" class="logo" src="../assets/icons/icon-hand@2x.png" />
    </div>
    <div>
      <h1>Collective</h1>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.lockup {
  display: flex;
  width: 100%;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-size: 3rem;
  margin: 0;
}

.logo {
  height: 4rem;
}

@media screen and (min-width: 768px) {
  h1 {
    font-size: 4rem;
    margin: 0;
  }

  .logo {
    height: 5rem;
  }
}

@media screen and (min-width: 1280px) {
  h1 {
    font-size: 7rem;
    margin: 0;
  }

  .logo {
    height: 8rem;
  }
}
</style>
