<script lang="ts">
	import ywm from '$lib/images/ywm.png';
	import BBG from '$lib/images/BB.png';
	import Arcsys from '$lib/images/logo.svg';
	import SMXbot from '$lib/images/SMXbot.png';
	import NTB from '$lib/images/NTB.png';
	import { Globe } from 'lucide-svelte';
	

	const items = [
  {
    logo: ywm,
    title: 'You We Movie',
    description: 'A movie blog platform developed using ASP.NET Core and Razor Pages. It allows users to browse, review, and rate movies.',
	link: 'https://github.com/Limorinho/YouWeMovie',
	type: 'repo',
  },
  {
    logo: BBG,
    title: 'Blue Ball Game',
    description: 'An in-development 2D platformer built in Godot Engine. Inspired by classic 16-bit titles, it features hand-crafted pixel art, multiple levels, and directional attack animations. Where I handle all development from design to mechanics.',
	link: 'https://github.com/Limorinho//Blue-Ball-Game',
	type: 'repo',
  },
  {
    logo: Arcsys,
    title: 'Arcsys',
    description: 'A tournament automation system for StepManiaX, built with .NET and React. It manages bracket creation, score tracking, and player scheduling. In addition to this a ranking algorithm was developed with the help of the data mining method CRISP-DM.',
	link: 'https://smxtournament.no',
	type: 'website',
  },
  {
    logo: SMXbot,
    title: 'SMX Weekly Bot',
    description: 'A Discord bot written in Python that fetches and posts weekly challenge data for StepManiaX players. I built a scraper, integrated with Discord’s API, and set up scheduled tasks for automatic updates.',
	link: 'https://github.com/Limorinho//SMX-Weekly-League-Bot',
	type: 'repo',
  },
  {
    logo: NTB,
    title: 'New Times Burger',
    description: 'A responsive restaurant website developed in PHP with a MySQL database. It includes a dynamic menu, reservation system, and admin dashboard for managing content.',
	link: 'https://github.com/Limorinho//NTB',
	type: 'repo',
  },
];

  let current = 0;
  const interval = 5000;

  const next = () => current = (current + 1) % items.length;

  const autoplay = setInterval(next, interval);

  // Optional: pause on hover or destroy interval on component destroy
  import { onDestroy } from 'svelte';
  onDestroy(() => clearInterval(autoplay));	

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>
  


<div class="py-6 sm:py-8 lg:py-12">
	<div class="mx-auto max-w-screen-xl px-4 md:px-8">
		<div class="flex flex-col md:flex-row md:items-stretch gap-8 lg:gap-12">
		<div class="flex-1">
			<div class="w-full max-w-xl mx-auto mt-5">
				<div class="relative rounded-xl text-center transition-all duration-700 ease-in-out h-[210px]">
				  <img src={items[current].logo} alt={items[current].title} class="h-16 mx-auto mb-4" />
				  <h1 class="text-xl text-(--color-theme-1) font-bold mb-2">{items[current].title}</h1>
				  <p class="text-(--color-theme-1)  text-sm">{items[current].description}</p>
				</div>

				<div class="flex items-center justify-center h-[190px]">
					<button
					class="bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center inline-flex text-white-600 items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
						<a href={items[current].link} target="_blank" class="flex items-center gap-2 text-white">
						{#if items[current].type === 'website'}
						<Globe class="w-6 h-6 text-white" />
						<span class="relative w-full text-white">View Website</span>
						{:else}
						<svg class="h-6 w-6" width="32" height="32" viewBox="0 0 24 24" fill="#ffffff" xmlns="http://www.w3.org/2000/svg">
						<path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
						</svg>
						<span class="relative w-full text-white">View Repository</span>
						{/if}
						</a>
					</button>
				</div>

				<!-- Optional nav buttons -->
				<div class="flex justify-center mt-4 space-x-2">
				  {#each items as _, i}
					<button
					  class="w-3 h-3 rounded-full border-2"
					  class:border-blue-500={current === i}
					  class:bg-blue-500={current === i}
					  on:click={() => current = i}>
					</button>
				  {/each}
				</div>
			  </div>

		</div>
		
		<div class="hidden md:flex justify-center">
			<div class="h-full w-[2px] rounded bg-gradient-to-b from-sky-400 to-emerald-600 opacity-60"></div>
		  </div>
		  
		<div class="md:pt-4 flex-1">
  
		  <h1 class="mb-4 text-center text-2xl font-bold text-gray-800 sm:text-3xl md:mb-6 md:text-left text-transparent bg-clip-text bg-gradient-to-r to-emerald-600 from-sky-400">Linor Ujkani</h1>
		  <p class="mb-6 text-sky-400 sm:text-lg md:mb-8">
			I am a software developer with a bachelor's degree in Computer Science, currently pursuing a Master's in Artificial Intelligence.
		</p>
		  <p class="mb-6 text-sky-400 sm:text-lg md:mb-8">In my free time, I enjoy programming, reading, and watching YouTube. My interest in programming has led me to develop multiple projects, which I've showcased here!</p>
		
		  <div class="flex gap-4">
			<a href="#" target="_blank" class=" transition duration-100 hover:text-gray-500 active:text-gray-600">
			  <svg class="h-6 w-6" width="32" height="32" viewBox="0 0 24 24" fill="#29cce5" xmlns="http://www.w3.org/2000/svg">
				<path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z" />
			  </svg>
			</a>
  
			<a href="#" target="_blank" class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
			  <svg class="h-6 w-6" width="32" height="32" viewBox="0 0 24 24" fill="#29cce5" xmlns="http://www.w3.org/2000/svg">
				<path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
			  </svg>
			</a>
  
			<a href="#" target="_blank" class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
			  <svg class="h-6 w-6" width="32" height="32" viewBox="0 0 24 24" fill="#29cce5" xmlns="http://www.w3.org/2000/svg">
				<path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
			  </svg>
			</a>
  
			<a href="#" target="_blank" class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
			  <svg class="h-6 w-6" width="32" height="32" viewBox="0 0 24 24" fill="#29cce5" xmlns="http://www.w3.org/2000/svg">
				<path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z" />
			  </svg>
			</a>
		  </div>

		  <div class="pt-10">
		  <a href="/projects"
		  class="relative inline-flex text-center rounded-full items-center bg-gradient-to-r to-emerald-600 from-sky-400 justify-start py-3 pl-4 pr-12 overflow-hidden font-semibold transition-all duration-150 ease-in-out hover:pl-10 hover:pr-6 hover:bg-indigo-100 group">
		  
		  <span class="absolute right-0 pr-4 duration-200 ease-out group-hover:translate-x-12">
			<svg class="w-5 h-5 text-white" xmlns="http://www.w3.org/2000/svg" width="24"
			  height="24" viewBox="0 0 24 24" fill="none">
			  <path
				d="M14.9385 6L20.9999 12.0613M20.9999 12.0613L14.9385 18.1227M20.9999 12.0613L3 12.0613"
				stroke="currentcolor" stroke-width="1.6" stroke-linecap="round"
				stroke-linejoin="round" />
			</svg>
		  </span>
		  <span
			class="absolute left-0 pl-2.5 -translate-x-12 group-hover:translate-x-0 ease-out duration-200">
			<svg class="w-5 h-5 text-white" xmlns="http://www.w3.org/2000/svg" width="24"
			  height="24" viewBox="0 0 24 24" fill="none">
			  <path
				d="M14.9385 6L20.9999 12.0613M20.9999 12.0613L14.9385 18.1227M20.9999 12.0613L3 12.0613"
				stroke="currentcolor" stroke-width="1.6" stroke-linecap="round"
				stroke-linejoin="round" />
			</svg>
		  </span>
		  <span
			class="relative w-full text-white text-left transition-colors duration-200 ease-in-out">Explore more</span>
		  </a>
		</div>

		</div>
	  </div>
	</div>
  </div>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}
	
</style>
