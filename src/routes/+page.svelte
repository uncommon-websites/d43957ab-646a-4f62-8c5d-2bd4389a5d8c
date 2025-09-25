<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<Hero
	title="Transform 3-hour operational tasks into 3-minute checks"
	subtitle="Record your workflow once, and let MindfulScale automate it across any website or application. Scale your team's productivity without hiring more staff."
	imageSrc="/generated/image-candid-photograph-of-a-professional-oper.webp"
	centered={false}
/>
<LogoScroller 
	label="Trusted by industry leaders"
	logoUrls={[
		'https://cdn.brandfetch.io/shopify.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/hubspot.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/mailchimp.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/intercom.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="Show it once. Let us handle it forever."
	text="MindfulScale turns hours of reports and data entry into minutes—by watching you do it once and repeating it across any site or tool, automatically. Just click through your workflow like you always do, and we'll record your actions and run them for you, every time, without extra setup or integrations."
/>

<Testimonials
	testimonials={[
		{
			name: "Maria Elena Rodriguez",
			position: "Operations Manager",
			company: "TechFlow Industries",
			quote:
				"MindfulScale transformed our daily reporting process from 3 hours to 3 minutes. We now save 15 hours weekly on data entry, allowing my team to focus on strategic initiatives instead of manual tasks.",
			image: "/generated/image-professional-headshot-of-maria-elena-rod.webp"
		},
		{
			name: "David Chen",
			position: "Director of Operations",
			company: "GrowthScale Solutions",
			quote:
				"Before MindfulScale, our team spent $24,000 monthly on overtime for manual processes. Now we've eliminated that cost entirely while reducing errors by 94% and improving data accuracy across all our systems.",
			image: "/generated/image-professional-headshot-of-david-chen-expe.webp"
		},
		{
			name: "Priya Patel",
			position: "Operations Executive",
			company: "Velocity Logistics",
			quote:
				"The risk reduction has been game-changing. MindfulScale eliminated human errors in our compliance reporting, saving us from potential $50,000 fines while scaling our operations from 50 to 150 employees seamlessly.",
			image: "/generated/image-professional-headshot-of-priya-patel-acc.webp"
		}
	]}
/>

<Features
	title="Why operations managers choose MindfulScale"
	subtitle="Transform your team's productivity without the complexity of traditional automation tools"
	features={[
		{
			title: "Zero integrations required",
			description: "Works with any website or application instantly, eliminating months of setup time that competitors like Zapier require."
		},
		{
			title: "Record once, automate everywhere",
			description: "Simply demonstrate your workflow once and MindfulScale replicates it across all your systems automatically."
		},
		{
			title: "Transform 3-hour tasks into 3-minute checks",
			description: "Turn your most time-consuming operational processes into quick verification steps, freeing your team for strategic work."
		},
		{
			title: "Scale without hiring",
			description: "Handle growing operational demands with your existing team by automating the manual work that's slowing you down."
		},
		{
			title: "Universal browser automation",
			description: "Our click-mimicking technology works on any web platform without requiring APIs or technical integrations."
		},
		{
			title: "Built for operations managers",
			description: "Designed specifically for the 15+ hours of weekly manual tasks that operations teams at growing SMBs face every day."
		}
	]}
/>
<AboutTeaser />
<CallToAction
	title="Skip the 3-hour task. Do it in 3 minutes instead."
	subtitle="Start saving hours this week"
	description="Show us your workflow once—MindfulScale handles it from there. No integrations, no dev time, and no more copy-paste. Just accurate, repeatable automation that runs anywhere your team works online."
	imageSrc="/generated/image-candid-photograph-of-a-professional-oper.webp"
	callsToAction={[
		{
			href: "/",
			label: "Book live demo",
			variant: "primary"
		},
		{
			href: "/about",
			label: "Learn more",
			variant: "secondary"
		}
	]}
/>
