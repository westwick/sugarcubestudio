<template>
  <section>
    <img src="@/assets/images/graddiv.jpg" class="w-full h-4 md:h-8" />
  </section>
  <footer class="bg-gray-900 text-white py-12">
    <div class="container mx-auto px-4 lg:px-0">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Section 1 -->
        <div>
          <h3 class="text-lg font-semibold mb-4">About Sugar Cube Studio</h3>
          <p class="text-sm text-gray-300 mb-4 leading-loose">
            We are an indie software company dedicated to creating innovative
            applications and games that resonate deeply with our audience.
          </p>
          <p class="text-sm text-gray-300 mb-4 leading-loose">
            Through art, design, and immersive storytelling, we aim to fill the
            gaps in the industry by crafting experiences that are not just
            unique, but transformative.
          </p>
          <p class="text-sm text-gray-300 leading-loose">
            Our products celebrate culture and creativity, bringing people
            together through shared moments of discovery and connection.
          </p>
        </div>

        <!-- Section 2 (with Button) -->
        <div>
          <h3 class="text-lg font-semibold mb-4">Stay up to date</h3>
          <p class="text-sm text-slate-300 mb-4 leading-loose">
            Sign up for our mailing list to receive updates on new products,
            exclusive offers, and important announcements. Get the latest on
            everything we're working on, directly in your inbox.
          </p>

          <div class="text-center mt-8 mb-4">
            <button
              class="gradient-button-yellow text-blue-950 font-semibold py-2 px-6 rounded transition-all duration-300"
            >
              Join the mailing list
            </button>
          </div>
        </div>

        <!-- Section 3 -->
        <div>
          <h3 class="text-lg font-semibold mb-4">Follow us</h3>
          <p class="text-sm text-slate-300 mb-4 leading-loose">
            Connect with us on social media. Follow for our latest updates,
            sneak peeks, and announcements.
          </p>
          <ul class="flex flex-col">
            <li class="mb-4">
              <Twitter class="inline mr-2" />
              <a
                href="https://x.com/sugarcubestudio"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                x.com/sugarcubestudio
              </a>
            </li>
            <li class="mb-4">
              <Instagram class="inline mr-2" />
              <a
                href="https://instagram.com"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                instagram.com/sugarcubestudio
              </a>
            </li>
            <li>
              <Youtube class="inline mr-2" />
              <a
                href="https://youtube.com"
                target="_blank"
                class="text-gray-400 hover:text-white transition duration-200"
              >
                youtube.com/@sugarcubestudio
              </a>
            </li>
          </ul>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="mt-12 text-center text-slate-600 text-sm">
        <p>&copy; {{ new Date().getFullYear() }} Sugar Cube Studio</p>
        <p>Terms of Service | Privacy Policy</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Twitter, Youtube, Instagram } from "lucide-vue-next";
</script>

<style>
footer {
  background: linear-gradient(
    195deg,
    #121328 0%,
    #121328 23%,
    #181f30 40%,
    #181f30 60%,
    #121328 85%,
    #121328 100%
  );
}
</style>
