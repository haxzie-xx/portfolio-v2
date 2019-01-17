<template>
  <div class="profile-container">
    <div class="column texts">
      <p class="intro">Hi there, I am</p>
      <h1 class="name" data-text="Musthaq Ahamad">Musthaq Ahamad</h1>
      <p class="bio">
        I am a hobbyist developer and designer who loves open source and helps others to adopt it.
        I build things for fun for Android and web using React and Node.
      </p>
    </div>
    <div class="column picture">
      <div class="anim"></div>
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
@keyframes sparkle {
  from {
    background-position: 0% 100%;
  }
  to {
    background-position: 200% 100%;
  }
}

$c1: #006eff;
$c2: #04f14b;
$c3: #ec0b43;

.profile-container {
  display: flex;
  flex-direction: row;
  flex-grow: 1;
  margin-top: 50px;

  .column {
    width: 50%;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
  }

  .texts {
    height: auto;
    padding-right: 20px;
    justify-content: center;
    .intro {
      font-size: 2em;
    }
    .name {
      font-size: 3em;
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
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    .anim {
      opacity: 0.5;
      max-width: 410px;
      max-height: 410px;
      min-width: 410px;
      min-height: 410px;
      animation: sparkle 4s infinite linear;
      background: linear-gradient(
        90deg,
        $c1 0%,
        $c2 11%,
        $c3 22%,
        $c1 33%,
        $c2 44%,
        $c3 55%,
        $c1 66%,
        $c2 77%,
        $c3 88%,
        $c1 100%
      );
      background-size: 300% 100%;
      content: "";
      position: absolute;
      width: 100%;
      height: 100%;
      border-radius: 50%;
      filter: blur(5px);
      z-index: -1;
      transform: scale(0.99) translateY(3px);

      &:hover {
        opacity: 1;
      }
    }
    .photo {
      min-width: 400px;
      min-height: 400px;
      background-image: url("../assets/photo.png");
      background-size: auto 100%;
      background-position: center;
      border-radius: 50%;
      &:hover > .anim {
        opacity: 1;
      }
    }
  }
}

@media (max-width: 768px) {
  .profile-container {
    flex-direction: column-reverse;
    min-height: 100%;
    margin-top: 0;
    .column {
      width: 100%;
    }
    .texts {
      padding: 0 0 0 0;
      align-items: center;
    }
    .intro {
      text-align: center;
      font-size: 2em;
    }
    .name {
      font-size: 2.5em;
      text-align: center;
    }
    .bio {
      text-align: center;
    }

    .photo, .anim {
      min-width: 300px;
      min-height: 300px;
      max-width: 300px;
      max-height: 300px;
    }
  }
}

@media (min-width: 360px) and (max-width: 480px) {
  .profile-container {
    flex-direction: column-reverse;
    margin-top: 0;
    .column {
      width: auto;
      .texts {
        padding: 0 0 0 0;
        align-items: center;
      }
      .intro {
        text-align: center;
        font-size: 1.2em;
      }
      .name {
        font-size: 2em;
      }
      .bio {
        text-align: center;
      }
      .picture {
        justify-content: flex-start;
        width: auto;
      }
      .photo, .anim {
        min-width: 240px;
        min-height: 240px;
        max-width: 240px;
        max-height: 240px;
      }
    }
  }
}
</style>
