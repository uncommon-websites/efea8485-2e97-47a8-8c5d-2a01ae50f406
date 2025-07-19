<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CenteredTextOnlyHero from "$lib/components/layout/hero-sections/CenteredTextOnlyHero.svelte";
	import UseCases from "$lib/components/layout/UseCases.svelte";
</script>

<CenteredTextOnlyHero
	title="Technology that feels human"
	subtitle="We map emotional intelligence to help teams build systems that understand, adapt, and connect—more like people do."
	imageSrc="/generated/image-a-group-of-diverse-people-in-an-open-off.webp"
/>
<LogoScroller 
	label="Trusted by leading AI research companies"
	logoUrls={[
		'https://logo.clearbit.com/anthropic.com',
		'https://logo.clearbit.com/deepmind.com',
		'https://logo.clearbit.com/huggingface.co',
		'https://logo.clearbit.com/cohere.ai'
	]}
/>

<Summary
	title="What we do"
	text="Kokoro Research develops human-centered AI by mapping emotional intelligence to bridge the gap between human values and technological advancement. We help AI researchers build systems that understand emotional context and align with human decision-making patterns."
/>

<Testimonials
	testimonials={[
		{
			name: "Marta Liden",
			position: "Head of AI Safety",
			company: "Novira Labs",
			quote:
				"Kokoro's emotional intelligence mapping cut our model validation time by 60%. We now deploy human-aligned AI systems 3x faster than before, saving months of iteration cycles.",
			image:
				"/generated/image-a-professional-woman-ai-researcher-is-wo.webp"
		},
		{
			name: "Nael Kumari",
			position: "Research Director",
			company: "Cedral AI",
			quote:
				"Their human values framework eliminated our biggest regulatory risk. We avoided a potential $2M compliance issue by catching alignment problems early in development.",
			image:
				"/generated/image-a-professional-man-an-ai-research-direct.webp"
		},
		{
			name: "Zara Thorne",
			position: "VP of AI Product",
			company: "Apex Technologies",
			quote:
				"Kokoro's emotional intelligence data reduced our AI training costs by 45%. Instead of rebuilding models from scratch, we enhanced existing ones with their proven datasets.",
			image:
				"/generated/image-a-professional-woman-technology-leader-i.webp"
		}
	]}
/>

<Features
	title="Emotional intelligence, engineered"
	subtitle="The missing layer in AI safety—human values and emotions mapped for responsible AI development"
	features={[
		{
			title: "Deep emotional intelligence mapping",
			description: "Proprietary datasets built on validated psychological frameworks that give AI systems the missing context to understand human nuance, emotions, and intent."
		},
		{
			title: "Human-aligned AI development",
			description: "Emotionally aware decision trees and value alignment scoring designed to integrate directly into AI training and inference cycles for safer model behavior."
		},
		{
			title: "Proven measurable outcomes",
			description: "Real-world tested with 40% improvement in human-AI alignment metrics, backed by peer-reviewed case studies published at top AI conferences."
		},
		{
			title: "Purpose-built for AI researchers",
			description: "Plug-and-play emotional modeling APIs and value alignment tools designed specifically for AI safety researchers at tech companies and research institutions."
		},
		{
			title: "Enterprise-ready platform",
			description: "End-to-end pilot programs with measurable human satisfaction gains, trusted by teams backed by leading AI-focused venture capital firms."
		},
		{
			title: "Responsible AI at scale",
			description: "Bridge the gap between human values and technological advancement with tools that ensure every AI decision is truly human-centered and ethically sound."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for AI emotional intelligence"
	useCases={[
		{
			title: "Accelerate AI safety research",
			description: "When building human-aligned AI systems, researchers need validated emotional intelligence data. Kokoro's frameworks reduce model validation time by 60% and prevent costly alignment failures.",
			image: "/generated/image-a-group-of-researchers-dressed-in-casual.webp",
			link: {
				href: "/use-cases/ai-safety-research",
				label: "Learn more"
			}
		},
		{
			title: "Improve human-AI interaction",
			description: "AI systems that understand emotional context create better user experiences. Kokoro's emotional mapping improves human-AI interaction metrics by 40% in real-world testing.",
			image: "/generated/image-in-a-contemporary-laboratory-setting-peo.webp",
			link: {
				href: "/use-cases/human-ai-interaction",
				label: "Learn more"
			}
		},
		{
			title: "Scale responsible AI development",
			description: "Enterprise teams need to ensure AI systems align with human values at scale. Kokoro's platform prevents regulatory risks and enables ethical AI deployment across organizations.",
			image: "/generated/image-a-diverse-team-of-professionals-is-seate.webp",
			link: {
				href: "/use-cases/responsible-ai-development",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
	title="Ready to build human-aligned AI?"
	subtitle="Start your pilot program today"
	description="Join leading AI research teams who trust Kokoro Research to map emotional intelligence and build truly human-centered AI systems. See measurable improvements in your next release cycle."
	imageSrc="/generated/image-a-cheerful-researcher-sitting-at-a-desk-.webp"
	callsToAction={[
		{
			href: "/contact",
			label: "Start pilot program",
			variant: "primary"
		},
		{
			href: "/research",
			label: "View our research",
			variant: "secondary"
		}
	]}
/>
