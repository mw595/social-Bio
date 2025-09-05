<!DOCTYPE html>
<html lang="en" >
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Social Bio - Exclusive Content Access</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet" />
</head>
<body class="bg-gradient-to-r from-indigo-900 via-purple-900 to-pink-900 min-h-screen flex items-center justify-center p-6 text-white">
  <main class="bg-gray-900 bg-opacity-90 rounded-xl shadow-xl max-w-lg w-full p-8 text-center">
    <h1 class="text-5xl font-extrabold mb-4 tracking-wide">Social Bio</h1>
    <p class="mb-6 text-indigo-300 text-lg">Unlock exclusive content for just <span class="font-bold text-green-400">600 XTZ (~$5)</span> per month.</p>

    <section class="mb-8">
      <h2 class="text-2xl font-semibold mb-3 text-purple-300">Follow me on Social Media</h2>
      <div class="flex justify-center gap-6 text-indigo-400 text-lg font-semibold">
        <a href="https://youtube.com/yourchannel" target="_blank" class="hover:text-green-400 transition">YouTube</a>
        <a href="https://facebook.com/yourpage" target="_blank" class="hover:text-green-400 transition">Facebook</a>
        <a href="https://instagram.com/ruvenmwita" target="_blank" class="hover:text-green-400 transition">Instagram</a>
        <a href="https://tiktok.com/@ruvenmwita7" target="_blank" class="hover:text-green-400 transition">TikTok</a>
      </div>
    </section>

    <section class="mb-8">
      <h2 class="text-2xl font-semibold mb-3 text-purple-300">Make Payment</h2>
      <p class="text-indigo-300 mb-4">Click the button below to pay <strong>600 XTZ</strong> directly and unlock exclusive content.</p>
      <a 
        href="https://wallet.kukai.app/transfer/your-tezos-wallet-address/600" 
        target="_blank"
        class="inline-block bg-green-500 hover:bg-green-600 font-bold py-3 px-6 rounded-md tr
         >
        Pay 600 XTZ Now
      </a>
    </section>

    <section>
      <h2 class="text-2xl font-semibold mb-3 text-purple-300">Submit Payment Confirmation</h2>
      <form id="confirmationForm" class="space-y-4 text-left max-w-md mx-auto" enctype="multipart/form-data">
        <label for="phone" class="block mb-1">Your Phone Number (optional):</label>
        <input
          type="tel"
          id="phone"
          name="phone"
          placeholder="+2557XXXXXXXX"
          class="w-full p-3 rounded-md text-black"
        />

        <label for="transactionId" class="block mb-1">Transaction Code (optional):</label>
        <input
          type="text"
          id="transactionId"
          name="transactionId"
          placeholder="Enter your transaction code"
          class="w-full p-3 rounded-md text-black"
        />

        <label for="paymentProof" class="block mb-1">Upload Payment Proof (image/pdf):</label>
        <input
          type="file"
          id="paymentProof"
          name="paymentProof"
          accept="image/*,application/pdf"
          required
          class="w-full p-3 rounded-md text-black"
        />

        <button
          type="submit"
          class="w-full bg-green-500 hover:bg-green-600 font-bold py-3 rounded-md transition duration-300"
        >
          Submit Confirmation
        </button>
      </form>
      <p id="message" class="mt-4 text-center text-indigo-300"></p>
    </section>
  </main>

  <script>
    const form = document.getElementById('confirmationForm');
    const message = document.getElementById('message');

    form.addEventListener('submit', e => {
      e.preventDefault();

      // Check if file is selected
      const fileInput = form.paymentProof;
      if (!fileInput.files.length) {
        message.textContent = 'Please upload your payment proof file.';
        return;
      }

      message.textContent = 'Submitting your payment confirmation...';

      // Simulate upload delay
      setTimeout(() => {
        message.textContent = 'Thank you! Your payment confirmation has been received. We will verify shortly.';
        form.reset();
      }, 1500);
    });
    const express = require('express');
const multer = require('multer');
const upload = multer({ dest: 'uploads/' });
const app = express();

app.post('/upload-payment-proof', upload.single('paymentProof'), (req, res) => {
  console.log('File info:', req.file);
  console.log('Other fields:', req.body);
  res.json({ message: 'Upload successful!' });
});

app.listen(3000, () => console.log('Server running on port 3000'));

<form
  id="confirmationForm"
  action="/upload-payment-proof"
  method="POST"
  enctype="multipart/form-data"
>

  </script>
</body>
</html>
