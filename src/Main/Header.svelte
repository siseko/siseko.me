<script lang="ts">
  import Icon from "../Icon.svelte";

  export let onMenuClick;
</script>

<header class="text-center px-2 py-8 bg-secondary text-white">
  <h1 class="uppercase">Siseko Nomavila</h1>
  <div class="bg-primary mx-auto max-w-32 h-0.5" />
  <h2 class="my-4 mb-0">Software Engineer</h2>
  <div class="menu mt-4 lg:hidden">
    <i class="pt-4 cursor-pointer" on:click={onMenuClick}>
      <Icon name="menu" className="fill-white" />
    </i>
  </div>
</header>
