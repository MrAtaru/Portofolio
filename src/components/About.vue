<script setup>
import Navbar from "./Navbar.vue";
</script>

<template>
  <div>
    <div>
      <Navbar />
    </div>

    <section
      class="bg-white dark:bg-gray-900 bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern.svg')] dark:bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern-dark.svg')]"
    >
      <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 z-10 relative">
        <div class="grid grid-cols-1 gap-6 sm:grid-cols-2">
          <img class="h-auto max-w-md ml-auto rounded-lg" src="/foto_gueh.jpg" alt="image description" />
          <div class="col-span-1">
            <h2 class="text-4xl font-thin dark:text-white">Sedikit tentang saya...</h2>
            <br />
            <p class="mb-3 text-justify text-gray-500 dark:text-gray-400">
              Perkenalkan nama saya Muhammad Athhar Malika Putra, kalian bisa memanggil saya <b>Athhar</b>. Saya lahir di Bandung
              pada tanggal 6 mei tahun 2005, anak dari Sonny Sonaji dan Irma Rakhmawati, saya anak pertama dari 2 bersaudara.
            </p>
            <p class="mb-3 text-justify text-gray-500 dark:text-gray-400">
              Dari TK sampai dengan SMP, saya sekolah di yayasan yang sama yaitu yayasan Al-Mumtaaz Karawang, banyak kisah atau
              pun pengalaman yang saya alami, mulai dari cerita sedih atau pun menyenangkan bahkan hingga cerita mistis. setelah
              lulus dari SMP Al-Mumtaaz, saya mendaftarkan diri ke sekolah SMK Assalaam Bandung, saya mengambil jurusan Rekayasa
              Perangkat Lunak (RPL) dan akhir nya saya bergabung dengan keluarga besar Assalaam.
            </p>
            <p class="mb-3 text-justify text-gray-500 dark:text-gray-400">
              Hobi yang saya favoritkan mencakup dari mendengar lagu, nonton film dan series, main game, hingga merakit gunpla.
              saat ini koleksi gundam yang saya punya adalah 4, di masa depan nanti semoga koleksi nya bertambah (aamiin). Selain
              itu, saya suka belajar bahasa, seperti bahasa Inggris dan Jepang (newbie), nanti saya juga ingin belajar bahasa yang
              lain nya jika ada waktu.
            </p>
            <p class="mb-3 text-center text-gray-500 dark:text-gray-400 italic">
              "If you move forward you gain two, If you run away you gain one"
              <br />
              - Sulletta Mercury.
            </p>
          </div>
        </div>
      </div>
      <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
        <div class="grid gap-3">
          <div>
            <h1 class="text-center mb-4 text-2xl tracking-tight leading-none text-gray-900 dark:text-white">Lagu Favorit</h1>
            <br>
            <iframe
              style="border-radius: 12px"
              src="https://open.spotify.com/embed/track/29m9hdcziVa1g3FrXtdNOe?utm_source=generator"
              width="100%"
              height="352"
              frameBorder="0"
              allowfullscreen=""
              allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
              loading="lazy"
            ></iframe>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.foto {
  width: auto;
  height: 100%;
  margin-left: 20%;
}
</style>
