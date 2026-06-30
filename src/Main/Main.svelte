<script lang="ts">
  import Header from "./Header.svelte";
  import Job from "./Job.svelte";
  import Section from "./Section.svelte";

  export let onMenuClick;

  const jobs = [
    {
      title: "Senior Frontend Developer",
      company: "BMW Group",
      website: "",
      timePeriod: "September 2023 - Present",
      summary: `As a Senior Frontend Developer within BMW's dealer solutions team, I am responsible for developing and maintaining a vehicle handover platform that streamlines the customer delivery process for BMW dealerships across multiple markets. My primary focus is on delivering a robust, scalable solution that ensures all critical checks are completed before vehicle handover while enhancing the overall customer experience.`,
      responsibilities: [
        `Develop and maintain the platform, ensuring optimal performance and UX across desktop and mobile interfaces. The platform manages financial verification, vehicle fault checks, sanctions screening, contract preparation, BMW app account setup, dealer checklists, accessories upselling, and fleet handovers`,
        `Implement comprehensive observability solutions using CloudWatch for backend logging and alarms, while leading the implementation of frontend observability to address UX blind spots`,
        `Develop automation tools and quality-of-life improvements including Microsoft Teams deployment notifications, automated Jira story updates with deployment environment tags, and GitHub PR-to-Jira story linking`,
        `Design and build CI/CD pipelines that are currently implemented across 8 projects, ensuring consistent deployment workflows and reliable delivery across the entire ecosystem`,
      ],
      tech: [
        `Angular 19`,
        `TypeScript`,
        `Signals`,
        `Tailwind CSS`,
        `AWS`,
        `CloudWatch`,
        `Microsoft Teams API`,
        `Jira API`,
        `GitHub API`,
      ],
    },
    {
      title: "Frontend Developer",
      company: "Osiris Trading",
      website: "",
      timePeriod: "July 2019 - August 2023",
      summary: `I built and maintained web applications for Betway's growing list of
        markets across the globe. My main focus was the frontend component
        library. Betway had been aggressively expanding its business into
        more markets, and the library helped maintain consistency across the
        brand and provided a repeatable process for building
        web applications.`,
      responsibilities: [
        `Built web applications for Betway Mozambique and Betway Bulgaria`,
        `Added onto and fine-tuned the NPM components library`,
        `Managed CI/CD on Azure DevOps`,
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

<section class="flex-1">
  <Header {onMenuClick} />
  <div class="p-8 md:p-16">
    <Section title="About">
      <p class="font-thin">
        A seasoned engineer with over twelve years of experience building
        transactional systems in regulated industries — environments where
        accuracy, compliance, and reliability aren't optional. From processing
        30,000 rental transactions per minute at DStv BoxOffice, to launching
        Standard Bank's Online Banking for Business, to now ensuring sanctions and
        compliance checks are completed before every BMW vehicle handover.
      </p>
      <p class="font-thin">
        I care deeply about domain knowledge. The systems I build serve
        real-world outcomes — compliance requirements being met, tax obligations
        being reported — and I treat understanding those
        outcomes as core to my job, not background noise. This is what drives my
        approach to engineering: start from the problem, work backwards into the
        solution.
      </p>
      <p class="font-thin">
        Beyond hands-on development, I have built reusable component libraries
        for Angular projects and led full project implementations from
        requirements analysis and technical feasibility through to delivery. I
        have managed entire software projects independently, including
        infrastructure setup on AWS and variants and deployment workflow
        optimization, ensuring projects are delivered on time and to
        specification.
      </p>
    </Section>
    <Section title="Experience">
      {#each jobs as job}
        <Job {job} />
      {/each}
    </Section>
    <!-- <Section title="Personal Projects">
      {#each personal as job}
        <Job {job} />
      {/each}
    </Section> -->
  </div>
</section>
