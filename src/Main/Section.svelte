<script lang="ts">
  export let title: string;
</script>

<h2 class="uppercase font-thin text-center bg-tertiary py-4 mt-5">
  {title}
</h2>
<div class="p-2">
  <slot />
</div>
