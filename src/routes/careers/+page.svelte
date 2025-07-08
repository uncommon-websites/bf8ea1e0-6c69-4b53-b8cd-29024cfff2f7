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
			title: "Shape the Future of Finance",
			description: "Build cutting-edge embedded financing solutions that transform how B2B businesses extend credit and accelerate growth.",
			icon: IconBriefcase
		},
		{
			title: "Accelerated Growth",
			description: "Join a high-growth fintech revolutionizing credit approvals from days to minutes. Your career will move as fast as our technology.",
			icon: IconUsers
		},
		{
			title: "Industry-Leading Impact",
			description: "Work with iconic brands like Volvo Trucks, Acer, and industry leaders. Your work directly drives business transformation.",
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
			name: "Michael Chen",
			position: "Senior Developer",
			company: "Engineering Team",
			quote:
				"At Credix, I'm building technology that transforms how businesses access credit. The pace of innovation is incredible - we're constantly pushing the boundaries of what's possible in fintech. What I love most is the collaborative culture where everyone's voice matters, and the growth opportunities are endless.",
			image: "/generated/image-a-professional-portrait-of-an-asian-male.webp"
		},
		{
			name: "Priya Sharma",
			position: "Product Designer",
			company: "Design Team",
			quote:
				"Working on embedded financing solutions for iconic brands like Volvo Trucks and Acer has been incredibly rewarding. The company invests heavily in our professional development, and I've grown from a junior designer to leading major product initiatives in just two years. The work environment is both challenging and supportive.",
			image: "/generated/image-a-professional-portrait-of-a-south-asian.webp"
		},
		{
			name: "Marcus Johnson",
			position: "Marketing Lead",
			company: "Marketing Team",
			quote:
				"Credix's mission to accelerate B2B credit approvals from days to minutes is genuinely exciting to be part of. The leadership genuinely cares about work-life balance while maintaining our high standards. I've had amazing mentorship opportunities and the chance to shape our go-to-market strategy with industry leaders.",
			image: "/generated/image-a-professional-portrait-of-an-african-am.webp"
		}
	];

	const processSteps = [
		{
			step: 1,
			title: "Apply & Screen",
			description:
				"Submit your application with resume and portfolio. Our team will review your background and conduct an initial screening call."
		},
		{
			step: 2,
			title: "Technical & Cultural Assessment",
			description: "Meet with hiring managers and team members for technical evaluation and cultural fit assessment to ensure mutual alignment."
		},
		{
			step: 3,
			title: "Final Interview & Offer",
			description: "Complete final interviews with leadership, receive your offer, and join our mission to transform B2B financing."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Speed & Excellence",
			description: "We deliver sub-2 minute credit approvals and maintain 99.9% uptime. Excellence at speed is our standard."
		},
		{
			icon: IconUsers,
			title: "Customer-Centric Innovation",
			description: "Every solution we build drives real business impact - increasing purchasing power while protecting margins."
		},
		{
			icon: IconGlobe,
			title: "Trusted Partnership",
			description: "We're the trusted partner to industry leaders, providing 24/7 support and 100% credit limit lift guarantees."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Build the future of B2B financing"
	subtitle="Join Credix and help transform how businesses access credit. We're building embedded financing solutions that empower companies to grow their purchasing power while protecting margins. Be part of a team that delivers sub-2 minute approvals and partners with iconic brands."
	imageSrc="/generated/image-a-diverse-team-of-professionals-engaged-.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join Credix?" subtitle="Build your career while revolutionizing B2B financing" />

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
