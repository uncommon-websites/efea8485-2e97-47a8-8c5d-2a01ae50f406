<script lang="ts">
	// Types
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
					<stat.icon class="text-primary-700 mb-4 h-8 w-8 opacity-80" />
					<span class="text-title1 mb-2 text-gray-900 dark:text-gray-50">{stat.value}</span>
					<span class="text-body text-gray-600 dark:text-gray-300">{stat.description}</span>
				</div>
			{/each}
		</div>
	</div>
</section>
