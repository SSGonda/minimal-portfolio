<script lang="ts">
	import './layout.css';
	const { children } = $props();
</script>

<svelte:head>
	<title>stephen gonda.</title>
	<meta name="description" content="The portfolio site of Stephen Gonda." />
	<link rel="icon" type="image/png" href="/favicon-96x96.png" sizes="96x96" />
	<link rel="icon" type="image/svg+xml" href="/favicon.svg" />
	<link rel="shortcut icon" href="/favicon.ico" />
	<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png" />
	<meta name="apple-mobile-web-app-title" content="stephen." />
	<link rel="manifest" href="/site.webmanifest" />
</svelte:head>

<div class="bg-gray-50">
	<div
		class="sticky top-0 z-50 flex flex-col justify-end gap-3 bg-gray-50 p-6 text-xl font-light md:flex-row md:gap-12 md:px-20 md:text-2xl"
	>
		<a href="#hero" class="mr-auto mb-auto font-semibold">stephen gonda.</a>
		<a href="#skills" class="hover:underline">skills</a>
		<a href="#projects" class="hover:underline">projects</a>
		<a href="#contact" class="hover:underline hover:ease-in-out">contact</a>
	</div>
	{@render children()}
</div>
