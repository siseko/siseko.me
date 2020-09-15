<script>
  import Icon from "../Icon.svelte";
  import Skill from "./Skill.svelte";

  let skills = [
    [
      { icon: "javascript", name: "JavaScript" },
      { icon: "", name: "TypeScript" },
      { icon: "html5", name: "HTML 5" },
      { icon: "css3", name: "CSS 3" },
    ],
    [
      { icon: "angular", name: "Angular" },
      { icon: "react", name: "React" },
      { icon: "", name: "Svelte" },
      { icon: "sass", name: "Sass" },
      { icon: "", name: "RxJS" },
    ],
    [
      { icon: "", name: "Java" },
      { icon: "nodejs", name: "Node.js" },
      { icon: "", name: "C#" },
    ],
    [
      { icon: "", name: "Spring" },
      { icon: "", name: ".NET Core" },
      { icon: "", name: "NestJS" },
      { icon: "", name: "Express" },
    ],
  ];
</script>

<div class="text--thin margin-t--xlg">
  <h3 class="text--uppercase border--b">Expertise</h3>
  <h4 class="margin-b--sm text--regular">Frontend Development</h4>
  <ul class="grid skills">
    {#each skills[0] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="grid skills padding-t--sm">
    {#each skills[1] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">Backend Development</h4>
  <ul class="grid skills">
    {#each skills[2] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="grid skills padding-t--sm">
    {#each skills[3] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
</div>
