<template>
  <section class="section-sponsors">
    <div class="container">
      <h2 class="title">Our sponsors</h2>
      <p class="subtitle">
        We are a perfect group to sponsor for any company or school that wishes
        to attract more talent or candidates especially for classes, workshops,
        trainings and job offers. Build your list and presence with this group
        for way less than what it costs to advertise on popular Social Media
        Platforms (e.g. Big Tech), and the great thing is you’ll reach real
        people
        <span class="bg">(not robots and fake profiles)!</span>
      </p>
      <p class="subtitle">
        If you want to become a sponsor of our group, simply contact us via our
        email
        <a href="mailto:info@wetzlar.dev">info@wetzlar.dev</a> .Please ask about
        Sponsorships in the subject line.
      </p>
      <div class="container-sponsors">
        <img
          class="sponsors-logos"
          src="@/assets/sponsors/reflectMedia.png"
          alt="Reflect medialogo"
        />
        <img class="sponsors-logos" src="@/assets/sponsors/atlasian.png" alt />
        <img
          src="@/assets/sponsors/digitalOcean.png"
          alt
          class="sponsors-logos"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Sponsors"
};
</script>

<style scoped>
.section-sponsors {
  padding: 4rem 0 6rem;
  background: url("../assets/SponsorBg.svg") no-repeat center center / 70%,
    var(--secondary-color);
}

.title {
  margin-bottom: 2rem;
}
.container-sponsors {
  margin-top: 4rem;
  display: grid;
  grid-template-columns: repeat(3, minmax(150px, 1fr));
  grid-gap: 2rem;
}
.sponsors-logos {
  display: block;
  max-height: 80px;
  width: 100%;
}
.bg {
  background: var(--textbg-color);
  color: var(--secondary-color);
}
</style>
