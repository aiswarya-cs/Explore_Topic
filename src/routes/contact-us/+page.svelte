<script lang="ts">
  import Breadcrumb from "$lib/components/pages/breadcrumbs.svelte";

const items = [
  { title: "Home", href: "/" },
  { title: "Contact", href: "/contact", active: true }
];
</script>

<!-- Header Section -->
<div
  class="min-h-[400px] w-full bg-gradient-to-tr from-[#13547a] to-[#80d0c7]
 flex flex-col md:flex-row justify-start items-center px-6 md:px-20"
>
  <div>
    <Breadcrumb {items} />
    <h1 class="text-white text-4xl md:text-6xl font-bold mt-3">
      Contact Form
    </h1>
  </div>
</div>

<div
  class="bg-[#f0f8ff] w-full flex flex-col lg:flex-row justify-center p-5 gap-8"
>
  <!-- Form -->
  <div class="w-full lg:w-1/2 px-4 md:px-10">
    <h1 class="text-black text-2xl md:text-4xl py-8 font-bold">
      We'd love to hear from you
    </h1>
    <form action="" class="my-5">
      <div class="flex flex-col md:flex-row justify-between gap-5 mb-8">
        <input
          type="text"
          placeholder="First Name"
          class="border bg-white border-gray-300 w-full md:w-1/2 h-14 p-4 rounded-full"
        />
        <input
          type="text"
          placeholder="Last Name"
          class="border bg-white border-gray-300 w-full md:w-1/2 h-14 p-4 rounded-full"
        />
      </div>

      <div class="w-full mb-8">
        <input
          type="email"
          placeholder="Email"
          class="border bg-white border-gray-300 w-full h-14 p-4 rounded-full"
        />
      </div>

      <div>
        <textarea
          placeholder="Your Message"
          class="border mb-5 bg-white border-gray-300 w-full h-40 p-4 rounded-3xl resize-none"
        ></textarea>
      </div>

      <div class="flex justify-end">
        <button
          type="submit"
          class="w-40 h-12 rounded-full text-lg text-white font-semibold border-2 bg-[#80d0c7] border-[#80d0c7] hover:bg-[#64b5b5] transition"
        >
          Submit
        </button>
      </div>
    </form>
  </div>

  <!-- Map and Info -->
  <div
    class="w-full lg:w-1/2 flex flex-col justify-center items-center lg:items-start"
  >
    <div
      class="w-4/5 rounded-lg overflow-hidden mt-20 shadow-md col-span-1 md:col-span-2 lg:col-span-1"
    >
      <iframe
        title="Map showing Kuravankonam, Thiruvananthapuram, Kerala"
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d7891.460504282523!2d76.94756763928316!3d8.525548626388955!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3b05bbd81cbe1fb9%3A0xceba8598382d5c5e!2sKuravankonam%2C%20Thiruvananthapuram%2C%20Kerala!5e0!3m2!1sen!2sin!4v1745927838539!5m2!1sen!2sin"
        class="w-full h-[250px] border-0"
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </div>
    <div class="mt-5">
      <h1 class="text-center lg:text-start text-3xl font-semibold">
        Topic Listing Center
      </h1>
      <p class="text-center lg:text-start my-5 text-xl">
        Bay St &, Larkin St, San Francisco, CA 94109, United States
      </p>
    </div>
  </div>
</div>
