<script lang="ts">
    import { Button } from '$lib/components/ui/button/index.js';
    import BeReadyLogo from '$lib/images/Be Ready (RGB Alpha).png?enhanced';
</script>

<section class="bg-background">
	<div class="grid px-4 py-8 lg:grid-cols-12 lg:gap-8 lg:py-16 xl:gap-0">
		<div class="mr-auto place-self-center lg:col-span-7">
			<h1
				class="mb-4 max-w-2xl text-xl text-foreground leading-none font-bold md:text-2xl xl:text-3xl"
			>
				BeReady e-learning platform
			</h1>
			<p
				class="mb-6 max-w-2xl font-light text-foreground md:text-lg lg:mb-8 lg:text-xl"
			>
				BeReady e-learning platform containes courses on urban heat island vunerability 
                and risk assessment developed as the result of the implementation of the BeReady INTERREG Danube Region project 
                co-funded by the European Union
			</p>
			<Button variant="outline" href="/about-spectra">About Spectra CE EU</Button>
			<Button class="ml-2">About BeReady Project</Button>
		</div>
		<div class="hidden lg:col-span-5 lg:mt-0 lg:flex">
			<enhanced:img
				src={BeReadyLogo}
				alt="BeReady Project logo"
			/>
		</div>
	</div>
</section>
