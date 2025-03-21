<script>
import CaseCard from '@/components/CaseCard.vue';

export default {
components: {CaseCard}
}

</script>
<template>
  <div class="about">
    <h1>Portfolio</h1>
    <div class="bento-box">
      <CaseCard title="Makeup School" image='case-study1.png'></CaseCard>
      <CaseCard title="AI Startup" image='case-study2.png'></CaseCard>
      <CaseCard title="Makeup School" image='case-study3.png'></CaseCard>
    </div>
  </div>
</template>





<style scoped>

.about {
  width:100%;
  height:100vh;
  background-color: var(--black);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  /* padding: 64px; */
  gap:64px;
}

h1 {
  color:var(--white);
  font-size:64px;
}

.bento-box {
  /* width:100%; */
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content:center;
  gap: 32px;
  flex-wrap: wrap;
}

</style>