<template>
  <footer class="footer">
    <div class="container">
      <div class="card">
        <h4 class="subtitle">
          In Wetzlar and into programing?
          <br />You need to join our meetup!
        </h4>
        <p class="card-content">
          Every
          <strong>3rd Wednesday of the month</strong> you’ll find us talking
          about what we’re doing and what’s happening around us in the world of
          programing.
        </p>
        <div class="container-btn">
          <SecondaryBtn textContent="Join Our Slack " />
        </div>
      </div>
      <img src="@/assets/logo/DuckLogo.svg" alt="Wetzlar developers meetup" />
    </div>
  </footer>
</template>

<script>
import SecondaryBtn from "@/components/btn/SecondaryBtn";
export default {
  components: {
    SecondaryBtn
  },
  name: "Footer"
};
</script>

<style scoped lang="scss">
.footer {
  margin-top: 10rem;
  padding: 10rem 0 2rem;
  background: var(--main-color);
  position: relative;
  //   -webkit-clip-path: polygon(0 1%, 100% 23%, 100% 100%, 0% 100%);
  //   clip-path: polygon(0 1%, 100% 23%, 100% 100%, 0% 100%);
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }
  strong {
    font-weight: 500;
  }
}
.card {
  padding: 2rem;
  border-radius: 0.5rem;
  max-width: 800px;
  width: 80%;
  position: absolute;
  top: -8rem;
  z-index: 100;
  background: #fff;
  box-shadow: 0px 1px 1px rgba(10, 10, 10, 0.1);
  transition: all 0.3s ease-in-out;
}
.container::before {
  content: "";
  padding: 4rem;
  width: 110%;
  background: var(--secondary-color);
  position: absolute;
  right: -5rem;
  top: -3rem;

  transform: rotate(3deg);
}
.container-btn {
  margin-top: 2rem;
  --secondary-color: var(--main-color);
  --main-color: var(--secondary-color);
}
.card:hover {
  box-shadow: 0px 5px 40px rgba(10, 10, 10, 0.1);
  transform: translateY(-0.3rem) scale(1.01);
}
</style>
