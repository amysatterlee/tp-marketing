<script lang="ts">
  let activeSlide = 1;

  const onClick = (offset: number) => {
    let newSlide = activeSlide + offset;
    if (newSlide < 1) {
      newSlide = 3;
    } else if (newSlide > 3) {
      newSlide = 1;
    }
    activeSlide = newSlide;
  }
</script>

<div class="w-full bg-slate-100 py-6 lg:py-12">
  <div class="section-container">
    <div class="txt-category">SERVICES</div>
    <div class="flex flex-col lg:flex-row items-center justify-center mb-3 lg:mb-6">
      <div class="txt-headline flex-1">From Base Camp to Summit: Guiding Your Business to Tech Mastery</div>
      <div class="txt-subheadline flex-1 text-center lg:ml-3">We provide a full suite of services to drive your business forward. Whether you need scalable cloud computing, infrastructure, and CI/CD solutions to optimize operations, custom software development to bring your vision to life, or expert technical consulting to navigate complex challenges, we’re here to guide you every step of the way. Our mission is to empower startups and small businesses with the tools and expertise to reach new heights in technology mastery.</div>
    </div>
    <div class="slideshow-container mt-3 lg:mt-6">
      <div class={`slideshow-item slideshow-fade lg:animate-none ${activeSlide === 1 ? 'slide-active' : ''}`}>
        <div class="bg-slate-500 w-full aspect-[2/1] mb-3 lg:mb-6"></div>
        <div class="txt-subheadline font-bold text-center">Elevate Your Business With Tailored Software Solutions</div>
        <div class="h-2 w-2/5 border-teal-600 border-t-2 m-auto mb-3"></div>
        <div class="text-center">We build custom software tailored to your unique business needs. Whether it's a sleek web app, robust backend, powerful APIs, or AI integration, we have the expertise to bring your vision to life. Our team delivers scalable, high-performance solutions that enhance productivity, streamline operations, and drive growth. Let us turn your ideas into reality with our end-to-end software development services.</div>
      </div>
      <div class={`slideshow-item slideshow-fade lg:animate-none ${activeSlide === 2 ? 'slide-active' : ''}`}>
        <div class="bg-slate-500 w-full aspect-[2/1] mb-3 lg:mb-6"></div>
        <div class="txt-subheadline font-bold text-center">Power Your Growth with Scalable Cloud Computing Services</div>
        <div class="h-2 w-2/5 border-teal-600 border-t-2 m-auto mb-3"></div>
        <div class="text-center">We offer expert cloud computing services designed to optimize performance and reduce costs. Specializing in AWS cloud infrastructure, CI/CD pipelines, and Infrastructure as Code (IaC), we ensure your cloud environment is scalable, efficient, and secure. Our tailored solutions help streamline development, automate deployments, and maximize your cloud investments, so your business can grow without limits.</div>
      </div>
      <div class={`slideshow-item slideshow-fade lg:animate-none ${activeSlide === 3 ? 'slide-active' : ''}`}>
        <div class="bg-slate-500 w-full aspect-[2/1] mb-3 lg:mb-6"></div>
        <div class="txt-subheadline font-bold text-center">Expert Technical Consulting to Drive Innovation and Efficiency</div>
        <div class="h-2 w-2/5 border-teal-600 border-t-2 m-auto mb-3"></div>
        <div class="text-center">Our technical consulting services provide the expertise and guidance you need to tackle complex challenges and achieve your business goals. From optimizing infrastructure to adopting new technologies, we provide strategic insights and hands-on support. We help you streamline operations, reduce costs, and position your business for long-term success.</div>
      </div>
      <button class="prev" on:click={() => onClick(-1)}>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-10">
          <path fill-rule="evenodd" d="M7.72 12.53a.75.75 0 0 1 0-1.06l7.5-7.5a.75.75 0 1 1 1.06 1.06L9.31 12l6.97 6.97a.75.75 0 1 1-1.06 1.06l-7.5-7.5Z" clip-rule="evenodd" />
        </svg>        
      </button>
      <button class="next" on:click={() => onClick(1)}>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="size-10">
          <path fill-rule="evenodd" d="M16.28 11.47a.75.75 0 0 1 0 1.06l-7.5 7.5a.75.75 0 0 1-1.06-1.06L14.69 12 7.72 5.03a.75.75 0 0 1 1.06-1.06l7.5 7.5Z" clip-rule="evenodd" />
        </svg>        
      </button>
    </div>
    <div class="slideshow-progress-bar">
      <div class={`slideshow-progress-circle ${activeSlide === 1 ? 'slide-active' : ''}`}></div>
      <div class={`slideshow-progress-circle ${activeSlide === 2 ? 'slide-active' : ''}`}></div>
      <div class={`slideshow-progress-circle ${activeSlide === 3 ? 'slide-active' : ''}`}></div>
    </div>
  </div>
</div>