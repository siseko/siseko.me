<script lang="ts">
  import Icon from "../Icon.svelte";
  import Personal from "./Personal.svelte";
  import Education from "./Education.svelte";
  import Expertise from "./Expertise.svelte";

  export let hide: boolean;
  export let onSideHide: () => void;

  if (window.innerWidth < 1024) {
    onSideHide();
  }
</script>


<section
  class="side bg-tertiary p-5 max-w-xs absolute z-[1] lg:relative"
  class:hidden={hide}>
  <div class="text-right cursor-pointer lg:hidden" on:click={() => onSideHide()}>
    <Icon name="cross" />
  </div>
  <img
    src="https://res.cloudinary.com/vw/image/upload/v1599915557/siseko/dc138e8a-dc25-4805-9d5e-3f947f5043c0.jpg"
    alt="Siseko Nomavila"
    class="rounded-full h-[250px] w-[250px] block mx-auto" />
  <Personal />
  <Education />
  <Expertise />
</section>
