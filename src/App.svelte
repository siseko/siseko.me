<script lang="ts">
  import Main from "./Main.svelte";
  import Side from "./Side/Side.svelte";

  let hideSide;

  let onMenuClick = function () {
    hideSide = !hideSide;
  };
  let onSideHide = function () {
    hideSide = true;
  };
</script>

<style type="text/scss" global>
  @import "./styles/index.scss";
</style>

<main class="display--flex">
  <Side hide={hideSide} {onSideHide} />
  <Main {onMenuClick} />
</main>
