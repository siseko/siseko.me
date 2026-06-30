<script lang="ts">
  import axios from "axios";
  import { onDestroy } from "svelte";

  export let className: string;
  export let name: string;
  let svg: string = "";
  let alive = true;

  function fetchtIcon() {
    if (!name) {
      return;
    }

    axios
      .get(`https://res.cloudinary.com/vw/image/upload/icons/${name}.svg`)
      .then((res) => {
        if (!alive) return;

        svg = res.data;

        if (className) {
          const template = document.createElement("template");
          template.innerHTML = res.data;

          const el = template.content.firstElementChild;
          el?.classList.add(
            ...(className?.split(" ").filter((c: string) => !!c) || [])
          );

          svg = el?.outerHTML || "";
        }
      });
  }

  fetchtIcon();

  onDestroy(() => {
    alive = false;
  });
</script>

{@html svg}
