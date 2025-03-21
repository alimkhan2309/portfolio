<script>
import ButtonComponent from './ButtonComponent.vue';

export default {
    props: ['title', 'image'],
    components: { ButtonComponent }, // Fixed typo "component" → "components"
};
</script>

<template>
  <div class="card">
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
.card {
    width: clamp(280px, 24vw, 380px);
    height: 553px;
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
    width: 100%; /* Fill the entire card width */
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


@media :  {
    
};




</style>
