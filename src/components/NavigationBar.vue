<template>
    <div class="NavigationBar">
        <div class="Navigation">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/about">About</RouterLink>
            <RouterLink to="/projects">Projects</RouterLink>
            <RouterLink to="/contact">Contact</RouterLink>
            <RouterLink to="/faqs">FAQ's</RouterLink>
        </div>
        <hr />
    </div>
</template>

<style scoped>
  .NavigationBar {
      display: grid;
      padding: 1em 0;
      grid-template-columns: 1fr;

      & .Navigation {
          justify-self: end;
      }

      & a, & a:active, & a:hover, & a:link {
          padding: 0 1em;
          text-decoration: none;
          color: black;
      }

      & hr {
          width: 100%;
          margin: 2em 0;
      }
  }
</style>