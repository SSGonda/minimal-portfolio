<script lang="ts">
	import ProjectItem from '$lib/components/ui/ProjectItem.svelte';
	import type { Project } from '$lib/types.js';
	import { TypeWriter } from 'svelte-typewrite';

	let projects: Project[] = [
		{
			title: 'wribit.',
			stack: 'svelte, postgressql, docker, cloudflare',
			description:
				'A notes app with sandboxed code execution, LaTeX support, and Realtime Collaboration.',
			link: 'https://wribit.com',
			image: '/images/wribit.webp'
		},
		{
			title: '2025 Philippine Elections in a Nutshell (Hindsight is 20-25!)',
			stack: 'selenium, sklearn, matplotlib, plotly',
			description:
				'An exploratory data analysis and linear model of the 2025 Philippine Midterm Elections from scraped social media posts on Twitter; sentiments analyzed through an agentic workflow with Llama-4-Maverick-17B-128E-Instruct.',
			repo: 'https://github.com/SSGonda/2025ElectionsInANutshell',
			link: 'https://nutelex.wribit.com/',
			image: '/images/elections.png'
		},
		{
			title: 'The UP ParseNet',
			stack: 'svelte, cloudflare',
			description:
				'A lightweight news site with a Content Management System (CMS) for The UP Parser!',
			repo: 'https://github.com/nViNova/parser',
			link: 'https://theupparser.pages.dev',
			image: '/images/parsenet.png'
		},
		{
			title:
				'Seconds to action: Spatiotemporal analysis and Cellular Automata Modelling of crowd-sourced Philippine Earthquake Data',
			stack: 'numpy, sklearn, matplotlib, pandas',
			description:
				'A scientific computing project to produce synthetic earthquake data which mimics the geologic qualities of the 2023 Davao Earthquake using the Olami-Feder-Christensen (OFC) model.',
			repo: 'https://github.com/SHIROKAMIQQ/cs138project',
			link: 'https://bit.ly/SecondsToAction',
			image: '/images/secondstoaction.png'
		},
		{
			title: 'BomberLAN',
			stack: 'dart, haskell',
			description:
				'A LAN multiplayer bomberman clone with a thin-client, thick-server architecture capable of cross platform play.',
			repo: 'https://github.com/SSGonda/BomberLAN',
			image: '/images/bomberlan.png'
		},
		{
			title: 'MNIST - Number Draw!',
			stack: 'streamlit, pytorch, pyxel',
			description:
				'A short data science project that performs inferences on handwritten digits with a Neural Network Model trained on the MNIST Dataset using PyTorch.',
			repo: 'https://github.com/nViNova/MNIST',
			link: 'https://kunopsim.streamlit.app/',
			image: '/images/mnist.png'
		},
		{
			title: 'Assembly Python Ception',
			stack: 'python, assembly, pyxel',
			description:
				'An assembler and emulator on a custom instruction set based on the Harvard Architecture made with Python and visuals shown using Pyxel. A snake game was made to demonstrate the emulator and monitor made with Pyxel.',
			repo: 'https://github.com/SSGonda/AssemblyPythonCeption',
			image: '/images/assemblypythonception.png'
		}
	];
</script>

<section
	id="hero"
	class="flex h-[calc(100vh-18rem)] w-full flex-col items-start justify-start px-8 pt-10 pb-36 md:h-[calc(100vh-3rem)] md:px-24"
>
	<h1 class="mt-auto text-6xl font-bold md:text-9xl">Stephen</h1>
	<h1 class="bg-amber-300 text-6xl font-bold md:text-9xl">Gonda</h1>
	<!-- <h1 class="text-9xl font-bold"></h1> -->
</section>

<section id="action" class="hidden h-screen w-full flex-col items-center justify-center md:flex">
	<h2 class="text-center text-xl font-bold wrap-normal md:text-8xl">
		writer, data <span class="bg-amber-300">engineer</span>, software <br /> developer
	</h2>
	<div class="my-6">
		<p>
			Building projects <span class="font-bold"
				><TypeWriter texts={['with a story.', 'with an impact.', 'with a purpose.']} /></span
			>
		</p>
	</div>
</section>

<section id="action" class="flex h-screen w-full flex-col items-center justify-center md:hidden">
	<h2 class="text-center text-4xl font-bold wrap-normal">writer</h2>
	<h2 class="text-center text-4xl font-bold">data <span class="bg-amber-300">engineer</span></h2>
	<h2 class="text-center text-4xl font-bold">software</h2>
	<h2 class="bg-amber-300 text-center text-4xl font-bold">developer.</h2>
	<div class="my-6">
		<p>
			Building projects <span class="font-bold"
				><TypeWriter texts={['with a story.', 'with an impact.', 'with a purpose.']} /></span
			>
		</p>
	</div>
</section>

<section id="skills" class="flex h-screen w-full flex-col px-8 pt-10 pb-36 md:flex-row md:px-24">
	<h2 class="flex flex-col justify-center text-6xl font-bold md:w-1/2 lg:text-8xl">
		I build with,
	</h2>
	<div class="flex flex-col justify-center text-xl md:w-1/2 md:text-3xl">
		<h3 class="my-3 font-bold">web.</h3>
		<p class="text-xl font-light">
			<span class="bg-amber-300">svelte</span>, react, vue, tailwind, postgressql, mongodb
		</p>
		<h3 class="my-3 font-bold">data science.</h3>
		<p class="text-xl font-light">python, pytorch, tensorflow, sklearn, plotly, matplotlib</p>
		<h3 class="my-3 font-bold">cloud and systems.</h3>
		<p class="text-xl font-light">docker, terraform, cloudflare, oracle cloud, aws</p>
	</div>
</section>

<section id="projects" class="flex w-full flex-col px-8 pt-10 pb-36 md:px-24">
	<h2 class="ml-auto text-right text-6xl font-bold lg:text-8xl">
		I <span class="bg-amber-300">worked</span> on,
	</h2>
	<div class="my-6 ml-auto">
		<p>Building projects with a <span class="bg-amber-300 font-black">purpose.</span></p>
	</div>
	{#each projects as project(project.title)}
		<ProjectItem {...project} />
	{/each}
</section>

<section id="contact" class="flex w-full flex-col items-center px-8 pt-10 pb-36 md:px-24">
	<h2 class="text-6xl font-bold lg:text-8xl">let's <span class="bg-amber-300">talk</span>.</h2>
	<div class="my-6 text-xl">
		<p>Got an idea? Let's build it.</p>
	</div>
	<div class="flex justify-end gap-3">
		<a href="https://linkedin.com/in/sjgonda" class="underline">linkedin</a>
		<a href="https://github.com/SSGonda" class="underline">github</a>
		<a href="mailto:stephenjgonda@gmail.com" class="underline">stephenjgonda@gmail.com</a>
	</div>
</section>
