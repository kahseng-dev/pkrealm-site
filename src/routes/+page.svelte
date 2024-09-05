<script lang="ts">
  import "./globals.css";
  import Logo from "$lib/components/Logo.svelte";
</script>

<div class="p-8">
  <Logo />
  <p class="mt-2">A fan made online CO-OP Pokémon adventure</p>
  <article class="mt-8 flex flex-col gap-8">
    <section class="flex justify-between gap-8">
      <div class="w-1/2">
        <h2 class="text-3xl text-neutral-50 font-bold">
          Collect, Catch, and Level Up
        </h2>
        <p class="text-sm mt-2">Description</p>
      </div>
      <div class="w-1/2 h-64 bg-red-400"></div>
    </section>
    <section class="flex justify-between gap-8">
      <div class="w-1/2">
        <h2 class="text-3xl text-neutral-50 font-bold">Play Together</h2>
        <p class="text-sm mt-2">Description</p>
      </div>
      <div class="w-1/2 h-64 bg-red-400 md:order-first"></div>
    </section>
    <section class="flex justify-between gap-8">
      <div class="w-1/2">
        <h2 class="text-3xl text-neutral-50 font-bold">Join a Community</h2>
        <p class="text-sm mt-2">Description</p>
      </div>
      <div class="w-1/2 h-64 bg-red-400"></div>
    </section>
  </article>
</div>
