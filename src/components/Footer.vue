<template>
  <div class="footer">
    <div class="left">
      <p>Made by the Collective in Canberra, Australia.</p>
    </div>
    <div class="right">
      <p>© The Good Collective Delivery Co. 2024</p>
    </div>
  </div>
</template>

<script></script>

<style lang="scss" scoped>
.footer {
  display: flex;
  width: 100%;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  text-transform: uppercase;
}

.left {
  text-align: left;
}

.right {
  text-align: right;
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
