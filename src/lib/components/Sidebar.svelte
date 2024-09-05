<script lang="ts">
  import BrandName from "$lib/components/BrandName.svelte";
  import { fade } from "svelte/transition";

  const fadeIn = {
    delay: 100,
    duration: 200,
  };

  let isExpanded = false;
</script>

<aside
  class="h-screen border-r border-neutral-700 bg-neutral-950"
  class:expanded={isExpanded}
>
  <div class="flex h-16 items-center pl-4 justify-between">
    {#if isExpanded}
      <div in:fade={fadeIn}>
        <BrandName />
      </div>
    {/if}
    <button
      class:buttonUnexpanded={!isExpanded}
      class="flex h-6 w-6 bg-neutral-900 rounded-full border border-neutral-700 mr-4 justify-center items-center"
      on:click={() => (isExpanded = !isExpanded)}
    >
      {#if isExpanded}
        <iconify-icon
          height="0.8em"
          width="0.8em"
          icon="flowbite:angle-right-outline"
        />
      {:else}
        <iconify-icon
          height="0.8em"
          width="0.8em"
          icon="flowbite:angle-left-outline"
        />
      {/if}
    </button>
  </div>
  <section class="flex flex-col mt-8">
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:user-solid"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>My Account</span>{/if}
    </a>
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:arrow-down-to-bracket-outline"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>Downloads</span>{/if}
    </a>
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:arrow-down-to-bracket-outline"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>Pokédex</span>{/if}
    </a>
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:annotation-solid"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>Forum</span>{/if}
    </a>
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:question-circle-solid"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>Support</span>{/if}
    </a>
    <a
      href="/"
      class="flex items-center gap-4 p-4 hover:bg-neutral-800 hover:text-neutral-50"
    >
      <iconify-icon
        class="pt-0.5"
        height="1.5em"
        width="1.5em"
        icon="flowbite:discord-solid"
      />
      {#if isExpanded}
        <span in:fade={fadeIn}>Discord</span>{/if}
    </a>
  </section>
</aside>

<style>
  .expanded {
    width: 16rem;
  }

  .buttonUnexpanded {
    position: relative;
    left: 1.75rem;
  }
</style>
