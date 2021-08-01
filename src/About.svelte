<script>
	const details = {
    name: "Yonah Aviv",
    headline: "Student at TanenbaumCHAT, Coding Tutor, Computer Programmer",
    summary:
      "I am a high school student who actively studies various STEM topics, mainly web development(web extensions, progressive web apps) and computer science. I teach coding to children as a self-employed tutor, and I work on various self initiated coding/tech projects in my own time. Technologies I use on a day-to-day basis include Python, JavaScript, Svelte(web-dev), Node.js, Git, and a little bit of React.",
  };
</script>

<section>
	<!--Name-->
	<h1>{details.name}</h1>
	<!--Headline-->
	<h2>
	  {details.headline}
	</h2>
	<br />
	  <div class="summary">
		<b>
		  <!--About me-->
		  <hr />
		</b>
		<p>
		  {details.summary}
		</p>
	</div>
</section>

<style>
	/* your styles go here */
</style>

<!-- markup (zero or more items) goes here -->