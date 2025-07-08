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
			name: "Dmitri Volkov",
			position: "Chief Financial Officer",
			company: "Meridian Industries",
			quote:
				"Credix delivered an immediate 40% increase in average order value while eliminating our credit risk exposure. The ROI was visible within the first quarter.",
			image:
				"/generated/image-a-professional-headshot-of-dmitri-volkov.webp"
		},
		{
			name: "Amara Okafor",
			position: "Finance Director",
			company: "Apex Manufacturing",
			quote:
				"The 2-minute approval process eliminated our biggest sales bottleneck. We've seen conversion rates jump to 75% since implementing Credix embedded financing.",
			image:
				"/generated/image-a-professional-headshot-of-amara-okafor-.webp"
		},
		{
			name: "Kenji Nakamura",
			position: "Operations Manager",
			company: "Velocity Logistics",
			quote:
				"Setup was incredibly straightforward - our team was up and running in days, not months. The platform's reliability has been flawless with genuine 24/7 support.",
			image:
				"/generated/image-a-professional-headshot-of-kenji-nakamur.webp"
		}
	]}
/>

<CallToAction
	title="Transform your B2B sales today"
	subtitle="Join industry leaders growing with Credix"
	description="Start offering embedded financing to your customers and unlock new revenue streams. With less than 2-minute approvals, 100% credit limit lift, and 99.9% uptime, Credix empowers your business to grow customer purchasing power while protecting your margins."
	imageSrc="/generated/image-a-business-professional-standing-in-a-mo.webp"
	callsToAction={[
		{
			href: "/contact",
			label: "Schedule a demo",
			variant: "primary"
		},
		{
			href: "/contact",
			label: "Talk to sales",
			variant: "secondary"
		}
	]}
/>
