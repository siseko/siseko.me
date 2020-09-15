<script lang="ts">
  export let title: string;
  export let company: string;
  export let timePeriod: string;
</script>

<div class="padding-b--xlg">
  <div class="text--uppercase text--lg">{title}</div>
  <span class="text--sm">{company} | {timePeriod}</span>
  <slot />
</div>
