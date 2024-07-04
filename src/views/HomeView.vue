<template>
  <div>
    <section class="row" id="landing">
      <LandingSection /> 
    </section>

   
    <section class="row max-height" id="about">
      <h2 class="main-heading">About</h2>
      <AboutSection/>
    </section>

    <section class="row max-height" id="education">
      <h2 class="main-heading">Education</h2>
      <EducationSection />
    </section>

    <section class="row max-height" id="skills">
      <h2 class="main-heading">Skills</h2>
      <SkillsSection />
    </section>

    <section class="row max-height" id="testimonials">
      <h2 class="main-heading">Testimonials</h2>
    </section>

    <section class="row max-height" id="projects">
      <h2 class="main-heading">Projects</h2>
    </section>

    <section class="row max-height" id="contact">
      <h2 class="main-heading">Contact</h2>
    </section>

  </div>
</template>

<script>
import LandingSection from '@/components/LandingSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import EducationSection from '@/components/EducationSection.vue'
import SkillsSection from '@/components/SkillsSection.vue'
export default {
  name: 'HomeView',
  components: {
    LandingSection,
    AboutSection,
    EducationSection,
    SkillsSection
  }
}
</script>