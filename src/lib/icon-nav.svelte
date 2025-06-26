<script>
    import { Button } from "$lib/components/ui/button/index.js";
    import logoLight from "$lib/images/SPECTRA_logo_light.png?enhanced";
    import logoDark from "$lib/images/SPECTRA_logo_dark.png?enhanced";
</script>

<Button variant="link" href="/" class="hidden md:flex items-center">
    <enhanced:img src="{logoLight}" alt="Spectra CE EU logo" class="block dark:hidden h-8 w-full hover:opacity-80" />
    <enhanced:img src="{logoDark}" alt="Spectra CE EU logo" class="hidden dark:block h-8 w-full hover:opacity-80" />
</Button>