<script lang='ts'>
  import HeroSection from '../lib/components/marketing/HeroSection.svelte';
  import AboutUsSection from '../lib/components/marketing/AboutUsSection.svelte'; 
  import ServicesSection from '../lib/components/marketing/ServicesSection.svelte';
  import MissionSection from '../lib/components/marketing/MissionSection.svelte';
  import TeamSection from '../lib/components/marketing/TeamSection.svelte';
  import ContactUsSection from '../lib/components/marketing/ContactUsSection.svelte';
</script>

<div class="parallax w-screen h-full">
  <div class="bg-white/60 w-screen h-full">
    <HeroSection />
    <ServicesSection />
    <MissionSection />
    <TeamSection />
    <ContactUsSection />
  </div>
</div>

<style>
  .parallax {
    background-image: url('../lib/assets/hero-background.png');
    background-size: cover;
    background-attachment: fixed;
  }
  @media only screen and (max-device-width: 1000px) {
    .parallax {
      background-attachment: scroll;
    }
  }
</style>