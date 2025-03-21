
<template>
  <section>
    <div class="content">
      <div class="title">
        <h3>Front-end Developer</h3>
        <h1>Alimkhan Zhanaladin</h1>
      </div>       
      <ButtonComponent 
        text = "Let's connect"
        type = "Primary"/>
    </div>
  </section>
</template>

<script>
import ButtonComponent from '@/components/ButtonComponent.vue';

export default {
  components: {ButtonComponent}
}
</script>

<style scoped lang="css">
* {
  padding: 0;
  margin: 0;
}
section {
  width: 100%;
  height: 100vh;
  /* background-color:black; */
  background-image: url('@/assets/background.jpg');
  display: flex;
  flex-direction: column;
  justify-content: end;
  align-items: start;
}
.content {
  width: 715px;
  z-index: 10;
  margin: 0 0 88px 64px;
  display: flex;
  flex-direction: column;
  gap:32px;
}

h1 {
  font-size:128px;
  color: white;
}
h3 {
  font-size: 32px;
  color: #8D7DE8;
}
</style>