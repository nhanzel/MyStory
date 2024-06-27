<template>
    <div>
      <h1 v-if="!showFamilyMessage">Hello World!</h1>
      <h1 v-if="showFamilyMessage">My Family! Wow!</h1>
      <p> - My name is <span class="bolded">Nathan Hanzel</span>, and I was born in Boise, Idaho before moving to Oregon when I was one year old. I lived in Oregon for 6 years and to this day it remains my happy place. Anywhere on the West Coast makes me happy (my parents currently live in San Francisco).</p>
      <p> - I have three siblings and two sibling-in-laws who all live in Utah.</p>
      <p> - I am a CS Major with one year left (fingers crossed I don't fail any classes), and I decided what better way to share my story than with a custom website!</p>
    </div>
    <div>
        <img :src="imageSource" :class="{'image-transition': true, 'fade-out': isFading}"
        @transitionend="handleTransitionEnd" alt="Oregon and Idaho" width="550vw" height="350vh"></img>
        <button @click="clickFamily">{{familyButtonText}}</button>
    </div>
</template>
  
<script>
  import oregonAndIdahoImage from '../assets/oregon_and_idaho.jpg';
  import familyImage from '../assets/family.jpeg';

  export default {
    name: 'Introduction',
    data() {
      return {
        imageSource: oregonAndIdahoImage,
        showFamilyMessage: false,
        familyButtonText: "See the family!",
        isFading: false,
        newImageSource: null,
      };
    },
    methods: {
      clickFamily() {
        this.newImageSource = this.imageSource === familyImage ? oregonAndIdahoImage : familyImage;
        this.showFamilyMessage = !this.showFamilyMessage;
        this.familyButtonText = this.showFamilyMessage ? "See Oregon and Idaho :(" : "See the family!";
        this.isFading = true;
      },
      handleTransitionEnd() {
        if (this.isFading) {
          this.imageSource = this.newImageSource;
          this.isFading = false;
        }
      },
    },
  };
</script>
  
<style scoped>
  button {
    background-color: green;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }
  button:hover {
    font-weight: bold;
  }
  div {
    margin: 0 auto;
    max-width: 800px;
    padding: 1rem;
  }
  h1 {
    font-size: 5rem;
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
  .image-transition {
    transition: opacity 0.5s;
  }
  .fade-out {
    opacity: 0;
  }
</style>