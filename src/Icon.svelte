<script lang="ts">
  import axios from "axios";

  export let className: string;
  export let name: string;
  let svg: string = "";

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
</script>

{@html svg}
