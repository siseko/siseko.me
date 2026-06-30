<script>
  import Icon from "../Icon.svelte";
  import Skill from "./Skill.svelte";

  let skills = [
    [
      { icon: "", name: "Full-stack architecture" },
      { icon: "", name: "Component library design" },
      { icon: "", name: "Log analysis and alerting" },
      { icon: "", name: "e2e testing" },
      { icon: "", name: "Test automation" },
      { icon: "", name: "Technical leadership" },
      { icon: "", name: "Mentoring" },
      { icon: "", name: "Workflow automation" },
      { icon: "", name: "Tooling" },
      { icon: "", name: "Cloud infra" },
      { icon: "", name: "CI/CD pipelines" },
      { icon: "", name: "Environment management" },
    ],
    [
      { icon: "javascript", name: "JavaScript" },
      { icon: "", name: "TypeScript" },
    ],
    [
      { icon: "angular", name: "Angular" },
      { icon: "react", name: "React" },
      { icon: "", name: "Tailwind" },
      { icon: "", name: "RxJS" },
    ],
    [
      { icon: "", name: "Java" },
      { icon: "nodejs", name: "Node.js" },
    ],
    [
      { icon: "", name: "Spring" },
      { icon: "", name: "NestJS" },
      { icon: "", name: "Express" },
    ],
    [
      { icon: "", name: "PostgreSQL" },
      { icon: "", name: "MySQL" },
      { icon: "", name: "MSSQL" },
    ],
    [
      { icon: "", name: "AWS" },
      { icon: "", name: "Fly.io" },
      { icon: "", name: "Docker" },
      { icon: "", name: "Kubernetes" },
      { icon: "", name: "Github Actions" },
      { icon: "", name: "Cloudwatch" },
      { icon: "", name: "Datadog" },
      { icon: "", name: "Terraform" },
    ],
    [
      { icon: "", name: "Cloudwatch" },
      { icon: "", name: "Datadog" },
    ],
    [
      { icon: "", name: "Microsoft Teams" },
      { icon: "", name: "GitHub" },
      { icon: "", name: "Jira" },
    ],
    [{ icon: "", name: "Jest" }],
  ];
</script>

<div class="font-thin mt-8">
  <h3 class="uppercase pb-[10px] border-b border-secondary">Expertise</h3>
  <h4 class="mb-2 font-normal">Core Competencies</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[0] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">Frontend Development</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[1] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="flex flex-wrap pt-2">
    {#each skills[2] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">Backend Development</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[3] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="flex flex-wrap pt-2">
    {#each skills[4] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">Databases</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[5] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">DevOps</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[6] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">Monitoring</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[7] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="my-2 font-normal">APIs</h4>
  <ul class="flex flex-wrap items-start">
    {#each skills[8] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
</div>
