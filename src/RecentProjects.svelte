<script>

	import { Accordion, AccordionItem } from 'svelte-collapsible'

	const projects = [
		{
			key: '1',
			img: 'https://picsum.photos/100?random=1',
			title: 'BEAM',
			subtitle: 'Brain scan Enhancer Assistive Model',
			text: 'Mollit consequat aute amet enim consectetur amet aute consectetur reprehenderit laboris. Ipsum reprehenderit minim laborum veniam mollit cillum anim duis. Enim dolor eiusmod consequat incididunt laborum dolore culpa nulla consectetur sit veniam. Eu magna elit et minim ad exercitation id. Sunt anim irure deserunt consectetur est consequat enim magna duis laboris duis. Est officia esse culpa nulla laborum deserunt. Aliqua culpa Lorem amet ipsum culpa ad dolore ullamco occaecat commodo pariatur sint. Excepteur enim est dolor sunt officia anim sunt commodo enim anim'
		},
		{
			key: '2',
			img: 'https://picsum.photos/100?random=2',
			title: 'FragmentQR',
			subtitle: "Link to anywhere on the web with text fragments, and also generate QR codes while your at it",
			text: 'Reprehenderit aliqua aliquip fugiat adipisicing officia. Incididunt qui esse incididunt officia ex fugiat sit exercitation amet cupidatat et. Irure sit reprehenderit amet eu dolor aliquip velit exercitation pariatur. Minim nostrud eiusmod duis sint fugiat tempor aute non. Commodo et Lorem anim est tempor nulla fugiat et pariatur adipisicing elit ex do do dolore. Fugiat anim incididunt minim aliqua dolore aliqua aliquip ut cupidatat id culpa aliqua. Exercitation aliquip Lorem dolore do duis.'
		},
		{
			key: '3',
			img: 'https://picsum.photos/100?random=3',
			title: 'Scanlendar',
			subtitle: "Turn your plain notes into full on calendar events using NLP",
			text: 'Exercitation irure esse excepteur tempor sit aliqua et mollit culpa dolor aliqua id ex. Nostrud veniam sit ea sit ad anim tempor proident aliquip. Exercitation ullamco reprehenderit dolore ut tempor dolore eu amet dolor aliqua ullamco est laboris consequat. Minim minim velit commodo fugiat pariatur. Est ut amet irure cillum in enim laboris in ut amet occaecat ullamco velit. Dolore laborum et Lorem do occaecat et in in consectetur enim et. Cupidatat nisi labore culpa consequat ea. Do ipsum esse elit eiusmod ad non Lorem enim.'
		},
		{
			key: '4',
			img: 'https://picsum.photos/100?random=1',
			title: 'Jesture',
			subtitle: 'Gesture based maps',
			text: 'Irure enim mollit do velit aliqua labore. Ullamco aliquip aliqua reprehenderit fugiat incididunt labore non. Fugiat aute ullamco labore et veniam. Aute cupidatat amet esse duis nostrud excepteur non.'
		},
	]

</script>

<section>
	<h3>Recent Projects</h3>
	<Accordion>
		{ #each projects as item }

			<AccordionItem key={item.key}>

				<div slot='header' class='header'>
					<img src={item.img} alt="Cover"/>
					<div>
						<h2>{ item.title }</h2>
						<p>{ item.subtitle }</p>
					</div>
				</div>

				<p slot='body' class='body'>
					{ item.text }
				</p>

			</AccordionItem>

		{ /each }
	</Accordion>
	<hr/>
</section>

<style>
		:global(.accordion) {
		width: 100%;
		max-width: 450px;
		margin: 0 auto;
	}

	:global(.accordion-item) {
		border-bottom: 1px solid rgb(100, 120, 140);
	}

	.header {
		display: flex;
		align-items: center;
		padding: 0.5em;
	}

	.header > img {
		margin-right: 1em;
		border-radius: 5px;
	}

	.header h2 {
		margin: 0;
		padding: 0;
	}

	.header p {
		font-size: 18px;
		margin: 0;
	}

	.body {
		padding: 0.5em;
		margin: 0;
		font-size: 18px;
	}

</style>