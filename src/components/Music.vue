<template>
    <div>
        <h1>Music</h1>
        <p> - Enough about all of the events in my life, what about what I do to relax? Music is my number one
            destressor.</p>
        <p> - I love to collect vinyl records, going to concerts, and just talking about music in general.</p>
        <p> - I try to expose myself to all genres of music that I come across, that way I can strike up a conversation
            with anyone about their music tastes!</p>
        <p> - My favorite artists are The Maine, Radiohead, Sufjan Stevens, Phoebe Bridgers, Billy Joel, and Chris
            Botti.</p>
    </div>
    <div>
        <img :src="imageSource" alt="Chris Botti" width="500vw" height="600vh"></img>
        <p style="color: #D4D4D4; font-size: 14px;">a pic of the man Chris Botti himself, taken by me :)</p>
    </div>
</template>

<script>
import chrisBottiImage from '../assets/chris_botti.jpeg';
export default {
    name: 'Music',
    data() {
        return {
            imageSource: chrisBottiImage,
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
</style>