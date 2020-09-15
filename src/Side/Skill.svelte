<script lang="ts">
  import Icon from '../Icon.svelte';
  
  export let icon: string;
  export let name: string;
</script>

<li>
  <Icon name={icon} className="v-align--middle" />
  <span class="v-align--middle"> {name} </span>
</li>