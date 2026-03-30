<script lang="ts">
	import './layout.css';

	const { children } = $props();
</script>

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
