<template>
  <div class="exp-section">
    <h2>What I do</h2>
  </div>
</template>

<script>
export default {
  name: "Experience"
};
</script>

<style lang="scss" scoped>
.exp-section {
  margin-top: 20px;
  display: flex;
  flex-direction: column;

  h2 {
    font-size: 2em;
    padding: 20px;

    &:after {
      content: ".";
      color: #01d62f;
    }
  }
}
</style>
