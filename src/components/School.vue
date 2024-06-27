<template>
    <div>
        <img :src="imageSource" alt="UVU Logo" width="550vw" height="550vh"></img>
    </div>
    <div>
        <h1>Schooling</h1>
        <p> - I started school in 2018 after graduating high school and I loved it! UVU is a great example of
            <span class="bolded">eustress</span>.
        </p>
        <p> - I have always been very studious, and all of the subjects that I have taken so far have been interesting
            to learn about!</p>
        <p> - I am on track to graduate with my bachelor's degree in the spring of 2025, which technically makes me a
            super senior.</p>
        <p> - Since moving to part time work, my sister and brother-in-law have been kind enough to let me move in with
            them. This has caused some <span class="bolded">acute</span> stress since I don't want to be a bother, but I
            recognize my fear is irrational.</p>
    </div>
</template>

<script>
import uvuLogoImage from '../assets/uvu_logo.jpg';

export default {
    name: 'School',
    data() {
        return {
            imageSource: uvuLogoImage,
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