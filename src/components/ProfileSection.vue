<template>
  <div class="profile-container">
    <div class="column texts">
      <p class="intro">Hi there, I am...</p>
      <h1 class="name">Musthaq Ahamad</h1>
      <p class="bio">
        I am a hobbyist developer and designer who loves open source and helps others to adopt it.
        I build things for fun for Android and web using React and Node.
      </p>
    </div>
    <div class="column picture">
      <div class="photo blue"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileSection"
};
</script>

<style lang="scss" scoped>
.profile-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;

  .column {
    width: 50%;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .texts {
    height: auto;
    padding-right: 20px;
    justify-content: center;
    .intro {
      font-size: 2em;
    }
    .name {
      font-size: 4em;
      line-height: 1.2em;
      margin-top: 10px;

      &:after {
        content: ".";
        color: #01d62f;
      }
    }
    .bio {
      margin-top: 30px;
      font-size: 1em;
    }
  }
  .picture {
      display: flex;
      justify-content: center;
      align-items: center;
    .photo {
      min-width: 450px;
      min-height: 500px;
      background-image: url('../assets/photo.png');
      background-size: auto 100%;
      background-position: center;
    }
  }
}
</style>
