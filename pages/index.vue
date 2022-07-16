<template>
  <div
    class="h-full min-h-screen flex flex-col gap-44 mx-auto max-w-screen-2xl py-20 px-24 bg-[#162030] font-poppins"
  >
    <div class="flex flex-col gap-4 -my-14">
      <h1
        class="font-bold text-7xl bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500"
      >
        WEBIHOO
      </h1>
      <p
        class="text-2xl text-[#344257] hover:text-pink-400 ease-in-out duration-300"
      >
        Webinar Platform to educate others.
      </p>
    </div>

    <div class="flex items-center justify-center">
      <div class="flex flex-col gap-10">
        <h1 class="text-4xl text-[#344257] hover:">Sponsors</h1>
        <div class="flex gap-10">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 400 298"
            class="group duration-300 ease-in-out"
          >
            <g fill="none" fill-rule="nonzero">
              <path
                class="group-hover:fill-[#108775] duration-300 ease-in-out"
                fill="#344257"
                d="M227.92099 82.07407l-13.6889 23.7037-46.8148-81.08641L23.7037 273.58025h97.3037c0 13.0912 10.61252 23.7037 23.70371 23.7037H23.70371c-8.46771 0-16.29145-4.52017-20.5246-11.85382-4.23315-7.33366-4.23272-16.36849.00114-23.70174L146.89383 12.83951c4.23415-7.33433 12.0596-11.85252 20.5284-11.85252 8.46878 0 16.29423 4.51819 20.52839 11.85252l39.97037 69.23456z"
              />
              <path
                class="group-hover:fill-[#2F495E] duration-300 ease-in-out"
                fill="#344257"
                d="M331.6642 261.7284l-90.05432-155.95062-13.6889-23.7037-13.68888 23.7037-90.04445 155.95061c-4.23385 7.33325-4.23428 16.36808-.00113 23.70174 4.23314 7.33365 12.05689 11.85382 20.5246 11.85382h166.4c8.46946 0 16.29644-4.51525 20.532-11.84955 4.23555-7.3343 4.23606-16.37123.00132-23.706h.01976zM144.7111 273.58024L227.921 129.48148l83.19012 144.09877h-166.4z"
              />
              <path
                class="group-hover:fill-[#108775] duration-300 ease-in-out"
                fill="#344257"
                d="M396.04938 285.4321c-4.23344 7.33254-12.05656 11.85185-20.52345 11.85185H311.1111c13.0912 0 23.7037-10.6125 23.7037-23.7037h40.66173L260.09877 73.74815l-18.4889 32.02963-13.68888-23.7037L239.5753 61.8963c4.23416-7.33433 12.0596-11.85252 20.5284-11.85252 8.46879 0 16.29423 4.51819 20.52839 11.85252l115.41728 199.8321c4.23426 7.33395 4.23426 16.36975 0 23.7037z"
              />
            </g>
          </svg>

          <svg
            class="group duration-300 ease-in-out"
            xmlns="http://www.w3.org/2000/svg"
            version="1.1"
            viewBox="0 0 261.76 226.69"
          >
            <g transform="matrix(1.3333 0 0 -1.3333 -76.311 313.34)">
              <g transform="translate(178.06 235.01)">
                <path
                  class="group-hover:fill-[#41b883] duration-300 ease-in-out"
                  d="m0 0-22.669-39.264-22.669 39.264h-75.491l98.16-170.02 98.16 170.02z"
                  fill="#344257"
                />
              </g>
              <g transform="translate(178.06 235.01)">
                <path
                  class="group-hover:fill-[#34495e] duration-300 ease-in-out"
                  d="m0 0-22.669-39.264-22.669 39.264h-36.227l58.896-102.01 58.896 102.01z"
                  fill="#344257"
                />
              </g>
            </g>
          </svg>
        </div>
      </div>
    </div>
    <div
      v-for="(web, idx) in webinar"
      :key="idx"
      class="flex flex-col-reverse lg:flex-row w-full bg-white dark:bg-gray-800 shadow rounded-xl"
    >
      <div class="w-full lg:w-1/2">
        <div
          aria-label="card"
          class="pt-4 lg:pt-6 pb-4 lg:pb-6 pl-4 lg:pl-6 pr-4 lg:pr-6"
        >
          <div
            class="flex justify-between items-center lg:items-start flex-row-reverse lg:flex-col"
          >
            <h4
              class="text-base text-gray-700 dark:text-gray-600 tracking-normal leading-4"
            >
              {{ web.jam }}
            </h4>
            <h4
              class="lg:mt-3 text-gray-600 dark:text-gray-400 text-base font-normal"
            >
              {{ web.Tanggal }}
            </h4>
          </div>
          <a
            tabindex="0"
            class="focus:outline-none focus:underline focus:text-gray-500 hover:text-gray-500 cursor-pointer text-gray-800 dark:text-gray-100"
            ><h2
              class="mt-4 mb-2 tracking-normal text-xl lg:text-2xl font-bold"
            >
              {{ web.Judul }}
            </h2></a
          >
          <p
            class="text-justify mb-6 font-normal text-gray-600 dark:text-gray-400 text-sm tracking-normal w-11/12 lg:w-11/12"
          >
            {{ web.Deskripsi }}
          </p>
          <div
            class="flex lg:items-end items-start flex-col lg:flex-row justify-start lg:justify-between"
          >
            <div class="flex justify-between items-end">
              <div class="flex flex-col">
                <h4 class="text-gray-400 text-sm">Speaker</h4>
                <h4 class="text-gray-400">{{ web.Speaker }}</h4>
              </div>
            </div>
            <button
              class="text-gray-600 dark:text-gray-400 focus:outline-none hover:text-pink-500 focus:text-pink-500 mt-4 lg:mt-0 ml-0 lg:ml-12 flex items-end justify-end"
            >
              <span class="mr-1">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="icon icon-tabler icon-tabler-map-pin"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  stroke-width="1.5"
                  stroke="currentColor"
                  fill="none"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path stroke="none" d="M0 0h24v24H0z" />
                  <circle cx="12" cy="11" r="3" />
                  <path
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 0 1 -2.827 0l-4.244-4.243a8 8 0 1 1 11.314 0z"
                  />
                </svg>
              </span>
              <p class="text-sm tracking-normal font-normal text-center">
                {{ web.Lokasi }}
              </p>
            </button>
          </div>
        </div>
        <div
          class="px-5 lg:px-5 md:px-10 py-3 lg:py-4 flex flex-row items-center justify-between border-t border-gray-300"
        >
          <div class="flex items-center">
            <button
              aria-label="save"
              class="focus:outline-none focus:text-gray-400 hover:text-gray-400 text-gray-600 dark:text-gray-400 cursor-pointer mr-4"
            >
              <svg
                class="feather feather-bookmark"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path
                  d="M19 21l-7-5-7 5V5a2 2 0 0 1 2-2h10a2 2 0 0 1 2 2z"
                ></path>
              </svg>
            </button>
            <button
              aria-label="share"
              class="text-indigo-700 dark:text-indigo-600 hover:text-indigo-500 focus:outline-none focus:text-indigo-500 cursor-pointer"
            >
              <svg
                class="feather feather-share-2"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="1.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <circle cx="18" cy="5" r="3"></circle>
                <circle cx="6" cy="12" r="3"></circle>
                <circle cx="18" cy="19" r="3"></circle>
                <line x1="8.59" y1="13.51" x2="15.42" y2="17.49"></line>
                <line x1="15.41" y1="6.51" x2="8.59" y2="10.49"></line>
              </svg>
            </button>
          </div>
        </div>
      </div>
      <div
        class="relative w-full h-64 lg:h-auto lg:w-1/2 rounded-t lg:rounded-t-none lg:rounded-r inline-block"
      >
        <img
          class="w-full h-full absolute inset-0 object-cover rounded-t lg:rounded-r lg:rounded-t-none"
          :src="web.Gambar"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",

  data() {
    return {
      webinar: [
        {
          jam: "12.00 PM",
          Tanggal: "23 December, Sunday",
          Judul: "How can we solve the antibiotic resistance crisis?",
          Deskripsi:
            "Antibiotics: behind the scenes, they enable much of modern medicine. We use them to cure infectious diseases, and to safely facilitate everything from surgery to chemotherapy to organ transplants. But we've stopped discovering new ones and we're at risk of losing them forever. How did we get into this situation? Gerry Wright shares what we can do about antibiotic resistance",
          Speaker: "Addison Anderson",
          Lokasi: "DKI Jakarta, Indoensia",
          Gambar:
            "https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/663f8b9a-536a-4b58-b81b-952e8d627086/anti5y.jpg?u%5Br%5D=2&u%5Bs%5D=0.5&u%5Ba%5D=0.8&u%5Bt%5D=0.03&quality=80&w=1080",
        },

        {
          jam: "11.00 PM",
          Tanggal: "19 January, Monday",
          Judul: "The secret to lifelong friendship",
          Deskripsi:
            "Tough conversations, lasting memories, shouldering loss together ... These speakers embody the highs and lows of true friendship",
          Speaker: "Paul Guge & Ben Simmons",
          Lokasi: "Surabaya, Indoensia",
          Gambar:
            "https://pi.tedcdn.com/r/talkstar-assets.s3.amazonaws.com/production/playlists/playlist_633/b8cefd1b-2908-46f8-89ee-b08a7e4e8b89/secret_to_lifelong_friendship-2000x2000.jpg?u%5Br%5D=2&u%5Bs%5D=0.5&u%5Ba%5D=0.8&u%5Bt%5D=0.03&quality=80&w=1920",
        },

        {
          jam: "09.00 AM",
          Tanggal: "07 July, Thursday",
          Judul: "What comes after tragedy? Forgiveness",
          Deskripsi:
            "On one awful night in 1995, Ples Felix's 14-year-old grandson murdered Azim Khamisa's son in a gang initiation fueled by drugs, alcohol and a false sense of belonging. The deadly encounter sent Khamisa and Felix down paths of deep meditation, to forgive and to be forgiven -- and in an act of bravery and reconciliation, the two men met and forged a lasting bond. Together, they've used their story as an outline for a better, more merciful society, where victims of tragedy can grow and heal. Prepare to be moved by their unimaginable story. 'Peace is possible,' Khamisa says. 'How do I know that? Because I am at peace.'",
          Speaker: "Plesfelix & Azimkhamisa",
          Lokasi: "Iowa , United States",
          Gambar:
            "https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/b495c23a-a29f-4cee-a630-49bb7a82c487/AzimKhamisaandPlesFelix_2017W-embed.jpg?u%5Br%5D=2&u%5Bs%5D=0.5&u%5Ba%5D=0.8&u%5Bt%5D=0.03&quality=80&w=640",
        },

        {
          jam: "15.00 PM",
          Tanggal: "07 May, Wednesday",
          Judul: "What Wikipedia teaches us about balancing truth and beliefs",
          Deskripsi:
            "Even with public trust at an all-time low, Wikipedia continues to maintain people's confidence. How do they do it? Former CEO of Wikimedia Foundation Katherine Maher delves into the transparent, adaptable and community-building ways the online encyclopedia brings free and reliable information to the public -- while also accounting for bias and difference of opinion. 'The seeds of our disagreement can actually become the roots of our common purpose,' she says.",
          Speaker: "Katherine Maher",
          Lokasi: "Ottawa, Canada",
          Gambar:
            "https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/c70e2aa0-1b3c-4ddc-9a19-9a9c3f15a73f/KatherineMaher_2021-embed.jpg?u%5Br%5D=2&u%5Bs%5D=0.5&u%5Ba%5D=0.8&u%5Bt%5D=0.03&quality=80&w=640",
        },

        {
          jam: "17.00 PM",
          Tanggal: "19 June, Wednesday",
          Judul: "How to fix the 'bug' in the net-zero code",
          Deskripsi:
            "Lucas Joppa, Microsoft's first chief environmental officer, thinks about climate change through the lens of coding, and he says the world's current net-zero approach simply won't compute. So how do we create a system that actually accounts for all the world's carbon emissions -- and helps us get to zero (as in zero additional carbon added to the atmosphere by 2050)? Joppa shares three 'bugs' in our current net-zero code, a four-point plan for fixing them – and how logic can help us change the current course of climate change.",
          Speaker: "Lucas Joppa",
          Lokasi: "Marina Bay Sands, Singapore",
          Gambar:
            "https://pi.tedcdn.com/r/talkstar-photos.s3.amazonaws.com/uploads/137b19ec-ce4d-4b71-a2f2-6de4b1c5f2ec/LucasJoppa_2021T-1350x675.jpg?u%5Br%5D=2&u%5Bs%5D=0.5&u%5Ba%5D=0.8&u%5Bt%5D=0.03&quality=80&w=640",
        },
      ],
    };
  },
};
</script>
