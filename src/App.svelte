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


<main class="flex max-w-[1199px] lg:my-16 lg:mx-auto">
  <Side hide={hideSide} {onSideHide} />
  <Main {onMenuClick} />
  {#if !hideSide && window.innerWidth < 1024}
    <div class="fixed inset-0 bg-[hsla(30,75%,99%,0.75)]" on:click={closeSide} />
  {/if}
</main>
