<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
	testimonials={[
		{
			name: "Elise Tanaka",
			position: "Director of Safety Research",
			company: "LatentScale",
			quote:
				"Adding Kokoro's emotional intelligence layer to our alignment stack helped us resolve ethical ambiguity 3x faster in our internal red teaming. The ROI was immediate and measurable.",
			image: "/generated/image-a-professional-headshot-of-an-asian-woma.webp"
		},
		{
			name: "Dr. Armin Vogel",
			position: "Cognitive Scientist",
			company: "Oxford Values Lab",
			quote:
				"The emotional values dataset from Kokoro was more predictive of human judgment than any behavioral metric we'd used prior. Implementation took just two weeks and delivered results that would have taken our team months to achieve.",
			image: "/generated/image-a-professional-headshot-of-a-german-man-.webp"
		},
		{
			name: "Nia Brook",
			position: "Lead ML Engineer",
			company: "Parallax Labs",
			quote:
				"We saw a 25% increase in user trust ratings after fine-tuning with Kokoro's alignment signals. The pricing pays for itself when you consider the cost of retraining models that miss human nuance.",
			image: "/generated/image-a-professional-headshot-of-a-black-woman.webp"
		}
	]}
/>

<CallToAction
	title="AI that understands what it means to be human"
	subtitle="Join the researchers building responsible AI"
	description="Build emotionally intelligent systems grounded in real human values. Kokoro Research helps AI teams move beyond mechanical responses to meaningful alignment—proven to improve human-AI interaction metrics by 40%. Start integrating values into your training pipeline today."
	imageSrc="/generated/image-a-researcher-sitting-at-a-desk-in-a-cozy.webp"
	callsToAction={[
		{
			href: "/contact",
			label: "Start a pilot program",
			variant: "primary"
		},
		{
			href: "/research",
			label: "View research",
			variant: "secondary"
		}
	]}
/>
