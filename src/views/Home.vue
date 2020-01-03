<template>
  <div class="home">
    <Hero />
    <MeetupsList />
    <Sponsors />
  </div>
</template>

<script>
// @ is an alias to /src
import Hero from "@/components/Hero";
import MeetupsList from "@/components/MeetupsList";
import Sponsors from "@/components/Sponsors";

export default {
  name: "home",
  components: {
    Hero,
    MeetupsList,
    Sponsors
  }
};
</script>
