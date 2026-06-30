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
      timePeriod: "July 2024 - Present",
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
      company: "Absa",
      website: "",
      timePeriod: "July 2022 - June 2024",
      summary: `As a Digital FX Developer within the Digital Foreign Exchange department at Absa, I was responsible for developing and enhancing specialized FX trading products tailored for large multinational clients, particularly in Africa. My primary focus was on delivering robust, scalable, and efficient solutions that facilitated critical aspects of foreign exchange trading and analytics.`,
      responsibilities: [
        `Developed and maintained trading applications for both desktop and web, ensuring they delivered a seamless, secure, and responsive user experience. This included handling trading activities, sourcing FX rates, and managing quoting processes`,
        `Built and continuously improved dashboards using Grafana that provided essential insights into business performance metrics. This helped facilitate better decision-making and performance tracking`,
        `Worked closely with product development to implement new features, oversaw testing phases to ensure product reliability, and addressed issues during the deployment phase`,
      ],
      tech: [`Angular`, `Typescript`, `Grafana`, `Azure DevOps`],
    },
    {
      title: "Frontend Developer",
      company: "Osiris Trading",
      website: "",
      timePeriod: "July 2019 - June 2022",
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

<section class="main">
  <Header {onMenuClick} />
  <div class="content">
    <Section title="About">
      <p class="text--thin">
        A seasoned engineer with a career spanning over twelve years working
        with South Africa's biggest companies across financial services, media,
        and automotive industries. Currently building a comprehensive vehicle
        handover platform for BMW dealerships that streamlines the customer
        delivery process through automated checks and workflow management.
      </p>
      <p class="text--thin">
        I have varied experience having helped deal with performance and
        concurrency issues at DStv's BoxOffice, then having been one of the
        initial developers to help launch Standard Bank's Online Banking For
        Business, and now developing solutions that enhance the automotive
        customer experience at BMW. My skills cut across multiple stacks, and my
        passion for solving problems combined with big picture thinking means I
        have worked on frontend development, various backends, with different
        operating systems and even delved into the DevOps side of things.
      </p>
      <p class="text--thin">
        Beyond hands-on development, I have built reusable component libraries
        for Angular projects and spearheaded full project implementations from
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
