<script lang="ts">
  let activeSlide = 1;

  const onClick = (offset: number) => {
    let newSlide = activeSlide + offset;
    if (newSlide < 1) {
      newSlide = 2;
    } else if (newSlide > 2) {
      newSlide = 1;
    }
    activeSlide = newSlide;
  }
</script>

<div class="w-full bg-slate-100 py-6 lg:py-12">
  <div class="section-container">
    <div class="text-center lg:text-left txt-category">MEET</div>
    <div class="flex flex-col lg:flex-row items-start justify-center">
      <div class="flex flex-col flex-2 mr-6 lg:mr-12">
        <div class="txt-headline text-center lg:text-left">Our Team</div>
        <div class="txt-subheadline text-center lg:text-left">With decades of combined experience in software engineering and IT leadership, our founders, Amy and Shawn, bring deep expertise and a shared passion for technology</div>  
      </div>
      <div class="flex-3">
        <div class="slideshow-container">
          <div class={`slideshow-item slideshow-fade lg:animate-none ${activeSlide === 1 ? 'slide-active' : ''}`}>
            <div class="bg-slate-500 w-full aspect-[1/1] mb-3 lg:mb-6 max-w-md mx-auto"></div>
            <div class="txt-subheadline font-bold text-center lg:text-left">Shawn LoPresto</div>
            <div class="text-center lg:text-left">As a seasoned DevOps architect and site reliability expert, Shawn's career includes leadership roles at KnowBe4 and Malwarebytes, where he directed teams to deliver resilient and scalable cloud platforms.</div>
          </div>
          <div class={`slideshow-item slideshow-fade lg:animate-none ${activeSlide === 2 ? 'slide-active' : ''}`}>
            <div class="bg-slate-500 w-full aspect-[1/1] mb-3 lg:mb-6 max-w-md mx-auto"></div>
            <div class="txt-subheadline font-bold text-center lg:text-left">Amy Satterlee</div>
            <div class="text-center lg:text-left">Amy is a multi-talented software engineer with an expertise in full-stack software development. She has consistently delivered top-notch frontend and backend solutions for major companies like KnowBe4 and Malwarebytes.</div>
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
        </div>
      </div>
    </div>
  </div>
</div>