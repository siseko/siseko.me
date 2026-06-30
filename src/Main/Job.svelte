<script lang="ts">
  export let job;
</script>

<div class="pb-8">
  <div class="uppercase text-xl">{job.title}</div>
  <span class="text-[0.95rem]">{job.company} | {job.timePeriod}</span>
  <div class="pt-2"><a class="text-[0.95rem] cursor-pointer font-medium text-accent link hover:underline" href={job.website} target="_blank">{job.website}</a></div>
  <div class="font-thin pt-4">
    <p>{job.summary}</p>
    <span class="font-normal">Responsibilities</span>
    <ol class="py-2">
      {#each job.responsibilities as text}
        <li>{text}</li>
      {/each}
    </ol>
    {#if job.tech?.length}
    <span class="font-normal">
      Tech used: {#each job.tech as tech, i}
        <span class="font-thin">
          {tech}{#if i !== job.tech.length - 1},{/if}
        </span>
      {/each}
    </span>
    {/if}
  </div>
</div>
