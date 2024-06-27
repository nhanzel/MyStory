<template>
    <div style="width: 80%;">
      <h1>Work History</h1>
      <p> - During the pandemic, I took some time off of school to work full time as a Software Engineer.</p>
      <p> - I worked at two companies during this time, <span class="bolded">FPS GOLD</span> (boring name) and <span class="bolded">Aristotle</span> (cool name).</p>
      <p> - I gained a LOT of professional and practical experience at this job, and I am 10x the programmer that I used to be because of these jobs. However, even after all of that, I would still rate this as an overall <span class="bolded">distressful</span> sitaution.</p>
      <p> - I wasn't happy where I was, I was feeling <span class="bolded">chronic stress</span> the entire time I was there. I am very glad I went back to part time work in order to persue school full time again.</p>
    </div>
    <div id="work-experience">
        <h2>FPS Gold (a division of DHICorp)</h2>
        <h3>- Program in C#, Knockout.js, and SQL.</h3>
        <h3>- Help small town banks and financial institutions with their software solutions <em>(yawn)</em></h3>
        <br>
        <h2>Aristotle</h2>
        <h3>- Program in C#, Vue.js, and SQL.</h3>
        <h3>- Help work on <a href="https://www.predictit.org/">PredictIt</a>, a website for betting on political events <em>(fun!)</em></h3>
    </div>
</template>
  
<script>
  export default {
    name: 'Work',
    data() {
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
  h2 {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    font-size: 1.7rem;
  }
  h3 {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

  }
  p {
    font-size: 1.1rem;
    margin-bottom: 1rem;
  }
  .bolded {
    font-weight: bold;
  }
  #work-experience {
    border: 2px solid green;
    border-radius: 10px;
  }
</style>