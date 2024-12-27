<!-- eslint-disable vue/multi-word-component-names -->

<template>
  <header class="custom-header">
    <div class="header-content">
      <div class="header-right-box">
        donate
      </div>
    </div>
  </header>
</template>


<style lang="scss" scoped>
.custom-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: transparent;
  z-index: 1000;
  padding: 10px;
}

.header-content {
  display: flex;
  justify-content: flex-end;
  width: 100%;
}

.header-right-box {
  cursor:pointer;
  @include text-3xl;
  background-color: white;
  border: 4px solid black;
  padding: 10px;
  max-width: 300px;
}
</style>
