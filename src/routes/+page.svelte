<script lang="ts">
  import "iconify-icon";

  const socials = [
    {
      platform: "youtube",
      href: "https://www.youtube.com/@dunderligan_ow",
    },
    {
      platform: "twitter",
      href: "https://x.com/dunderligan",
    },
    {
      platform: "discord",
      href: "https://discord.gg/74Y9B7dTNN",
    },
    {
      platform: "twitch",
      href: "https://www.twitch.tv/dunderligan_ow",
    },
    {
      platform: "tiktok",
      href: "https://www.tiktok.com/@dunderligan_ow",
    },
    {
      platform: "github",
      href: "https://github.com/Dunderligan",
    },
  ];
</script>

<div
  class="w-full h-screen flex flex-col items-center justify-center p-6 mx-auto max-w-xl text-center"
>
  <img class="size-32" src="/logo.png" alt="Dunderligan" />

  <h1 class="font-bold text-3xl text-gray-800 mb-8 -mt-2">
    Den här sidan är under konstruktion!
  </h1>
  <div>
    <div class="font-medium text-gray-600">
      Medan du väntar får du gärna ta en titt på följande länkar:
    </div>
    <div class="flex items-center gap-4 justify-center">
      {#each socials as { platform, href }}
        <a
          title={platform}
          {href}
          class="text-3xl text-fuchsia-800 mt-4 hover:text-fuchsia-900 transform hover:scale-110 transition-all"
          ><iconify-icon icon="ph:{platform}-logo"></iconify-icon></a
        >
      {/each}
    </div>
  </div>
</div>

<style>
  :global(body) {
    backdrop-filter: blur(1px) grayscale();
    background-image: radial-gradient(
        white 10%,
        rgba(100%, 100%, 100%, 90%) 80%
      ),
      url("/topographic-bg.jpg");
    object-fit: cover;
  }
</style>
