<script lang="ts">
  export let job;
</script>

<div class="padding-b--xlg">
  <div class="text--uppercase text--lg">{job.title}</div>
  <span class="text--sm">{job.company} | {job.timePeriod}</span>
  <div class="padding-t--sm"><a class="text--sm text--link" href={job.website} target="_blank">{job.website}</a></div>
  <div class="text--thin padding-t--md">
    <p>{job.summary}</p>
    <span class="text--regular">Responsibilities</span>
    <ol class="padding-v--sm">
      {#each job.responsibilities as text}
        <li>{text}</li>
      {/each}
    </ol>
    <span class="text--regular">
      Tech used: {#each job.tech as tech, i}
        <span class="text--thin">
          {tech}{#if i !== job.tech.length - 1},{/if}
        </span>
      {/each}
    </span>
  </div>
</div>
