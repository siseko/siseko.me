<script lang="ts">
  export let name: string;
</script>

<style type="text/scss" global>
  @import "village-components/dist/index.css";
  @import "village-components/dist/breakpoints.scss";
  
  @import "./styles/index.scss";

</style>

<main>
  <h1>Hello {name}!</h1>
  <p class="padding--sm">
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</main>
