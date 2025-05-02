<script lang="ts">
  interface Cards {
    name: string;
    paragraph: string;
    Image: string;
  }

  const designCards: Cards[] = [
    {
      name: "Web Design",
      paragraph:
        "Topic Listing includes home, listing, detail and contact pages. Feel free to modify this template for your custom websites.",
      Image: "images/designs/design1.png",
    },
    {
      name: "Graphics",
      paragraph:
        "Visit TemplateMo website to download free CSS templates. Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
      Image: "images/designs/design2.png",
    },
    {
      name: "Logo Design",
      paragraph:
        "Lorem ipsum dolor sit, amet consectetur adipisicing elit.  Feel free to modify this template for your custom websites.",
      Image: "images/designs/design3.png",
    },
  ];
</script>

<div
  class="min-h-[400px] w-full bg-gradient-to-tr from-[#13547a] to-[#80d0c7]
 flex flex-col md:flex-row justify-start items-center px-6 md:px-20"
>
  <div>
    <h1 class="text-white text-4xl md:text-6xl font-bold pt-40">
      Topics Listing
    </h1>
  </div>
</div>

<div class="flex flex-col gap-5 justify-center items-center mx-8">
  <div class="w-full flex flex-col justify-center items-center">
    <h1 class="text-4xl mt-8 font-bold">Popular Topics</h1>

    {#each designCards as design}
      <div
        class="bg-white w-full md:w-3/4 lg:w-2/3 xl:w-1/2 rounded-2xl shadow-2xl p-8
        my-8 flex flex-col md:flex-row gap-8 items-center relative"
      >
        <!-- Count Badge -->
        <div
          class="absolute top-4 right-4 bg-sky-500 text-white text-sm font-bold px-3 py-1 rounded-lg"
        >
          23
        </div>

        <!-- Image -->
        <img
          src={design.Image}
          alt={design.name}
          class="w-40 h-40 object-contain"
        />

        <!-- Text Content -->
        <div class="flex-1 text-left">
          <h2 class="text-2xl font-bold mb-2">{design.name}</h2>
          <p class="text-gray-600 mb-6">
            {design.paragraph}
          </p>
          <button
            class="bg-teal-400 text-white font-semibold px-5 py-2 rounded-full hover:bg-teal-500 transition"
          >
            Learn More
          </button>
        </div>
      </div>
    {/each}
  </div>
</div>
