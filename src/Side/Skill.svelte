<script lang="ts">
  import Icon from '../Icon.svelte';

  export let icon: string;
  export let name: string;
</script>

<style>
  li :global(svg) {
    width: 20px;
    height: 20px;
    fill: white;
  }
</style>

<li class="bg-secondary text-white rounded-sm py-1 px-2 mb-1 ml-1 text-[0.8rem] flex items-center gap-1">
  <Icon name={icon} className="fill-white" />
  <span> {name} </span>
</li>
