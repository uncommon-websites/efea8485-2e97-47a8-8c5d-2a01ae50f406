<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Human-centered design",
			description: "Every AI system we help create prioritizes human values, emotions, and decision-making patterns at its core."
		},
		{
			title: "Responsible development",
			description: "Advancing AI safety through rigorous emotional intelligence mapping and ethical alignment research."
		},
		{
			title: "Bridging understanding",
			description: "Connecting the gap between technological capability and human emotional complexity for meaningful progress."
		}
	];
</script>

<SecondaryHero
	title="Building AI that understands humanity"
	subtitle="through deep emotional intelligence mapping"
	imageSrc="/generated/image-a-diverse-group-of-professionals-dressed.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"The challenge hit us during late-night research sessions: how do we build AI systems that truly understand what humans value? While the tech world raced toward more powerful models, we saw a critical gap between artificial intelligence and human emotional intelligence.",
		"Founded by CEO Ryuzo Kijima, Kokoro Research emerged from a simple yet profound realization: AI safety isn't just about preventing harmful outputs, it's about creating systems that genuinely comprehend human emotions, values, and decision-making patterns. We're mapping the emotional landscape that makes us uniquely human.",
		"Today, we partner with AI researchers at leading tech companies, providing the deep emotional intelligence datasets they need to build truly human-aligned systems. Our work bridges the gap between technological advancement and human values, ensuring AI development stays grounded in what matters most: understanding and serving humanity."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Our team."
	subtitle="Leading the future of human-aligned AI."
	stakeholders={[
		{
			name: "Ryuzo Kijima",
			position: "Founder & CEO",
			bio: "Pioneering human-centered AI development through deep emotional intelligence mapping to bridge technology and human values.",
			image: "/generated/image-a-professional-business-portrait-of-a-ja.webp"
		}
	]}
/>

<!-- Investors section removed - no specific investors mentioned -->

<!-- CTA Section -->
<CallToAction
	title="Ready to build human-aligned AI?"
	subtitle="Partner with us"
	description="Join leading AI researchers and tech companies who are leveraging our emotional intelligence datasets to create more responsible, human-centered AI systems."
/>
