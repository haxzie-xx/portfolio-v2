<template>
  <div class="vertical">{{email}}</div>
</template>

<script>
export default {
  name: "VerticalBar",
  props: {
    email: String
  }
};
</script>

<style lang="scss" scoped>
.vertical {
  transform: rotate(90deg);
  transform-origin: left top 0;
  position: fixed;
  right: 20;
  bottom: 50;
}
</style>
