<script lang="ts">
  import axios from "axios";

  export let className: string;
  export let name: string;
  let svg: string;

  axios
    .get(`https://res.cloudinary.com/vw/image/upload/icons/${name}.svg`)
    .then((res) => (svg = res.data));
</script>

<span class={className} >
  {@html svg}
</span>
