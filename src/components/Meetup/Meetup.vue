<template>
  <article class="meetup-item" :style="meetupStyleHover">
    <h3 class="meetup-item__title">{{ item.title }}</h3>
    <small class="meetup-item__date">{{ item.date }}</small>
  </article>
</template>

<script>
export default {
  props: {
    item: {
      type: Object
    }
  },
  name: "Meetup",
  data: function() {
    return {
      itemStyle: {
        background: `url(${this.item.imgUrl}) no-repeat center  / 100% `,
        backgroundHover: `linear-gradient(45deg, rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)),url(${this.item.imgUrl}) no-repeat  center  `
      }
    };
  },
  computed: {
    meetupStyleHover: function() {
      return {
        "--meetup-itembg": this.itemStyle.background,
        "--meetup-itembg--hover": this.itemStyle.backgroundHover
      };
    }
  }
};
</script>

<style>
.meetup-item {
  padding: 1rem;
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out,
    background-size 0.5s ease-in-out;
  border-radius: 0.3rem;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-end;
  color: var(--secondary-color);

  font-size: 0.9rem;
  line-height: 1.3;
  background: var(--meetup-itembg);
  background-repeat: no-repeat;
  background-size: 150%;
}
.meetup-item:hover {
  background: var(--meetup-itembg--hover);
  background-size: 110%;
  transform: translate3d(0px, -0.1rem, 0px) scale(1.05);
  box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
}
.meetup-item__title {
  background: var(--textbg-color);
}
.meetup-item__date {
  margin-top: 0.3rem;
  background: var(--textbg-color);
}
</style>
