<script lang="ts">
	let showModal = false;
	let modalImage = "";
	let modalTitle = "";


	import ywm from '$lib/images/ywmView.png';
	import BBG from '$lib/images/BB.png';
	import Arcsys from '$lib/images/arcsysView.png';
	import SMXbot from '$lib/images/SMXbot.png';
	import NTB from '$lib/images/NTB.png';

	const items = [
  {
    logo: ywm,
    title: 'You We Movie',
    description: 'A movie blog platform developed using ASP.NET Core and Razor Pages. It allows users to browse, review, and rate movies.',
  },
  {
    logo: BBG,
    title: 'Blue Ball Game',
    description: 'An in-development 2D platformer built in Godot Engine. Inspired by classic 16-bit titles, it features hand-crafted pixel art, multiple levels, and directional attack animations. Where I handle all development from design to mechanics.',
  },
  {
    logo: Arcsys,
    title: 'Arcsys',
    description: 'A tournament automation system for StepManiaX, built with .NET and React. It manages bracket creation, score tracking, and player scheduling. In addition to this a ranking algorithm was developed with the help of the data mining method CRISP-DM.',
  },
  {
    logo: SMXbot,
    title: 'SMX Weekly Bot',
    description: 'A Discord bot written in Python that fetches and posts weekly challenge data for StepManiaX players. I built a scraper, integrated with Discord’s API, and set up scheduled tasks for automatic updates.',
  },
  {
    logo: NTB,
    title: 'New Times Burger',
    description: 'A responsive restaurant website developed in PHP with a MySQL database. It includes a dynamic menu, reservation system, and admin dashboard for managing content.',
  },
];

</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
	<h1>Projects</h1>

	<div class="py-6 sm:py-8 lg:py-16">
		<div class="mx-auto">
		  <!-- text - start -->
		  <div class="mb-10 md:mb-16">
			<p class="mx-auto text-center text-(--color-theme-1) md:text-lg">
			  This is a showcase of a few selected projects, presented with brief summaries and highlights.
			</p>
		  </div>
		  <!-- text - end -->
	  
		  <div class="grid gap-12">
			{#each items as item, i}
			  <div class="flex flex-col md:flex-row items-center gap-15"
				class:md:flex-row-reverse={i % 2 !== 0}>
				
				<div on:click={() => { showModal = true; modalImage = item.logo; modalTitle = item.title; }} class="group cursor-pointer">
					<div class="relative h-56 w-full md:h-48 md:w-72 overflow-hidden rounded-lg bg-gray-100 shadow-lg border-4 border-sky-400">

						<img src={item.logo} alt={item.title} class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-105" />
					</div>
				</div>
		  
				<div class="flex flex-col gap-2 max-w-2xl">
				  <h1 class="text-center text-3xl font-bold text-gray-800 sm:text-3xl md:mb-6 md:text-left text-transparent bg-clip-text bg-gradient-to-r to-emerald-600 from-sky-400">{item.title}</h1>
				  <p class="text-(--color-theme-1)">{item.description}</p>
				</div>
			  </div>
			{/each}
		  </div>
		  
		</div>
	  </div>
	  
	  {#if showModal}
	  <div
		class="fixed inset-0 z-50 flex items-center justify-center bg-black bg-opacity-75"
		on:click={() => (showModal = false)}
	  >
		<div
		  class="relative max-w-3xl w-full p-4"
		  on:click|stopPropagation
		>
		  <img src={modalImage} alt={modalTitle} class="w-full h-auto rounded shadow-lg" />
		  <button
			class="absolute top-2 right-2 text-white text-3xl leading-none hover:text-gray-300"
			on:click={() => (showModal = false)}
		  >
			&times;
		  </button>
		</div>
	  </div>
	{/if}
</div>