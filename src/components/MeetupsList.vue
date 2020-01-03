<template>
  <main class="main">
    <h1 class="title">Next meetups</h1>
    <section class="container">
      <div class="meetup--container">
        <Meetups v-for="meetups in allMeetups" :key="meetups.title" :item="meetups" />
      </div>
    </section>
  </main>
</template>

<script>
import Meetups from "./Meetup/Meetup";
export default {
  name: "MeetupList",
  components: {
    Meetups
  },
  data: function() {
    return {
      allMeetups: [
        {
          title: "Vuejs for php devs",
          date: "09/08/2020",
          imgUrl: require("@/assets/javascriptImage.png")
        },
        {
          title: "Vuejs vs Reactjs",
          date: "01/08/2020",
          imgUrl: require("@/assets/vuejsvsreact.png")
        },
        {
          title: "Job search",
          date: "03/08/2020",
          imgUrl: require("@/assets/jobSearch.png")
        },
        {
          title: "Docker game changer",
          date: "04/08/2020",
          imgUrl: require("@/assets/docker.png")
        },
        {
          title: "Kubernetes the new way",
          date: "05/08/2020",
          imgUrl: require("@/assets/kubernetes.png")
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
.main {
  padding: 2rem;
  background: #fff;
}
.meetup--container {
  margin-top: 4rem;
  display: grid;
  grid-gap: 2rem;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, minmax(150px, 200px));
  @media (max-width: 800px) {
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, minmax(150px, 200px));
  }
}
</style>
