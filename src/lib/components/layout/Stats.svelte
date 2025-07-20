<script lang="ts">
	// Icons
	import IconClock from "~icons/lucide/clock";
	import IconLaptop from "~icons/lucide/laptop";
	import IconBuilding from "~icons/lucide/building";

	type StatItem = {
		value: string;
		description: string;
		icon: typeof IconClock;
	};

	// Props
	const {
		stats = [
			{
				value: "3 mins",
				description: "to set up your network",
				icon: IconClock
			},
			{
				value: "2.5m",
				description: "devices connected",
				icon: IconLaptop
			},
			{
				value: "10K+",
				description: "companies running Tailscale",
				icon: IconBuilding
			}
		],
		class: classes = ""
	}: { stats?: StatItem[]; class?: string } = $props();
</script>

<section class="w-full py-16 md:py-24 {classes}">
	<div class="container mx-auto px-6 lg:px-8">
		<div class="grid grid-cols-1 gap-12 md:grid-cols-3 md:gap-8">
			{#each stats as stat}
				<div class="flex flex-col items-center text-center md:items-center">
					{#if stat.iconName === 'clock'}
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-primary-700 mb-4 h-8 w-8 opacity-80"><circle cx="12" cy="12" r="10"/><polyline points="12,6 12,12 16,14"/></svg>
					{:else if stat.iconName === 'laptop'}
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-primary-700 mb-4 h-8 w-8 opacity-80"><path d="m20 16-4-4V4a2 2 0 0 0-2-2H4a2 2 0 0 0-2 2v8l-4 4v4h20v-4Z"/><path d="M6 18h.01"/><path d="M10 18h.01"/></svg>
					{:else if stat.iconName === 'building'}
						<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-primary-700 mb-4 h-8 w-8 opacity-80"><rect width="16" height="20" x="4" y="2" rx="2" ry="2"/><path d="M9 22v-4h6v4"/><path d="M8 6h.01"/><path d="M16 6h.01"/><path d="M12 6h.01"/><path d="M12 10h.01"/><path d="M12 14h.01"/><path d="M16 10h.01"/><path d="M16 14h.01"/><path d="M8 10h.01"/><path d="M8 14h.01"/></svg>
					{/if}
					<span class="text-title1 mb-2 text-gray-900 dark:text-gray-50">{stat.value}</span>
					<span class="text-body text-gray-600 dark:text-gray-300">{stat.description}</span>
				</div>
			{/each}
		</div>
	</div>
</section>
