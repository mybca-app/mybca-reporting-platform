<script lang="ts">
	import BusArrivalSection from "./BusArrivalSection.svelte";
</script>

<svelte:head>
    <title>Open Reporting Platform • myBCA</title>
    <meta name="description" content="The Open Reporting Platform provides fast access to public data collected by myBCA's systems. myBCA is the student-developed, all-in-one app for students of the Bergen County Academies.">
</svelte:head>

<section class="space-y-5">
	<h1 class="font-serif text-3xl font-bold">Welcome to the myBCA Open Reporting Platform.</h1>
	<p class="text-lg">
		The Open Reporting Platform provides fast access to public data collected by myBCA's systems.
		You can browse through the available data and download reports easily.
	</p>
</section>

<BusArrivalSection />