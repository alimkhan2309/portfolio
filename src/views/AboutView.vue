<script>
import CaseCard from '@/components/CaseCard.vue';

export default {
components: {CaseCard}
}

</script>
<template>
  <div class="about-section">
    <h1>Portfolio</h1>
    <div class="about-wrap">

      <div class="row-2">
        <div class="about-card card">
          <img src="@/assets/self.png" alt="">
          <div class="about-card-content">
            <h3>About Me</h3>
            <p>Web Developer with a passion for building fast and visually appealing websites. Highly adaptable to changing environments, with a keen eye for detail. </p>
          </div>      
        </div>
        <div class="tech-card card">
          <h3>Tech Stack</h3>
          <div class="icon-train">
            
          </div>
        </div>
      </div>

      <div class="row-1">
        <CaseCard title="Makeup School" image='case-study1.png'></CaseCard>
        <CaseCard title="AI Startup" image='case-study2.png'></CaseCard>
        <CaseCard title="Makeup School" image='case-study3.png'></CaseCard>
      </div>
      
    </div>
  </div>
</template>


<style scoped lang="css">

h1 {
  color:var(--white);
  font-size:64px;
  padding: 4rem 0;
}

.about-section {
  width:fill;
  height:fit-content;
  background-color: var(--black);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap:32px;
}


.row-1 {
  width:100%;
  display: flex;
  flex-direction: row;
  /* align-items: center; */
  /* justify-content:center; */
  gap: 32px;
  /* justify-content: space-around; */
  /* flex-wrap: wrap; */
  /* padding: 0 128px; */
}

.row-2 {
  width:fill;
  display: flex;
  flex-direction: row;
  gap: 32px;
  /* align-items: center; */
  /* justify-content: start; */
  /* flex-wrap: wrap; */
}

.about-card {
  width: clamp(18.375rem, 15.061274509803923rem + 13.594771241830065vw, 31.375rem);
  height: 416px;
  justify-content: start;
}
.about-wrap {
  width: fill;
  padding: 64px 128px;
  display: flex;
  flex-direction:column;
  gap:32px;
}

.tech-card {
  width:fill;
  height: 416px;
  /* height:fit-content; */
}

.icon-train {
  width: fill;
  background-color:white;
}


.about-card-content {
  padding: 12px 32px;
}

.about-card img {
  padding: 32px 0 0 0;
}

.about-card h3 {
  font-size: 36px;
  padding: 12px 0;
}
.about-card p {
  color: var(--light-grey)
}

</style>