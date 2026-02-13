<template>
  <div class="min-h-screen bg-linear-to-br from-gray-800 via-blue-900 to-bg-gray-800">
    <NavBar />
    <Hero />
    <Service />
    <Education />
    <!-- <Skill /> -->
    <Project />
    <About />
    <Contact />
    <Footer />

  </div>
</template>
<script>
import Aos from 'aos';
import 'aos/dist/aos.css';
import Hero from './components/Hero.vue';
import NavBar from './components/NavBar.vue';
import { ref, nextTick, onMounted } from 'vue';
import Service from './components/Service.vue';
import Education from './components/Education.vue';
import Project from './components/Project.vue';
import About from './components/About.vue';
import Footer from './components/Footer.vue';
import Contact from './components/Contact.vue';
import Skill from './components/Skill.vue';
export default {
  components: {
    NavBar,
    Hero,
    Service,
    Education,
    Project,
    About,
    Contact,
    Footer,
    Skill
  },
  setup() {
    const loading = ref(true);
    onMounted(async () => {
      await nextTick();
      Aos.init({
        duration: 1000,
        once: false,
        offset: 100,
        easing: 'ease-in-out'
      });
      setTimeout(() => {
        loading.value = false;
      }, 800);
    });
    return { loading };
  }
}
</script>
<style></style>