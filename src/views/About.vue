<template>
  <div class="about">
    <HeroBlog
      title="About us"
      subtitle="A group for anyone interested in all
    kind of programming. Visit
    <a href='https://wetzlar.dev'>https://wetzlar.dev</a> for more info on us,
    the meetups we've held, videos you can watch on Youtube and blogs offering
    technical expertise."
    />
  </div>
</template>
<script>
import HeroBlog from "@/components/HeroBlog";
export default {
  name: "About",
  components: {
    HeroBlog
  }
};
</script>
