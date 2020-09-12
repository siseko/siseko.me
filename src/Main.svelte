<script lang="ts">
  import Header from "./Header.svelte";
  export let onMenuClick;
</script>

<section class="main">
  <Header {onMenuClick} />
</section>
