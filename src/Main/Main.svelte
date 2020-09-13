<script lang="ts">
  import App from "../App.svelte";
  import Header from "./Header.svelte";
  import Job from "./Job.svelte";
  import Section from "./Section.svelte";

  export let onMenuClick;

  const jobs = [
    {
      title: "Frontend Developer",
      company: "Osiris Trading",
      timePeriod: "July 2019 - Current",
      summary: `I build and maintain web applications for Betway's growing list of
            markets across the globe. My main focus is the frontend component
            library. Betway has been aggressively expanding its business into
            more markets, the library helps maintain consistency across the
            brand and provides a consistent and repeatable process for building
            web applications.`,
      responsibilities: [
        `Build the web applications for Betway Mozambique and Betway Bulgaria`,
        `Add onto and fine-tune the NPM components library`,
        `Manage CI/CD on Azure DevOps`,
      ],
    },
    {
      title: "Software Developer",
      company: "PSG Wealth",
      timePeriod: "October 2018 - April 2019",
      summary: `I build and maintain web applications for Betway's growing list of
            markets across the globe. My main focus is the frontend component
            library. Betway has been aggressively expanding its business into
            more markets, the library helps maintain consistency across the
            brand and provides a consistent and repeatable process for building
            web applications.`,
      responsibilities: [
        `Build the web applications for Betway Mozambique and Betway Bulgaria`,
        `Add onto and fine-tune the NPM components library`,
        `Manage CI/CD on Azure DevOps`,
      ],
    },
  ];
</script>

<section class="main">
  <Header {onMenuClick} />
  <div class="content">
    <Section title="About">
      <p class="text--thin">
        A seasoned engineer with a career spanning just under seven years
        working with South Africa’s biggest companies in financial services and
        media. Currently building a library of frontend components to power the
        growing number of online gambling markets for Betway.
      </p>
      <p class="text--thin">
        I have varied experience having helped deal with performance and
        concurrency issues at DStv’s BoxOffice, then having been one of the
        initial developers to help launch Standard Bank’s Online Banking For
        Business. My skills cut across just a single stack, my passion for
        solving problems and my big picture thinking means I have worked on
        frontend, various backends, with different operating systems and even
        delved into the DevOps side of things.
      </p>
    </Section>
    <Section title="Experience">
      {#each jobs as job}
        <Job
          title={job.title}
          company={job.company}
          timePeriod={job.timePeriod}>
          <div class="text--thin padding-t--md">
            <p>{job.summary}</p>
            <span class="text--regular">Responsibilities</span>
            <ol class="padding-v--sm">
              {#each job.responsibilities as text}
                <li>{text}</li>
              {/each}
            </ol>
          </div>
        </Job>
      {/each}
    </Section>
  </div>
</section>
