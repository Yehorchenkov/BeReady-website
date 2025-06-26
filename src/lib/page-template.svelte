<script>
  let { children } = $props();
</script>

<div class="prose max-w-4xl text-justify mx-auto p-6 dark:prose-invert">
  {@render children()}
</div>