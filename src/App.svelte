<script>
  // UI Components
  import Icon from "@iconify/svelte"
  import { Tabs, Tab, TabList, TabPanel } from "svelte-tabs";
  // Components
  import Skills from "./Skills.svelte";
  import RecentProjects from "./RecentProjects.svelte";
import About from "./About.svelte";

  // Variables
  let rand = -1;
  // Functions
  function getRand() {
    fetch("./rand")
      .then((d) => d.text())
      .then((d) => (rand = d));
  }
  // Component Parameters
  export let name;
</script>

<!-- <h1>Your number is {rand}!</h1>
<button on:click={getRand}>Get a random number</button>
<main>
  <h1>Heeeeello {name}!</h1>
  <p>
    Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn
    how to build Svelte apps.
  </p>
</main> -->
<Tabs>
  <TabList>
    <b>Yonah Aviv</b>
    <Tab>About</Tab>
    <Tab>Projects</Tab>
    <Tab>Resume</Tab>
    <a href="https://github.com/y330" title="My GitHub"><Icon icon="tabler:brand-github" /></a>
  </TabList>

  <TabPanel>
    <About/>
    <Skills />
    <RecentProjects />
  </TabPanel>

  <TabPanel>
    <h2>Projects</h2>
  </TabPanel>

  <TabPanel>
    <h2>Resume</h2>
  </TabPanel>
</Tabs>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #312fff;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
