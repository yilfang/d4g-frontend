<script>
  import SectionTitle from "../../lib/components/section_title.svelte";
  import TeamCard from "../../lib/components/team_card.svelte";
  import AlumniCard from "../../lib/components/alumni_card.svelte";
  import SzymonProfile from "$lib/assets/profile-pics/szymon_sarnowicz.png";
  import SaraProfile from "$lib/assets/profile-pics/sara_haptonstall.png";
  import SudhaProfile from "$lib/assets/profile-pics/sudha_kannan.png";
  import ReedProfile from "$lib/assets/profile-pics/reed_paskvan.png"
  import YilinProfile from "$lib/assets/profile-pics/yilin_fang.jpeg"
  import Navbar from "$lib/components/navbar.svelte";

  const currentPage = "team";

  const execTeam = [
    {
      name: "Edward G. Happ",
      position: "Executive Fellow Emeritus",
      description:
        "Edward G. Happ is an Executive Fellow at the University of Michigan School of Information, where he is teaching and conducting research. His 40 years of professional experience include all facets of managing information services and high technology businesses, including general management with P&L responsibility, operations, product management, sales, marketing, customer service, human resources management, technical consulting, manufacturing, and both software and hardware development.",
      image:
        "https://pbs.twimg.com/profile_images/1653043667211370496/tsXMk4do_400x400.jpg",
      linkedin: "https://www.linkedin.com/in/edward-g-happ/",
    },
    {
      name: "Sara Haptonstall",
      position: "Project Manager",
      description:
        "Sara is a graduate of the Master's  in Applied Data Science program from the University of Michigan. She holds a Bachelor's degree in  Accounting. Sara has extensive experience in using analytical tools to enhance business operations and decision-making, optimizing productivity and reducing costs through innovative automation and data analytics solutions.  Her technical skills include advanced proficiency in Python, SQL, and various AI & machine learning frameworks.",
      image: SaraProfile,
      linkedin: "https://www.linkedin.com/in/sarahaptonstall/",
    },
  ];

  const dataTeam = [
    {
      name: "Sidra Effendi",
      position: "Consultant and Data Scientist",
      description:
        "Sidra is a Master's student at the University of Michigan School of Information, specializing in Data Science. She has an undergraduate degree in Computer Engineering. She has previously worked as an Edge Hacker for Zenatix Solutions and also co-founded a company called Pixli, where she worked on Software Development, UX/UI and Marketing.",
      image: "https://avatars.githubusercontent.com/u/5307694?v=4",
      linkedin: "https://www.linkedin.com/in/sidraeffendi/",
    },
    {
      name: "Sudha Kannan",
      position: "Data Scientist",
      description:
        "Sudharsana graduated with a Master’s in Mobile and Embedded Systems from the University of Passau, Germany, and holds a Bachelor’s degree in Information and Communication Technology. She has professional experience in Data Science, having worked for a consulting company, and has also been an academic researcher at the university in the field of Data Science. Additionally, Sudha has experience in Information Technology, having worked for Amazon and Tata Communications Limited in the IT sector.",
      image: SudhaProfile,
      linkedin: "http://www.linkedin.com/in/sudharsanakannan/",
    },
    {
      name: "Xabier Urruchua",
      position: "Systems Specialist",
      description:
        "TBA",
    },
    {
      name: "Reed Paskvan",
      position: "Data Scientist",
      description:
        "TBA",
      image: ReedProfile
    },
    {
      name: "Sihyun Kyung",
      position: "Data Scientist",
      description:
        "TBA",
    }
    // {
    //   name: "Hina Joshua",
    //   position: "Data Scientist",
    //   description:
    //     "Hina is a master's student at the University of Michigan School of Information, Master of Applied Data Science Program. She has a Master of Public Health degree from Michigan State University and has previously worked in the public health domain in government and corporate settings where she analyzed health data including state disease surveillance system data and medical insurance claims data for ad hoc and routine report compilation. Hina is interested in the application of NLP in the NGO domain to improve decision-making in development and relief programs.",
    //   image:
    //     "https://media.licdn.com/dms/image/C4E03AQHSs935QuzMhw/profile-displayphoto-shrink_800_800/0/1649256757363?e=2147483647&v=beta&t=THtp_Ris8Bt9DdFXiFedB7wxSsaMxqztomO_ZSE3yqU",
    //   linkedin: "https://www.linkedin.com/in/hina-joshua-63013a10b/",
    // },
    // {
    //   name: "Takao Kakegawa",
    //   position: "Data Scientist",
    //   description:
    //     "Takao is a current Master's student at the University of Michigan School of Information, in the MADS program. He has an undergraduate degree in Applied Mathematics and Statistics, with a computer science specialisation. He has prior experience in statistical analysis research through the SURF Fellowship at UC Berkeley.",
    //   image:
    //     "https://media.licdn.com/dms/image/C5603AQE0TAUWH63lAw/profile-displayphoto-shrink_800_800/0/1552117070041?e=2147483647&v=beta&t=N5xI3dLQoCNVUA_Ui5kMEiaQEKmxsZsgdNR2snJUUwQ",
    //   linkedin: "https://www.linkedin.com/in/takao-kakegawa/",
    // },
  ];

  const webTeam = [
    {
      name: "Yilin Fang",
      position: "Web Developer and UX Designer",
      description:
        "Yilin is a senior dual degree student studying Computer Science and User Experience Design at the University of Michigan. Yilin has 3x project and internship experience with product design and research. She has advanced proficiency working with Python, REST API, SQL JavaScript and other full-stack development tools and languages. She is also interested in learning more about AI, LLMs and ML frameworks. ",
      image:
        YilinProfile,
      linkedin: "https://www.linkedin.com/in/yilin-fang/",
    },
    // {
    //   name: "Prithvijit Dasgupta",
    //   position: "Systems Specialist and Web Developer",
    //   description:
    //     "Prithvijit is a current Master's student in the University of Michigan School of Information aiming to specialize in the Big Data Analytics track. He has experience working on distributed cloud systems and building RESTful APIs. He has an undergraduate degree in Mechanical Engineering.",
    //   image:
    //     "https://pbs.twimg.com/profile_images/1594033657437736971/sL_utrNg_400x400.jpg",
    //   linkedin: "https://www.linkedin.com/in/prithvijit-dasgupta/",
    // },
    // {
    //   name: "Szymon Sarnowicz",
    //   position: "Full Stack Developer",
    //   description:
    //     "Szymon is a current Master's student at the University of Michigan School of Information, in the MADS program. He is currently a Software Engineer at General Motors working on battery diagnostics as well as a previous Program Manager in Autonomous Systems. As a developer he has helped launch Hangul 2.1 which includes all new UI, improved API handling, and feature alerting.",
    //   image: SzymonProfile,
    //   linkedin: "https://www.linkedin.com/in/szymonsarnowicz/",
    // },
  ];

  const alumni = [
    {
      name: "Prithvijit Dasgupta",
      position: "Systems Specialist and Web Developer",
      startYear: 2023,
      endYear: 2024,
      linkedin: "https://www.linkedin.com/in/prithvijit-dasgupta/",
    },
    {
      name: "Szymon Sarnowicz",
      position: "Full Stack Developer",
      startYear: 2023,
      endYear: 2024,
      linkedin: "https://www.linkedin.com/in/szymonsarnowicz/",
    },
    {
      name: "Takao Kakegawa",
      position: "Data Scientist",
      startYear: 2023,
      endYear: 2024,
      linkedin: "https://www.linkedin.com/in/takao-kakegawa/",
    },
    {
      name: "Hina Joshua",
      position: "Data Scientist",
      startYear: 2023,
      endYear: 2024,
      linkedin: "https://www.linkedin.com/in/hina-joshua-63013a10b/",
    },
    {
      name: "Feng-Yu (Leo) Yeh",
      position: "Web Developer and UX Design",
      startYear: 2023,
      endYear: 2024,
      linkedin: "https://www.linkedin.com/in/leoyeh/",
    },
    {
      name: "Kensuke Suzuki",
      position: "Data Consultant",
      startYear: 2021,
      endYear: 2022,
      linkedin: "https://www.linkedin.com/in/kensukesuzuki",
    },
    {
      name: "Anuya Karnik",
      position: "Website Designer",
      startYear: 2021,
      endYear: 2022,
      linkedin: "https://www.linkedin.com/in/anuya-karnik/",
    },
    {
      name: "Harrison Hall",
      position: "Project Manager and Data Scientist",
      startYear: 2021,
      endYear: 2022,
      linkedin: "https://www.linkedin.com/in/harrison-joseph-hall/",
    },
    {
      name: "Mariah Jacobs",
      position: "Web Developer",
      startYear: 2019,
      endYear: 2021,
      linkedin: "https://www.linkedin.com/in/mariah-jacobs/",
    },
    {
      name: "Shivika Bisen",
      position: "Data Scientist",
      startYear: 2020,
      endYear: 2021,
      linkedin: "https://www.linkedin.com/in/shivika-k-bisen/",
    },
    {
      name: "Kevin Lee",
      position: "Data Scientist",
      startYear: 2020,
      endYear: 2021,
      linkedin: "https://www.linkedin.com/in/kevjunlee/",
    },
    {
      name: "Hojoon Kim",
      position: "Project Manager and Data Scientist",
      startYear: 2020,
      endYear: 2021,
      linkedin: "https://www.linkedin.com/in/hojoon-kim-88ba17aa/",
    },
    {
      name: "Cara Canady",
      position: "Data Consultant",
      startYear: 2019,
      endYear: 2020,
      linkedin: "https://www.linkedin.com/in/caracanady/",
    },
    {
      name: "Bryan Romas",
      position: "Data Scientist",
      startYear: 2019,
      endYear: 2020,
      linkedin: "https://www.linkedin.com/in/bryan-romas/",
    },
    {
      name: "Hope Tambala",
      position: "Project Manager",
      startYear: 2019,
      endYear: 2020,
      linkedin: "https://www.linkedin.com/in/hope-tambala/",
    },
    {
      name: "Akio Kakishima",
      position: "Data Scientist",
      startYear: 2019,
      endYear: 2020,
      linkedin: "https://www.linkedin.com/in/akio-kakishima/",
    },
  ];
</script>

<svelte:head>
  <title>Team</title>
</svelte:head>

<Navbar {currentPage} />
<div class="container">
  <div class="cards-container">
    <div class="cards">
      <SectionTitle title="Executive Team" />
      {#each execTeam as member}
        <TeamCard {...member} />
      {/each}
      <SectionTitle title="Data Science Team" />
      {#each dataTeam as member}
        <TeamCard {...member} />
      {/each}
      <SectionTitle title="Web and Systems Team" />
      {#each webTeam as member}
        <TeamCard {...member} />
      {/each}
      <SectionTitle title="Alumni" />
      <div class="alumni-container">
        {#each alumni as member}
          <AlumniCard {...member} />
        {/each}
      </div>
    </div>
  </div>
</div>

<style>
  .container {
    height: 100%;
    display: flex;
    justify-content: center;
    padding: 1%;
  }

  .cards-container {
    width: 70%;
    margin: 0 0 2rem 0;
  }
  
  .alumni-container {
    display: flex;
    gap: 2%;
    flex-flow: row wrap;
    justify-content: space-evenly;
    flex-wrap: wrap;
  }

  @media (max-device-width: 912px) and (min-resolution: 2dppx) {
    .cards-container {
      width: 90%;
    }
  }
</style>
