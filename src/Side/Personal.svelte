<script>
  import Icon from "../Icon.svelte";
</script>

<div class="mt-8 font-thin py-2">
  <h3 class="uppercase my-4 pb-[10px] border-b border-secondary">Personal Information</h3>
  <ul class="py-2">
    <li>
      <Icon name="location" className="fill-secondary inline-block align-middle" />
      <span class="pl-2">Johannesburg, South Africa</span>
    </li>
    <li>
      <Icon name="envelope" className="fill-secondary inline-block align-middle" />
      <a
        class="pl-2"
        href="mailto:siseko@monacodev.co"
        target="_blank">siseko@monacodev.co</a>
    </li>
    <li>
      <Icon name="phone" className="fill-secondary inline-block align-middle" />
      <span class="pl-2">+27... request by email</span>
    </li>
  </ul>
</div>
