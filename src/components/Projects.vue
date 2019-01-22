<template>
  <div class="project-section">
    <h2>What I work on</h2>
    <div class="project-grid">
        <ProjectCard v-for="(project, index) in projects" :key="index" :details="project"/>
    </div>
    <p class="external-link">View all my projects on <a href="https://github.com/haxzie">GitHub</a></p>
  </div>
</template>

<script>
import ProjectCard from './ProjectCard'

export default {
  name: "Projects",
  components: {
      ProjectCard
  },
  data: () => ({
      projects: [
          {
              name: "Wring.js",
              link: `https://github.com/haxzie/wring.js`,
              tags: ['Typescript', 'node.js', 'npm'],
              description: `Dead Simple String formatting and templating for humans and bots. This NPM module helps in easily managing strings for building bots.`
          },
          {
              name: "GitMe Bot",
              link: `https://github.com/haxzie/gitme`,
              tags: ['React.js', 'Gatsby', 'Probot'],
              description: `A Probot automated Git and GitHub workshop exercise for beginners to help make their fist open source contribution.`
          },
          {
              name: "Stackby",
              link: `https://github.com/haxzie/stackby`,
              tags: ['Python', 'PyPI', 'CLI'],
              description: `Python command line application to replicate the MacOS mojave stack feature. Stack files based on extension, type, and created date.`
          },
          {
              name: "SOSC-Website",
              link: `https://github.com/haxzie/sosc-website`,
              tags: ['React.js', 'Gatsby', 'SPA'],
              description: `Official website for Sahyadri Open Source Community, build with React and Gatsby static site generator. Includes features like Blogs, events, etc.`
          },
          {
              name: "Slidex",
              link: `https://github.com/haxzie/slidex`,
              tags: ['Node.js', 'npm', 'CLI'],
              description: `A web remote controller (Node CLI) from any of your device on a network to control presentations.`
          },
          {
              name: "Driodo",
              link: `https://github.com/haxzie/driodo`,
              tags: ['Android', 'Java'],
              description: `A Driving Assistant app to generate driving routes and to alert on realtime speedlimit violation and provide defensive driving tips.`
          }

      ]
  })
};
</script>

<style lang="scss" scoped>
.project-section {
  margin-top: 50px;
  display: flex;
  flex-direction: column;

  h2 {
    font-size: 2em;
    padding: 20px 0px 20px 0px;

    &:after {
      content: ".";
      color: #01d62f;
    }
  }
  .project-grid {
      display: grid;
      widows: 100%;
      grid-template-columns: repeat( auto-fit, minmax(300px, 1fr));
      grid-row-gap: 10px;
      grid-column-gap: 10px;
      margin-top: 10px;
  }

  .external-link {
      padding: 20px 0px 20px 0px;
      font-weight: bold;

      a {
          text-decoration: none;
          color: #01d62f;
      }
  }
}
</style>
