<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={true}
  title="Efficiency at scale, without the extra overhead"
  subtitle="Transform high-volume operations with a fully integrated restaurant system—built for consistency, speed, and higher margins across every location. No added headcount required."
  customers={[
    {
      name: "Alicia Nguyen",
      position: "VP operations, FreshBowl",
      imageSrc: "/generated/image-a-confident-asian-woman-in-business-atti.webp",
    },
    {
      name: "Marcus Lewis",
      position: "Director of tech, SpeedEats",
      imageSrc: "/generated/image-a-poised-black-man-in-a-suit-serving-as-.webp",
    },
    {
      name: "Priya Patel",
      position: "COO, Urban Bites",
      imageSrc: "/generated/image-a-professional-south-asian-woman-the-res.webp",
    },
    {
      name: "Carlos Romero",
      position: "Director of strategy, GoQuick",
      imageSrc: "/generated/image-a-latino-man-in-a-casual-suit-serving-as.webp",
    },
    {
      name: "Emma Johansson",
      position: "Head of experience, NordicBite",
      imageSrc: "/generated/image-a-scandinavian-woman-with-a-crisp-busine.webp"
    },
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		'https://logo.clearbit.com/mcdonalds.com',
		'https://logo.clearbit.com/yum.com',
		'https://logo.clearbit.com/arbys.com'
	]}
/>

<Summary
	title="How tomorrow runs"
	text="KAIKAKU is a next-generation restaurant operating system built from scratch for quick-service chains. Powered by robotics and AI, our platform brings automation, real-time intelligence, and margin expansion—so your restaurants run faster, with fewer hands, and greater consistency."
/>

<Testimonials
	testimonials={[
		{
			name: "Ellis Raynor",
			position: "SVP, strategy",
			company: "Global QSR Group",
			quote: "We cut order assembly time in half—and consistently hit peak throughput, even during our busiest hours. KAIKAKU’s automation meant fewer errors and more happy guests, with less stress for my team.",
			image: "/generated/image-a-male-executive-in-a-modern-quick-servi.webp"
		},
		{
			name: "Malika Trenton",
			position: "Director of restaurant innovation",
			company: "CopperGrill Group",
			quote: "Consistency was a huge challenge with staff turnover. Now, bowls at all our locations look and taste the same—our team focuses on guest service, not micromanaging prep. KAIKAKU saved us time and major training costs.",
			image: "/generated/image-a-female-director-in-a-bustling-restaura.webp"
		},
		{
			name: "Rakeem Cho",
			position: "COO",
			company: "Imperial Bowls International",
			quote: "Margins in our category are razor-thin. With KAIKAKU, we saw measurable savings in labor and supply waste within the first month—plus insights I wish I had years ago.",
			image: "/generated/image-an-asian-male-coo-in-a-corporate-office-.webp"
		}
	]}
/>

<Features
	title="The operating system for automation-first restaurants"
	subtitle="Built from scratch with robotics and AI, KAIKAKU powers the next generation of QSRs—designed for scale, speed, and margin."
	features={[
		{
			title: "Lower labor, higher throughput",
			description: "FUSICON replaces manual bowl making with robotics-driven assembly—70% fewer staff, consistent quality, and faster line speeds. Built for any cuisine, delivered at unmatched precision."
		},
		{
			title: "Smarter operations with every shift",
			description: "MOSAIC integrates front and back-of-house workflows under a single logic layer. AI-driven tools forecast demand, recommend shift scheduling, and flag revenue drivers in real time."
		},
		{
			title: "Engineered like a rocket company",
			description: "We build core systems in-house and from the ground up to drive over 90% unit-level cost savings. This isn't vendor bundling—it’s precision vertical integration across software, robotics, and AI."
		},
		{
			title: "Designed in London. Proven in-store.",
			description: "KAIKAKU is stress-tested in live QSR environments, not warehouse labs. We run rapid tech iterations in an active location to validate reliability at scale, fast."
		},
		{
			title: "Data that drives better decisions",
			description: "KAIKAKU Intelligence turns raw data into adhesive insights: location-level forecasts, real-time staff productivity, and AI-personalized upsell prompts mapped to macro trends or allergens. Less guesswork, more growth."
		},
		{
			title: "Automation built to transform margins",
			description: "KAIKAKU expands margin by design—more consistent food, reduced overhead, and higher output with leaner teams. For $1B+ chains ready to move from optimization to reinvention."
		}
	]}
/>

<UseCases
	title="Use Cases"
	subtitle="Real-world applications for your business needs"
	useCases={[
		{
			title: "Robotic food assembly at scale",
			description: "Cut prep labor in half and double capacity during peak hours by automating modular menu components with FUSICON.",
			image: "/generated/image-a-bustling-fast-food-restaurant-kitchen-.webp",
			link: {
				href: "/use-cases/robotic-food-assembly",
				label: "Learn more"
			}
		},
		{
			title: "AI-driven kitchen staffing",
			description: "Reduce crew planning overhead and schedule smarter. KAIKAKU Intelligence creates real-time labor forecasts across units to prevent overstaffing or shortages.",
			image: "/generated/image-a-restaurant-manager-in-a-contemporary-f.webp",
			link: {
				href: "/use-cases/ai-driven-kitchen-staffing",
				label: "Learn more"
			}
		},
		{
			title: "Dynamic upsell personalization",
			description: "Boost average check size with AI that cross-sells based on real-time preferences, allergen data, and frequent ordering patterns.",
			image: "/generated/image-customers-at-a-quick-service-restaurant-.webp",
			link: {
				href: "/use-cases/dynamic-upsell-personalization",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction
  title="Ready to run your restaurants leaner and faster?"
  subtitle="See how automation-first operations can transform your margins."
  description="KAIKAKU is the only fully integrated QSR operating system built from scratch with robotics and AI. Schedule a personalized demo to see how we help leading chains cut labor costs, boost throughput, and serve guests better—at scale."
  imageSrc="/generated/image-a-joyful-and-smiling-executive-in-the-qu.webp"
  callsToAction={[
    {
      href: "/request-demo",
      label: "Request a demo",
      variant: "primary"
    },
    {
      href: "/contact",
      label: "Talk to sales",
      variant: "secondary"
    }
  ]}
/>
