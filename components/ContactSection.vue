<script setup lang="ts"></script>

<template>
  <section id="contact">
    <div class="mt-16 text-center">
      <h1 class="text-4xl lg:text-5xl font-bold lg:tracking-tight">
        <span class="text-primary poppins"> Contact</span>
        me
      </h1>
    </div>
    <div
      class="bg-[radial-gradient(ellipse_at_center,_var(--tw-gradient-stops))] from-primary-900 to-transparent rounded-full h-80 w-80 z-0 blur-lg absolute top-3/4 -left-4 transform -translate-x-1/2 -translate-1/2"></div>
    <div class="grid md:grid-cols-2  py-24 gap-4 relative">
      <div class=" flex flex-col !items-center">
        <h2 class="text-xl font-bold my-2 md:!mb-2 md:!mt-32 ">Let's Do Something Incredible Together</h2>
        <!-- <p class="mb-4 max-w-md">
          Don't hesitate to send me a message or an e-mail. <br />I will get
          back to you as fast as I can.
        </p> -->
        <div class="flex flex-col md:flex-row justify-around  gap-4 text-xl">
          <div class="flex flex-row gap-x-6">
            <a
              href="https://www.linkedin.com/in/omar-elbakry-495848250/"
              target="_blank"
              class="hover:text-primary"
              aria-label="LinkedIn Profile">
              Linkedin
              <Icon
                name="fa6-brands:linkedin"
                class="size-8" />
            </a>
          </div>
          <div class="flex flex-row items-center">
            <a
              href="mailto:omarbss15@gmail.com"
              class="text-base md:text-lg font-bold hover:text-primary">
              <Icon
                name="fa6-solid:envelope"
                class="size-6" />
              omarbss15@gmail.com</a
            >
          </div>
          <div class="flex flex-row items-center">
<a
  href="https://wa.me/201096126337?text=Hello, I would like to inquire about..."
  target="_blank"
  class="text-base md:text-lg font-bold hover:text-primary">
  <Icon
    name="logos:whatsapp-icon"
    class="size-6" />
  01096126337
</a>
</div>
        </div>
      </div>
      <div>
        <form class="flex flex-col">
          <div class="mb-6">
            <label
              for="email"
              class="block mb-2 text-sm font-medium"
              >Your email</label
            ><input
              type="email"
              id="email"
              required
              class="bg-white/10 border border-primary text-sm outline-none rounded-md block w-full p-3 focus:ring-2 ring-primary"
              placeholder="example@gmail.com"
              name="email" />
          </div>
          <div class="mb-6">
            <label
              for="subject"
              class="block text-sm mb-2 font-medium"
              >Subject</label
            ><input
              type="text"
              id="subject"
              required
              class="bg-white/10 border border-primary text-sm outline-none rounded-md block w-full p-3 focus:ring-2 ring-primary"
              placeholder="Subject of your message"
              name="subject" />
          </div>
          <div class="mb-6">
            <label
              for="message"
              class="block text-sm mb-2 font-medium"
              >Message</label
            ><textarea
              name="message"
              id="message"
              class="bg-white/10 border border-primary text-sm outline-none rounded-md block w-full p-3 focus:ring-2 ring-primary"
              placeholder="Let's talk about..."></textarea>
          </div>
          <button
            type="submit"
            class="bg-primary text-white hover:bg-blue-300 font-extrabold py-2.5 px-5 rounded-lg w-full">
            Send Message
          </button>
        </form>
      </div>
    </div>
  </section>
</template>
