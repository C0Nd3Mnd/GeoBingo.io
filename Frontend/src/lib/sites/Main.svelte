<script>
  import Carousel from "$lib/components/Carousel.svelte";
  import Discord from "$lib/components/Discord.svelte";
  import Login from "$lib/components/Login.svelte";
  import Logo from "$lib/components/Logo.svelte";
  import Socials from "$lib/components/Socials.svelte";
  import StreamerFrontPage from "$lib/components/StreamerFrontPage.svelte";
  import YoutubeVideo from "$lib/components/YoutubeVideo.svelte";
  import { api } from "$lib/js/api";
  import DonationPopup from "$lib/components/DonationPopup.svelte";
  // let events = [
  // 	{
  // 		image: 'ukraine.jpg.webp',
  // 		link: 'https://bank.gov.ua/en/news/all/natsionalniy-bank-vidkriv-spetsrahunok-dlya-zboru-koshtiv-na-potrebi-armiyi'
  // 	},
  // 	{
  // 		image: 'FMYn0keWUAABtRY.png',
  // 		link: 'https://donate.redcrossredcrescent.org/ua/donate/~my-donation'
  // 	}
  // ];
  let events = [
    {
      image: "wikiparty.png",
      link: "https://wikiparty.org",
    },
  ];
  let disabled = false;
</script>

<div class="min-h-screen">
  <div class="flex justify-center items-center p-2">
    <img class=" rounded-md back shadow-2xl w-1/4" src="cover.png" alt="" />
  </div>

  <div class="w-full flex flex-col md:flex-row p-2 justify-center items-center">
    <div class="p-2 flex items-center justify-center">
      {#if $api?.player}
        <Login />
        <!-- {:else}
		loading -->
      {/if}
    </div>
  </div>
</div>
