<script lang="ts">
  import AmyImage from '../../assets/amy.png';
  import ShawnImage from '../../assets/shawn.png';
</script>

<div class="w-full bg-slate-100 h-full">
  <div class="aboutUsSection w-full lg:w-2/3 lg:m-auto">
    <div class="headline text-center text-2xl md:text-3xl lg:text-4xl py-3 lg:py-6 font-semibold">About Us</div>
    <div class="subheadline text-center text-md md:text-lg px-1">At Twin Peak Technologies, we are dedicated to empowering small and medium-sized businesses with world class cloud infrastructure and software development solutions. Our mission is to provide scalable, secure, and cost-effective software development and site reliability engineering services, empowering companies that may not have the budget for full-time, in-house teams. Whether it's building robust cloud infrastructure, implementing AI-driven solutions, or developing cutting-edge front-end and back-end applications, we deliver results tailored to your business needs.</div>
    <div class="subheadline text-center text-md md:text-lg px-1 my-3">With decades of combined experience in software engineering and IT leadership, our founders, Amy and Shawn, bring deep expertise and a shared passion for technology.</div>
    <div class="flex flex-col lg:flex-row items-center lg:mx-12">
      <img class="w-32 h-32 lg:w-40 lg:h-40 my-3 rounded-3xl mr-3" src={ShawnImage} alt="Shawn"/>
      <div class="subheadline text-center lg:text-left text-md md:text-lg px-1 my-3"><span class="font-bold">Shawn</span> is a seasoned leader with extensive experience in DevOps and IT engineering. He has a proven track record of building secure, stable, and cost-effective cloud solutions that scale with business growth. As a seasoned DevOps architect and site reliability expert, Shawn's career includes leadership roles at KnowBe4 and Malwarebytes, where he directed teams to deliver resilient and scalable cloud platforms.</div>
    </div>
    <div class="flex flex-col lg:flex-row-reverse items-center lg:mx-12">
      <img class="w-32 h-32 lg:w-40 lg:h-40 my-3 rounded-3xl ml-3" src={AmyImage} alt="Amy"/>
      <div class="subheadline text-center lg:text-right text-md md:text-lg px-1 my-3"><span class="font-bold">Amy</span> is a multi-talented software engineer with an expertise in full-stack software development. She has consistently delivered top-notch frontend and backend solutions for major companies like KnowBe4 and Malwarebytes. Her passion lies in creating efficient, user-centric software that drives business success.</div>
    </div>
    <div class="subheadline text-center text-md md:text-lg px-1 py-6 lg:py-12">Together, we are committed to making cutting-edge technology accessible to businesses of all sizes. Our services cover every aspect of software development and site reliability engineering, ensuring that your systems are not only built to perform but also optimized for the future. From cloud infrastructure to web development to AI integration, we’re here to support your business every step of the way.</div>
  </div>
</div>

<style>
  .aboutUsSection {
    &.headline {
      font-family: 'Roboto';
    }
    &.subheadline {
      font-family: 'Source Sans Pro';
    }
  }
</style>