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

<div class="text--thin margin-t--xlg">
  <h3 class="text--uppercase border--b">Expertise</h3>
  <h4 class="margin-b--sm text--regular">Core Competencies</h4>
  <ul class="grid skills">
    {#each skills[0] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-b--sm text--regular padding-t--sm">Frontend Development</h4>
  <ul class="grid skills">
    {#each skills[1] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="grid skills padding-t--sm">
    {#each skills[2] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">Backend Development</h4>
  <ul class="grid skills">
    {#each skills[3] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <ul class="grid skills padding-t--sm">
    {#each skills[4] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">Databases</h4>
  <ul class="grid skills">
    {#each skills[5] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">DevOps</h4>
  <ul class="grid skills">
    {#each skills[6] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">Monitoring</h4>
  <ul class="grid skills">
    {#each skills[7] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <h4 class="margin-v--sm text--regular">APIs</h4>
  <ul class="grid skills">
    {#each skills[8] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul>
  <!-- <h4 class="margin-v--sm text--regular">Testing</h4>
  <ul class="grid skills">
    {#each skills[9] as skill}
      <Skill icon={skill.icon} name={skill.name} />
    {/each}
  </ul> -->
</div>
