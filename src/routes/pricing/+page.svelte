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
      name: "Ava Landers",
      position: "COO",
      company: "Urban Fry Co.",
      quote:
        "We modeled KAIKAKU side-by-side with our legacy systems—now our throughput is up 22% and labor spend dropped by nearly a third. The platform paid for itself in weeks.",
      image: "/generated/image-a-polished-headshot-of-a-successful-whit.webp"
    },
    {
      name: "Malik Chen",
      position: "VP of Store Operations",
      company: "Thrive Kitchen",
      quote:
        "Rolling out FUSICON across 40 sites took less than a month and caused zero downtime. Assembly bottlenecks are gone, and making changes is as easy as tapping a button.",
      image: "/generated/image-a-refined-headshot-of-an-accomplished-ea.webp"
    },
    {
      name: "Lina Okonkwo",
      position: "Director of Workforce Planning",
      company: "RevoEats",
      quote:
        "KAIKAKU Intelligence has cut our scheduling admin to under an hour per week. Forecast accuracy is above 95%, so we can schedule lean and still hit service targets.",
      image: "/generated/image-a-distinguished-headshot-of-a-black-fema.webp"
    }
  ]}
/>

<CallToAction
  title="Stop bleeding margin. Start scaling intelligently."
  subtitle="Bring robotics and AI to your kitchen with KAIKAKU."
  description="KAIKAKU cuts labor costs, accelerates throughput, and expands margins—powered by automation and AI. Built for QSR chains ready for real transformation."
  imageSrc="/generated/image-a-cheerful-quick-service-restaurant-mana.webp"
  callsToAction={[
    { href: '/contact', label: 'Request a demo', variant: 'primary' },
    { href: '/overview', label: 'Download overview', variant: 'secondary' }
  ]}
/>
