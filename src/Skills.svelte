<script>
  // UI Components
  import Icon from "@iconify/svelte";
  import Chip, { Set, LeadingIcon, TrailingIcon, Text } from "@smui/chips";
  // Variables
  let clicked = 0;
  let skills = [
    {
      value: "Python",
      label: "py",
      icon: "tabler:brand-python",
      color: "#3877ac",
    },
    {
      value: "JavaScript",
      label: "js",
      icon: "tabler:brand-javascript",
      color: "hsl(53, 92%, 42%)",
    },
    {
      value: "Git",
      label: "git",
      icon: "teenyicons:git-outline",
      color: "#de4c36",
    },
    {
      value: "Natural Language Processing",
      label: "nlp",
      icon: "tabler:file-text",
    },
    {
      value: "ML/AI",
      label: "ml",
      icon: "carbon:machine-learning-model",
      color: "violet",
    },
    {
      value: "Google Cloud Platform",
      label: "gcp",
      icon: "tabler:cloud",
      color: "#4285f4",
    },
    {
      value: "Node.js",
      label: "node",
      icon: "ion:logo-nodejs",
      color: "#539e43",
    },
    {
      value: "Svelte",
      label: "svelte",
      icon: "file-icons:svelte",
      color: "#e84238",
    },
    {
      value: "HTML",
      label: "html",
      icon: "tabler:brand-html5",
      color: "#ea6438",
    },
    { value: "CSS", label: "css", icon: "tabler:brand-css3", color: "#2965f1" },
    {
      value: "Financial Analysis",
      label: "finance",
      icon: "tabler:chart-line",
    },
    { value: "Statistics", label: "stats", icon: "tabler:chart-pie" },
    {
      value: "Pandas",
      label: "pandas",
      icon: "tabler:brand-python",
    },
    { value: "Web Extensions", label: "webext", icon: "tabler:puzzle" },
    { value: "Flask", label: "flask", icon: "tabler:flask", color: "seagreen" },
  ];
</script>

<section>
  <h3>Skills</h3>
  <Set chips={skills} let:chip key={(chip) => chip.label} choice>
    <!-- Note: the `chip` property is required! -->
    <Chip class="tag__" {chip}>
      <Icon icon={chip.icon} style="color:{chip.color}" height="1.2em" />

      <Text>{chip.value}</Text>
    </Chip>
  </Set>

  <pre class="status">Clicked: {clicked}</pre>
<hr/>
</section>

<style>
  /* your styles go here */
</style>
