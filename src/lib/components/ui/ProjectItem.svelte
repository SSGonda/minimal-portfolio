<script lang="ts">
	import SquareArrowOutUpRight from '@lucide/svelte/icons/square-arrow-out-up-right';
	import FolderGit2 from '@lucide/svelte/icons/folder-git-2';
	import type { Project } from '$lib/types.js';
	let { title, stack, description, link, image, repo }: Project = $props();
</script>

<div id={title} class="flex flex-col md:flex-row">
	<img src={image} class="p-10 md:w-1/2" alt="wribit" />
	<div class="p-10 md:w-1/2">
		<h3 class="mb-3 text-3xl font-bold">{title}</h3>
		<p class="mb-2 text-xl font-light">{stack}</p>
		<p class="mb-3 text-xl">{description}</p>
		{#if repo}
			<a rel="external" href={repo} target="_blank" class="flex gap-2 underline"
				><FolderGit2 /> See the repo.</a
			>
		{/if}
		{#if link}
			<a rel="external" href={link} target="_blank" class="flex gap-2 underline"
				><SquareArrowOutUpRight /> See it in action!</a
			>
		{/if}
	</div>
</div>
