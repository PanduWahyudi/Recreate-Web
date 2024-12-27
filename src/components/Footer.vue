<!-- eslint-disable vue/multi-word-component-names -->

<script>
import WebflowIcon from './icons/WebflowIcon.vue'
import WebflowBadgetIcon from './icons/WebflowBadget.vue'

export default {
  components: {
    WebflowIcon,
    WebflowBadgetIcon,
  },
}
</script>
<template>
  <footer class="custom-footer">
    <div class="footer-content">
      <div class="footer-right-box">
        <div class="web-icon">
          <WebflowIcon />
        </div>
        <div class="web-text">
          <WebflowBadgetIcon />
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.custom-footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: transparent;
  z-index: 1000;
  padding: 10px;
}

.footer-content {
  display: flex;
  justify-content: flex-end;
  width: 100%;
}

.footer-right-box {
  cursor: pointer;
  background-color: white;
  display: flex;
  border-radius: 4px;
  align-items: center;
  gap: 5px;
  padding: 5px;
  max-width: 700px;
}

.web-icon {
  width: 30px;
  height: 20px;
}

.web-text {
  width: 150px;
  height: auto;
}
</style>
