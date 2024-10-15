<template>
  <div>
    <section class="row" id="landing">
      <LandingSection /> 
    </section>

   
    <section class="row max-height" id="about">
      <h2 class="main-heading">About</h2>
      <AboutSection/>
    </section>

    <section class="row max-height" id="skills">
      <h2 class="main-heading">Skills</h2>
      <SkillsSection />
    </section>

    <section class="row max-height" id="education">
      <h2 class="main-heading">Education & Experience</h2>
      <EducationSection />
    </section>

    <section class="row max-height" id="certifications">
      <h2 class="main-heading">My Certifications</h2>
      <p> These Are The Certifications I Aquired During My Journey.</p>
      <Certification />
    </section>

    <!-- <section class="row max-height" id="testimonials">
      <h2 class="main-heading">Testimonials</h2>
      <TestimonialsSection />
    </section> -->

    <section class="row max-height" id="projects">
      <h2 class="main-heading">Projects</h2>

      <ProjectsSection />
    </section>

    <section class="row max-height" id="contact">
      <h2 class="main-heading">Contact</h2>
      <ContactSection />
    </section>

  </div>
</template>

<script>
import LandingSection from '@/components/LandingSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import EducationSection from '@/components/EducationSection.vue'
import SkillsSection from '@/components/SkillsSection.vue'
import Certification from '@/components/Certification.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
import ContactSection from '@/components/ContactSection.vue'
export default {
  name: 'HomeView',
  components: {
    LandingSection,
    AboutSection,
    EducationSection,
    SkillsSection,
    Certification,
    ProjectsSection,
    ContactSection
  }
}
</script>

<style scoped>

#projects{
  margin-top: 30rem;  
}

  #education h2{

    margin-bottom: 4rem;
  }

  p {
    font-size:1.2rem;
    color:#fff;
    font-weight:400;
  }
</style>