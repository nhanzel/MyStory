<template>
    <div>
        <img :src="imageSource" alt="Lds Logo" width="550vw" height="550vh"></img>
    </div>
    <div>
      <h1>My Deconstruction</h1>
      <p> - I grew up in the Mormon Church, and while many have negative experiences with the church, I enjoyed going every Sunday and hanging out with my friends.</p>
      <p> - However, as I looked into the history of the church I came to realize I didn't believe in the doctrine of the church. I kept up appearances until I was 18, but once I moved out on my own I left the church.</p>
      <p> - I can't think of a better example of <span class="bolded">eustress</span> in my life than my deconstruction. I went through years of stress and anxiety over my decision and my family dynamics were stretched. However, I have come out stronger on the other side. I have a new perspective on my life, the people in it, and treating everyone with respect.</p>
      <p> - I don't have anything negative against Mormons, most of my family and friends are still in the faith, but I'm glad to have my new sense of empathy and acceptance with the life we're given.</p>
    </div>
</template>
  
<script>
  import ldsLogoImage from '../assets/lds_logo.jpg';

  export default {
    name: 'Deconstruction',
    data() {
      return {
        imageSource: ldsLogoImage,
      };
    },
    methods: {
    },
  };
</script>
  
<style scoped>
  div {
    margin: 0 auto;
    max-width: 100%;
    padding: 1rem;
  }
  h1 {
    font-size: 4rem;
    margin-bottom: 1rem;
    color: green;
  }
  p {
    font-size: 1.1rem;
    margin-bottom: 1rem;
  }
  .bolded {
    font-weight: bold;
  }
</style>