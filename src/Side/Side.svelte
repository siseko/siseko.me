<script lang="ts">
  import Icon from "../Icon.svelte";
  import Personal from "./Personal.svelte";
  import Education from "./Education.svelte";

  export let hide: boolean;
  export let onSideHide: () => void;

  if (window.innerWidth < 1024) {
    onSideHide();
  }
</script>

<section class="side bg--tertiary padding--lg" class:display--none={hide}>
  <div class="text--right close" on:click={() => onSideHide()}>
    <Icon name="cross" />
  </div>
  <img
    src="https://res.cloudinary.com/vw/image/upload/v1599915557/siseko/dc138e8a-dc25-4805-9d5e-3f947f5043c0.jpg"
    alt="Siseko Nomavila"
    class="border-rad--50 profile-image display--block margin--auto" />
  <Personal />
  <Education />
</section>
