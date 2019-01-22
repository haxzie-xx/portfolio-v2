<template>
  <div class="project-card">
    <a :href="details.link">
      <h2>{{details.name}}</h2>
    </a>
    <p>{{details.description}}</p>
    <ul>
        <li v-for="(tag, index) in details.tags" :key="index"> {{tag}}</li>
    </ul>
    <p class="bg-text">{{details.name[0]}}</p>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: {
    details: Object
  }
};
</script>

<style lang="scss" scoped>

.project-card {
  width: auto;
  height: 200px;
  background-color: #ffffff;
  border: 1px solid #c9c9c9;
  border-top: 3px solid #0491e2;
  border-radius: 2px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  position: relative;

  .bg-text {
    position: absolute;
    font-size: 10em;
    clear: both;
    margin-top: 40px;
    margin-left: -20px;
    opacity: 0.1;
  }

  a {
    text-decoration: none;
    color: inherit;

    &:hover {
      color: #01ac26;
    }
  }
  h2 {
    font-size: 1.2em;
    font-weight: bold;
    &:after {
      content: ".";
      color: #01d62f;
    }
  }
  p {
    font-size: 0.9em;
    flex-grow: 1;
    margin: 20px 0px 10px 0px;
  }

  ul {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;

      li {
          padding: 4px 15px 4px 15px;
          margin: 5px;
          background-color: #02b820;
          color: white;
          font-size: 0.8em;
          border-radius: 20px;
          font-family: 'Courier New', Courier, monospace;
      }
  }
}
</style>
