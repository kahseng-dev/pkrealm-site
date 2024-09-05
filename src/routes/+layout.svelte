<script lang="ts">
  import Sidebar from "$lib/components/Sidebar.svelte";
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
</script>

<main class="flex text-neutral-400 bg-neutral-900 h-screen">
  <div>
    <Sidebar />
  </div>
  <div class="flex flex-col w-full">
    <div>
      <Header />
    </div>
    <div class="overflow-x-auto">
      <slot></slot>
      <Footer />
    </div>
  </div>
</main>
