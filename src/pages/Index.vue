<template>
  <Layout>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

    <h1>Hello, world!</h1>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur
      excepturi labore tempore expedita, et iste tenetur suscipit explicabo!
      Dolores, aperiam non officia eos quod asperiores
    </p>

    <Button
      url="http://www.brixtoncycles.com"
      text="Button Test"
      variant="primary"
    />
    <Card />

    <p class="home-links">
      <a href="https://gridsome.org/docs/" target="_blank" rel="noopener"
        >Gridsome Docs</a
      >
      <a
        href="https://github.com/gridsome/gridsome"
        target="_blank"
        rel="noopener"
        >GitHub</a
      >
    </p>
  </Layout>
</template>

<script>
import Button from "~/components/ButtonLink.vue";
import Card from "~/components/Card.vue";

export default {
  name: "index",
  components: {
    Card,
    Button
  },
  metaInfo: {
    title: "Hello, test page"
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
