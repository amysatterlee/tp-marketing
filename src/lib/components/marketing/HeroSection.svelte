<script lang="ts">
  import Logo from '../../assets/twinpeakslogo.png';
  import { goto } from '$app/navigation';
</script>

<div class="heroSection w-screen h-screen">
  <div class="flex bg-white/80 w-full h-full">
    <div class="flex flex-col w-full lg:flex-row lg:w-9/10 xl:w-2/3 m-auto h-9/10 lg:h-1/2 items-center">
      <img src={Logo} alt="Twin Peak Technologies" class="logo mt-5 lg:mt-0 mb-9 lg:mb-0"/>
      <div class="flex flex-1 flex-col items-center p-3">
        <div class="headline text-3xl md:text-5xl font-bold text-center mb-6 txt-primary">Scaling Your Business to New Peaks</div>
        <div class="subheadline text-2xl md:text-4xl text-center my-3 mx-3 txt-secondary">Innovative software solutions and expert consulting services designed to elevate your business performance.</div>
        <button type="button" on:click={() => goto('/contact')} class="btn-primary w-fit px-5 py-2 m-3" aria-expanded="false">Request a Consultation</button>
      </div>
    </div>
  </div>
</div>

<style>
  .heroSection {
    background-image: url('../../assets/hero-background.png');
    background-size: cover;
    &.headline {
      font-family: 'Roboto';
    }
    &.subheadline {
      font-family: 'Source Sans Pro';
    }
  }
  .logo {
    max-height: 300px;
  }
</style>