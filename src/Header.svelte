<script lang="ts">
  import Icon from "./Icon.svelte";

  export let onMenuClick;
</script>

<header
  class="text--center padding--sm padding-v--xlg bg--secondary text--white">
  <h1 class="text--uppercase">Siseko Nomavila</h1>
  <div class="hr margin--auto" />
  <h2 class="margin-v--md margin-b--none">Software Engineer</h2>
  <div class="menu margin-t--md">
    <i class="padding-t--md" on:click={onMenuClick}>
      <Icon name="menu" className="fill--white" />
    </i>
  </div>
</header>
