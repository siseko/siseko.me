<script lang="ts">
  import axios from "axios";

  export let className: string;
  export let name: string;
  let svg: string = "";

  function fetchtIcon() {
    if (!name) {
      return;
    }

    axios
      .get(`https://res.cloudinary.com/vw/image/upload/icons/${name}.svg`)
      .then((res) => {
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
</script>

{@html svg}
