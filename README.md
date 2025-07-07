# drubotz-ai-generator
Website Generator Prompt Simulasi Model AI
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Drubotz - Generator Prompt Simulasi AI</title>
<script src="https://cdn.tailwindcss.com"></script>
<style>
  body {
    background-color: #121827;
    color: #d1d5db;
    font-family: 'Inter', sans-serif;
  }
  .card {
    background-color: #1e293b;
    border-radius: 0.75rem;
    padding: 1.5rem;
  }
  .form-label {
    color: #a5b4fc;
  }
  .btn-primary {
    background-color: #7c3aed;
    transition: background-color 0.3s ease;
  }
  .btn-primary:hover {
    background-color: #9333ea;
  }
  .btn-secondary {
    background-color: #334155;
    transition: background-color 0.3s ease;
  }
  .btn-secondary:hover {
    background-color: #475569;
  }
  .gradient-text {
    background: linear-gradient(90deg, #6366f1, #ec4899);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .footer-text {
    color: #94a3b8;
    font-size: 0.875rem;
  }
</style>
</head>
<body class="min-h-screen flex flex-col items-center p-4 md:p-10">

<!-- Welcome message -->
<section class="card w-full max-w-4xl mb-8">
  <div class="flex items-center justify-between">
    <h2 class="font-semibold text-white text-lg">Selamat Malam! <span aria-label="celebration" role="img">🎊</span></h2>
    <div class="flex items-center text-green-400 font-mono select-none">
      <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" 
        viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" aria-hidden="true"><path d="M11 17l-5-5m0 0l5-5m-5 5h12"></path></svg>
      48%
    </div>
  </div>
  <time class="block text-gray-400 mt-1 font-mono">Senin, 7 Juli 2025 | 18:41:40</time>
</section>

<!-- Main prompt generator card -->
<section class="card w-full max-w-4xl mb-12 grid grid-cols-1 md:grid-cols-3 gap-8 items-start">
  <!-- Upload preview image -->
  <div class="col-span-1 flex justify-center">
    <img 
      src="https://placehold.co/300x400?text=User+Uploaded+Image"
      alt="Vertical photo showing a group of people standing under a concrete structure with pillars outdoors"
      class="rounded-lg shadow-lg max-h-[400px] object-cover"
      onerror="this.src='https://placehold.co/300x400/png?text=Image+Loading+Error';"
    />
  </div>

  <!-- Form -->
  <form id="promptForm" class="col-span-2 space-y-5 text-gray-300 text-sm">
    <h3 class="gradient-text font-semibold text-lg mb-1">Generator Prompt (<span class="text-pink-500">Simulasi Model AI</span>)</h3>
    <p class="text-gray-400 mb-4 text-xs">Unggah gambar dan simulasikan hasil dari berbagai model AI terkemuka.</p>

    <div>
      <label for="model" class="form-label block mb-1 font-semibold">Pilih Model (Simulasi):</label>
      <select id="model" name="model" class="w-full rounded-md bg-gray-800 py-2 px-3 focus:outline-none focus:ring-2 focus:ring-purple-500">
        <option>Gemini Flash (Sangat Detail)</option>
        <option>Alpha Vision (Realistis)</option>
        <option>NeuraArt 3D Render</option>
        <option>PixelDream Ultra</option>
      </select>
    </div>

    <div>
      <label for="aspect" class="form-label block mb-1 font-semibold">Rasio Aspek:</label>
      <select id="aspect" name="aspect" class="w-full rounded-md bg-gray-800 py-2 px-3 focus:outline-none focus:ring-2 focus:ring-purple-500">
        <option>3:4 (Potret)</option>
        <option>16:9 (Lanskap)</option>
        <option>1:1 (Persegi)</option>
        <option>4:3 (Klasik)</option>
      </select>
    </div>

    <div>
      <label for="distance" class="form-label block mb-1 font-semibold">Jarak Kamera:</label>
      <select id="distance" name="distance" class="w-full rounded-md bg-gray-800 py-2 px-3 focus:outline-none focus:ring-2 focus:ring-purple-500">
        <option>Sedang (Medium Shot)</option>
        <option>Jauh (Wide Shot)</option>
        <option>Dekat (Close-up)</option>
      </select>
    </div>

    <div>
      <label for="quality" class="form-label block mb-1 font-semibold">Kualitas Gambar:</label>
      <select id="quality" name="quality" class="w-full rounded-md bg-gray-800 py-2 px-3 focus:outline-none focus:ring-2 focus:ring-purple-500">
        <option>Ultra</option>
        <option>Tinggi</option>
        <option>Sedang</option>
        <option>Rendah</option>
      </select>
    </div>

    <div>
      <label for="device" class="form-label block mb-1 font-semibold">Perangkat Pengambilan Gambar:</label>
      <select id="device" name="device" class="w-full rounded-md bg-gray-800 py-2 px-3 focus:outline-none focus:ring-2 focus:ring-purple-500">
        <option>iPhone 16 Pro Max</option>
        <option>Google Pixel 8</option>
        <option>Samsung Galaxy S24</option>
        <option>Canon EOS R6</option>
      </select>
    </div>

    <div class="flex space-x-4 mt-4">
      <button type="submit" class="btn-primary px-5 py-2 rounded-md text-white font-semibold flex items-center gap-2 hover:bg-pink-600" aria-label="Buat Prompt">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24" aria-hidden="true"><path d="M12 20l9-12H3l9 12z"></path></svg> Buat Prompt
      </button>
      <button type="reset" class="btn-secondary px-5 py-2 rounded-md text-gray-300 font-semibold hover:bg-gray-600" aria-label="Reset Form">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24" aria-hidden="true"><path d="M6 18L18 6M6 6l12 12"></path></svg> Reset
      </button>
    </div>
  </form>
</section>

<!-- Logo and contact section -->
<section class="card w-full max-w-3xl text-center space-y-6">
  <div>
    <img 
      src="https://placehold.co/600x400?text=Drubotz+Logo+Robot+Blue+Teal+Cartoon+Smiling+Friendly+Tech" 
      alt="Logo robot keren warna biru dan hijau toska bergaya kartun dengan ekspresi tersenyum ramah mewakili Drubotz"
      class="mx-auto rounded-lg shadow-lg max-w-full h-auto"
      onerror="this.src='https://placehold.co/600x400/png?text=Logo+Loading+Error';"
      />
  </div>
  <h2 class="gradient-text font-semibold text-xl">Hubungi Kami</h2>
  <p class="text-gray-400 text-sm mb-4">Kami siap membantu Anda melalui berbagai saluran!</p>
  <div class="flex justify-center gap-5 mb-4">
    <a href="https://wa.me/628638980660" target="_blank" rel="noopener noreferrer" aria-label="Hubungi via WhatsApp" class="px-5 py-2 rounded-md text-white bg-green-600 hover:bg-green-700 flex items-center gap-2">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M20.52 3.48A11.93 11.93 0 0012 .03C5.37.03.05 5.39.05 12a11.87 11.87 0 002.05 6.51L0 24l5.6-2.93a11.94 11.94 0 006.42 1.83h.02c6.62 0 11.95-5.37 11.95-12 0-3.2-1.25-6.21-3.46-8.42zm-8.47 16.9c-1.91 0-3.7-.51-5.28-1.47l-.37-.22-3.31 1.71 1.7-3.23-.24-.38a8.5 8.5 0 01-1.3-4.53c0-4.7 3.83-8.53 8.53-8.53a8.54 8.54 0 015.99 2.48 8.45 8.45 0 012.54 6.05 8.53 8.53 0 01-8.54 8.5zm4.92-6.44c-.27-.14-1.59-.79-1.83-.88-.24-.1-.41-.14-.59.14-.18.27-.7.88-.85 1.06-.16.18-.31.2-.59.07-.27-.14-1.13-.42-2.15-1.32-.8-.71-1.34-1.59-1.5-1.86-.16-.27-.02-.41.12-.54.12-.12.27-.31.41-.47.14-.16.18-.27.27-.45.09-.18.05-.34-.02-.47-.07-.14-.59-1.43-.81-1.97-.21-.52-.43-.45-.59-.46h-.51c-.18 0-.47.07-.72.34-.27.27-1.03 1.01-1.03 2.46s1.05 2.86 1.2 3.06c.14.2 2.07 3.16 5.02 4.43.7.3 1.24.48 1.66.61.7.22 1.34.19 1.85.12.57-.08 1.76-.72 2.01-1.41.24-.7.24-1.29.17-1.41-.07-.12-.27-.18-.59-.31z"/></svg>
      WhatsApp
    </a>
    <a href="https://t.me/drubotz" target="_blank" rel="noopener noreferrer" aria-label="Hubungi via Telegram" class="px-5 py-2 rounded-md text-white bg-blue-600 hover:bg-blue-700 flex items-center gap-2">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M21.53 2.47a1.71 1.71 0 00-2.46.3L4.92 17.1 2.13 13.05a1.69 1.69 0 00-2.31-.49 1.65 1.65 0 00-.62 1.49l1.94 7.54a1.69 1.69 0 003.1 1c.15-.27 3.58-6.24 5.1-8.86 2.44-4.77 3.53-5.91 7.6-9.05a1.71 1.71 0 00.28-2.47z"/></svg>
      Telegram
    </a>
    <a href="https://facebook.com/drubotz" target="_blank" rel="noopener noreferrer" aria-label="Hubungi via Facebook" class="px-5 py-2 rounded-md text-white bg-blue-800 hover:bg-blue-900 flex items-center gap-2">
      <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M22.68 0H1.32A1.34 1.34 0 000 1.32v21.36A1.34 1.34 0 001.32 24h11.51v-9.28H10.33v-3.62h2.5V8.4c0-2.48 1.52-3.83 3.73-3.83 1.04 0 1.94.08 2.2.11v2.55h-1.51c-1.18 0-1.66.7-1.66 1.62v2.27h3.34l-.44 3.62h-2.9V24h5.68A1.34 1.34 0 0024 22.68V1.32A1.34 1.34 0 0022.68 0z"/></svg>
      Facebook
    </a>
  </div>

  <p class="footer-text mt-6">
    Atau hubungi kami melalui:<br />
    Email: <a href="mailto:muhamadbadruwasih8@gmail.com" class="underline hover:text-purple-400">muhamadbadruwasih8@gmail.com</a><br />
    Telepon: <a href="tel:+628638980660" class="underline hover:text-purple-400">+62 86 389 8060</a>
  </p>
</section>

<script>
  const form = document.getElementById('promptForm');
  form.addEventListener('submit', e => {
    e.preventDefault();
    const formData = new FormData(form);
    const prompt = 
      \`Simulasi Model AI:\nModel: \${formData.get('model')}\nRasio Aspek: \${formData.get('aspect')}\nJarak Kamera: \${formData.get('distance')}\nKualitas Gambar: \${formData.get('quality')}\nPerangkat: \${formData.get('device')}\`;
    alert('Prompt untuk AI generator:\\n\\n' + prompt);
  });
</script>

</body>
</html>

