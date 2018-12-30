<template>
  <div class="nav-bar">
    <h1 class="title">{{ title }}</h1>
    <ul class="nav-menu">
      <li>
        <a href="#">home</a>
      </li>
      <li>
        <a href="#">portfolio</a>
      </li>
      <li>
        <a href="#">projects</a>
      </li>
      <li>
        <a href="#">resume</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  props: {
    title: String
  }
};
</script>

<style lang="scss" scoped>
.nav-bar {
  display: flex;
  align-items: center;
  background-color: white;
  width: 100%;
  padding: 20px;
}
.title {
  font-size: 1.5em;

  &:after {
    content: ".";
    font-size: 1.5em;
    color: #01d62f;
  }
}

.nav-menu {
  list-style: none;
  display: flex;
  flex-direction: row;
  margin-left: auto;
  margin-right: 20px;

  li a {
    color: #2c3e50;
    text-decoration: none;
    font-size: 1.2em;
    padding: 10px 15px 10px 15px;
    transition: 0.5s all ease-in-out;
    &:hover {
      color: #01ac26;
    }
  }
}
</style>
