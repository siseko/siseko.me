<script lang="ts">
  import Header from "./Header.svelte";
  import Job from "./Job.svelte";
  import Section from "./Section.svelte";

  export let onMenuClick;

  const jobs = [
    {
      title: "Frontend Developer",
      company: "Osiris Trading",
      website: "",
      timePeriod: "July 2019 - Current",
      summary: `I build and maintain web applications for Betway's growing list of
            markets across the globe. My main focus is the frontend component
            library. Betway has been aggressively expanding its business into
            more markets, the library helps maintain consistency across the
            brand and provides a repeatable process for building
            web applications.`,
      responsibilities: [
        `Build the web applications for Betway Mozambique and Betway Bulgaria`,
        `Add onto and fine-tune the NPM components library`,
        `Manage CI/CD on Azure DevOps`,
      ],
      tech: [`Angular`, `Typescript`, `SASS`, `Azure DevOps`],
    },
    {
      title: "Software Developer",
      company: "PSG Wealth",
      website: "",
      timePeriod: "October 2018 - April 2019",
      summary: `My role was to provide a solution to the manual process of third party 
            tax submissions to the South Africa Revenue Services. This would help to 
            save the business time and put power back in the hands of the tax managers. As a financial 
            services provider the business is obliged to provide their clients' transaction data 
            for every tax year. The business offers varying products from offshore equities, 
            retirement investement products and pension funds and the different requirements 
            for each of these needed to be catered for.`,
      responsibilities: [
        `Process and categorize transactions in the millions for the different product types`,
        `Move tax business rules contained in stored procedures to the code`,
        `Deploy docker services onto Azure Kubernetes Service`,
        `Provide guidance and mentorship to juniors in the team`,
      ],
      tech: [`.NET Core 2`, `Angular`, `Docker`, `Azure DevOps`],
    },
    {
      title: "Software Developer",
      company: "Absa Bank",
      website: "",
      timePeriod: "March 2018 - October 2018",
      summary: `I was mainly responsible for rewriting the backend services supporting the bank's rest of Africa 
            online banking platforms. With the bank's split from its then biggest shareholder, Barclays PLC, came a few rewrites and platform migrations. 
            To support this, I successfully migrated applications from Barclay's infrastructure onto Absa's infrastructure.`,
      responsibilities: [
        `Integrate with downstream SOAP services and expose RESTful services for frontend consumption`,
        `Dockerize and deploy newly written services onto OpenShift`,
        `Migrate existing applications onto RHEL 7`,
      ],
      tech: [`Spring Boot`, `Angular`, `Docker`, `OpenShift`],
    },
    {
      title: "Software Engineer",
      company: "Entelect",
      website: "",
      timePeriod: "February 2016 - February 2018",
      summary: `During my tenure at Entelect I worked for their biggest client, Standard Bank. 
            I worked on their Online Banking for Business product, joining at an early stage to 
            build most of the core functionality and implement role based access control across 
            the entire online banking product.
      `,
      responsibilities: [
        `Roll out a beta version of the platform to thirty thousand pre-selected customers`,
        `Implement role based access control to restrict system access by business employees`,
        `Run code critique sessions to ensure quality in the code base`,
        `I kicked off the tough process of upgrading from AngularJS to Angular 2`,
      ],
      tech: [`Java`, `AngularJS`, `Angular`, `Cucumber`],
    },
    {
      title: "Software Developer",
      company: "DStv Digital Media",
      website: "",
      timePeriod: "January 2014 - January 2016",
      summary: `I played a key role in the success of DStv BoxOffice in Africa. 
            In the time I was there we rolled out to 12 African countries, migrated South Africa 
            to a new platform and drastically reduced rental failure rates. I resolved issues with
            concurrency and performance and led the team for months when we had no Seniors.
      `,
      responsibilities: [
        `Build a reliable and perfomant application that caters for up to 30 thousand transactions per minute`,
        `Create ETL jobs to migrate the data of more than a million customers`,
        `Built a graphing application for the business to track rental statistics`,
        `Set up a dashboard to help customer service resolve customer issues quicker`,
      ],
      tech: [`Java`, `Spring`, `ActiveMQ`, `Node.js`],
    },
  ];

  const personal = [
    {
      title: "",
      company: "Village Web",
      timePeriod: "July 2018 - Current",
      website: "https://www.villageweb.co.za",
      summary: `Village Web seeks to bring back the sense of community that has always been at the 
            core of most African cultures. Targeted at residents in living estates, the project encourages 
            the sharing of resources amongst residents therefore allowing them to cut down on living expenses. 
            Leveraging off the network of residents around you, you can share your satellite TV costs, 
            WiFi costs, share your ride, find a tennis buddy, find a professional and many more.`,
      responsibilities: [
        `I take care of the entire tech stack from setting up the infrastructure all the way to the UI and UX`,
        `Working closely with the Managing Director to ensure his vision for the product is realised through the application`,
      ],
      tech: [
        `React`,
        `Redux`,
        `PostgreSQL`,
        `Spring Boot`,
        `Docker`,
        `Cypress`,
        `Nginx`,
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
        <Job {job} />
      {/each}
    </Section>
    <Section title="Personal Projects">
      {#each personal as job}
        <Job {job} />
      {/each}
    </Section>
  </div>
</section>
