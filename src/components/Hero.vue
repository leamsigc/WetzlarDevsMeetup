<template>
  <section class="section-hero" :style="heroStyle">
    <div class="container">
      <div class="hero-title">
        <h1 class="title">Welcome to Wetzlar Devs</h1>
        <p>
          We are a community of software developers in Wetzlar, Germany. Whether
          you love writing code or are just getting started, you are welcome
          here!
        </p>
      </div>
      <div class="btn-container">
        <SecondaryBtn v-for="btn in heroBtns" :key="btn" :textContent="btn" />
      </div>
    </div>
  </section>
</template>

<script>
import WetzlarBg from "../assets/Wetzlar.png";
import SecondaryBtn from "./btn/SecondaryBtn";
export default {
  components: {
    SecondaryBtn
  },
  name: "Hero",
  data: function() {
    return {
      heroStyle: {
        background: `linear-gradient(45deg, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.6))
        ,url(${WetzlarBg}) no-repeat center bottom / cover`
      },
      heroBtns: [
        "Join  our Slack",
        "Join our Meetup",
        "Become Patreon",
        "Contribute Code"
      ]
    };
  }
};
</script>

<style scoped lang="scss">
.section-hero {
  color: var(--secondary-color);
  padding: 2rem 1rem;
  min-height: 80vh;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  text-align: left;

  @media (max-width: 800px) {
    flex-direction: column;
    min-height: 50vh;
  }
}
.btn-container {
  flex: 1 1 1;
  margin: 4rem 0 5rem;
  display: flex;
  @media (max-width: 800px) {
    flex-wrap: wrap;
    justify-content: center;
    .btn {
      margin-bottom: 1rem;
      margin-left: 0;
    }
  }
}
.btn-container .btn:not(:first-child) {
  margin-left: 1rem;
}
</style>
