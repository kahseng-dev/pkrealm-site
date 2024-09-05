<script lang="ts">
  import BrandName from "$lib/components/BrandName.svelte";
  import { fade } from "svelte/transition";

  const fadeIn = {
    delay: 100,
    duration: 200,
  };

  let isExpanded = true;
</script>

<navbar class:expanded={isExpanded}>
  <div
    class="flex h-16 w-full pl-8 gap-4 bg-neutral-950 border-b border-neutral-700 items-center"
  >
    <button
      class="flex px-1 bg-neutral-900 rounded border border-neutral-700 justify-center items-center"
      on:click={() => (isExpanded = !isExpanded)}
    >
      {#if isExpanded}
        <iconify-icon height="2em" width="2em" icon="flowbite:bars-outline" />
      {:else}
        <iconify-icon height="2em" width="2em" icon="flowbite:close-outline" />
      {/if}
    </button>
    <BrandName />
  </div>
  {#if !isExpanded}
    <section class="fixed w-full bg-neutral-950 border-b border-neutral-700">
      <div class="flex gap-4 p-4 items-center">
        <button in:fade={fadeIn}>Log In</button>
        <button in:fade={fadeIn}>Sign Up</button>
      </div>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:user-solid"
        />
        <span in:fade={fadeIn}>My Account</span>
      </a>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:arrow-down-to-bracket-outline"
        />
        <span in:fade={fadeIn}>Downloads</span>
      </a>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:arrow-down-to-bracket-outline"
        />
        <span in:fade={fadeIn}>Pokédex</span>
      </a>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:annotation-solid"
        />
        <span in:fade={fadeIn}>Forum</span>
      </a>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:question-circle-solid"
        />
        <span in:fade={fadeIn}>Support</span>
      </a>
      <a
        href="/"
        class="flex gap-4 p-4 items-center hover:bg-neutral-800 hover:text-neutral-50"
      >
        <iconify-icon
          class="pt-0.5"
          height="1.5em"
          width="1.5em"
          icon="flowbite:discord-solid"
        />
        <span in:fade={fadeIn}>Discord</span>
      </a>
    </section>
  {/if}
</navbar>
