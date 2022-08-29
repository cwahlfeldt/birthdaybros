<script>
  /** @type {import('./$types').PageData} */
  export let data;
</script>

<main>
  <div class="container mx-auto px-10 h-screen font-sans flex justify-center flex-col items-start max-w-7xl">
    <h1 class="font-heading font-semibold text-10xl leading-tighter mb-2 text-slate-700">
      { @html data.title }
    </h1>
    <p class="text-xl italic w-full font-serif text-slate-500">
      coming soon...
    </p>
  </div>
</main>
