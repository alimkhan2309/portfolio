<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
    props: ['title', 'image'],
    components: { ButtonComponent }, 
};
</script>

<template>
  <div class="case-card">
    <div class="image-container">
      <img :src="require(`@/assets/${image}`)" alt="Project Display">
    </div>
    <div class="info-bar">
      <h3>{{ title }}</h3>
      <ButtonComponent text="Learn More" type="secondary"></ButtonComponent>
    </div>  
  </div>
</template>

<style scoped>
.case-card {
    /* width: clamp(280px, 24vw, 380px); */
    /* width: clamp(18.375rem, 15.061274509803923rem + 13.594771241830065vw, 31.375rem); */
    width:fill;
    aspect-ratio: 502/738;
    /* height: 553px; */
    background-color: var(--dark-grey);
    display: flex;
    flex-direction: column;
    align-content: start;
    justify-content: end;
    border-radius: 40px;
    overflow: hidden; /* Prevents image overflow */
    position: relative; /* Keeps children positioned inside */
}

.image-container {
    width: 100%;
    height: 100%;
    position: relative;
}

img {
    width: 100%; /* Make image fill the container */
    height: 100%; /* Ensure image covers full height */
    object-fit: cover; /* Maintain aspect ratio and crop */
}

.info-bar {
    width: Fill; /* Fill the entire card width */
    background-color: var(--grey);
    color: var(--white);
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    padding: 16px 32px;
    z-index: 1;
    border-radius: 0 0 40px 40px;
}
</style>
