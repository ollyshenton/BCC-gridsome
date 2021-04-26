<template>
  <Layout>
    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/assets/images/bc-shop-s.jpg" width="250" />

    <h1>Brixton Cycles Club</h1>

    <p>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur
      excepturi labore tempore expedita, et iste tenetur suscipit explicabo!
      Dolores, aperiam non officia eos quod asperiores
    </p>

    <Button
      url="http://www.brixtoncycles.co.uk"
      text="Button Test"
      variant="primary"
      icon='light'
    />
    <Card /> 

    <Button
      url="http://www.brixtoncycles.co.uk"
      text="Button Secondary"
      variant="secondary" 
      icon='light'
    >
      <svgContent>
        SVG 
      </svgContent>
    </Button>

     <Button
      url="http://www.brixtoncycles.co.uk"
      text="Button Secondary"
      variant="secondary" 
      icon='light'
    />


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
