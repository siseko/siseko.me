<script lang="ts">
  import Main from "./Main/Main.svelte";
  import Side from "./Side/Side.svelte";

  let gtag: any;

  let hideSide;

  let onMenuClick = function () {
    gtag && gtag("event", "click", {
      event_category: "sidenav",
      event_label: "open sidenav",
      value: "open",
    });
    hideSide = !hideSide;
  };
  let onSideHide = function () {
    hideSide = true;
  };

  let closeSide = function () {
    hideSide = true;
  };
</script>

<style type="text/scss" global>
  @import "./styles/index.scss";
</style>

<main class="display--flex">
  <Side hide={hideSide} {onSideHide} />
  <Main {onMenuClick} />
  {#if !hideSide && window.innerWidth < 1024}
    <div class="side-overlay" on:click={closeSide} />
  {/if}
</main>
