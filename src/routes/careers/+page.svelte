<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Pioneer AI Safety Research",
			description: "Lead groundbreaking research in emotional intelligence mapping that shapes the future of human-aligned AI systems.",
			icon: IconBriefcase
		},
		{
			title: "Accelerated Career Growth",
			description: "Fast-track your expertise in the emerging $240B AI market with mentorship from Stanford HAI alumni and access to top-tier research conferences.",
			icon: IconUsers
		},
		{
			title: "Impact-Driven Mission",
			description: "Bridge the gap between human values and technology, directly influencing how AI systems understand and respond to human emotions.",
			icon: IconHeart
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
		{
			name: "Dr. Ken Tanaka",
			position: "Senior AI Research Scientist",
			company: "Research Team",
			quote:
				"At Kokoro Research, I'm not just building AI systems — I'm helping shape how technology understands human emotions. The interdisciplinary collaboration here between psychologists, ethicists, and engineers creates breakthrough research that's both cutting-edge and deeply meaningful.",
			image: "/generated/image-a-professional-headshot-of-an-asian-male.webp"
		},
		{
			name: "Dr. Sofia Rodriguez",
			position: "Machine Learning Engineer",
			company: "Engineering Team",
			quote:
				"What drew me to Kokoro Research was the mission to bridge human values with AI development. Every day, I work on projects that directly impact how future AI systems will understand and respond to human needs. The growth opportunities are incredible — from publishing at top-tier conferences to collaborating with Stanford HAI alumni.",
			image: "/generated/image-a-professional-headshot-of-a-latina-fema.webp"
		},
		{
			name: "Marcus Thompson",
			position: "Product Manager",
			company: "Product Team",
			quote:
				"The culture here is unlike anywhere else I've worked. We're tackling one of the most important challenges of our time — ensuring AI systems are aligned with human values. Leadership genuinely invests in your professional development, and the work environment encourages both innovation and thoughtful ethical consideration.",
			image: "/generated/image-a-professional-headshot-of-a-black-male-.webp"
		}
	];

	const processSteps = [
		{
			step: 1,
			title: "Apply with Research Focus",
			description:
				"Submit your application highlighting your experience in AI research, emotional intelligence, or human-computer interaction. Include relevant publications or research projects."
		},
		{
			step: 2,
			title: "Technical & Values Assessment",
			description: "Engage in deep discussions about AI safety, human-centered design principles, and your vision for responsible AI development with our research team."
		},
		{
			step: 3,
			title: "Join the Mission",
			description: "Become part of our pioneering team developing the next generation of emotionally intelligent AI systems that bridge human values and technological advancement."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Human-Centered Innovation",
			description: "Every AI system we develop prioritizes human values and emotional intelligence, ensuring technology serves humanity."
		},
		{
			icon: IconUsers,
			title: "Interdisciplinary Excellence",
			description: "We unite AI researchers, psychologists, and ethicists to create breakthrough solutions in responsible AI development."
		},
		{
			icon: IconGlobe,
			title: "Transformative Impact",
			description: "Our research shapes how AI systems understand human emotions, creating safer and more aligned artificial intelligence for the world."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Shape the future of human-centered AI"
	subtitle="Join our passionate team of researchers and engineers as we bridge the gap between human values and technological advancement. Together, we're building AI that truly understands and serves humanity."
	imageSrc="/generated/image-a-diverse-group-of-researchers-in-a-mode.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
