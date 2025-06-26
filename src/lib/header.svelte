<script lang="ts">
    import IconNav from '$lib/icon-nav.svelte'
    import MainNav from '$lib/main-nav.svelte'
    // import MobileNav from './mobile-nav.svelte'
</script>

<header class="bg-background fixed top-0 p-2 z-50 w-full">
    <section class="flex mx-auto justify-between items-center max-w-screen-xl">
        <div class="flex">
            <IconNav />
            <!-- <MobileNav /> -->
        </div>
        <div class="hidden md:flex items-center space-x-1">
            <MainNav />
        </div>
    </section>
</header>
