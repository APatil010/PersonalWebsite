<template>
    <div class="homeGrid">
        <div class="headerText">
            <p class="mono-light font-40">Hello...</p>
            <p class="mono-light font-28">I am <strong>Aarsh Patil.</strong></p>
            <p class="mono-light font-16">Full Stack Software Developer</p>
        </div>
        <div class="quoteText font-20 mono-light">
            <blockquote>
                <strong class="font-28">"</strong> To create something that is genuinely new, you have to start again.
                And i think with great intent, you disconnect from the past. <strong class="font-28">"</strong>
                <br />
                —Jony Ive
            </blockquote>
        </div>
    </div>
</template>

<style scoped>
  .homeGrid {
      display: grid;
      min-height: 100vh;
      grid-template-columns: 1fr 2fr;
      grid-template-rows: 1fr 1fr;
      grid-row-gap: 2em;
  }
  
  .headerText {
      grid-row: 1 / 2;
      grid-column: 1 / 2;
  }
  
  .quoteText {
      text-align: right;
      grid-row: 2 / 3;
      grid-column: 2 / 3;
  }
</style>
