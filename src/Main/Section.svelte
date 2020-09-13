<script lang="ts">
  export let title: string;
</script>

<h2 class="text--uppercase text--thin text--center bg--tertiary padding-v--md margin-t--lg">
  {title}
</h2>
<div class="padding--sm">
  <slot />
</div>
