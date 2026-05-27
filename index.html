<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI-ster</title>

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background: linear-gradient(135deg, #0f172a, #111827);
      color: white;
      min-height: 100vh;
      padding: 30px;
    }

    h1 {
      text-align: center;
      font-size: 50px;
      margin-bottom: 10px;
    }

    .subtitle {
      text-align: center;
      color: #cbd5e1;
      margin-bottom: 40px;
    }

    .container {
      max-width: 1000px;
      margin: auto;
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 25px;
      padding: 30px;
      backdrop-filter: blur(10px);
      box-shadow: 0 0 30px rgba(0,0,0,0.4);
    }

    textarea {
      width: 100%;
      height: 120px;
      border-radius: 15px;
      border: none;
      padding: 15px;
      font-size: 16px;
      margin-top: 10px;
      background: rgba(255,255,255,0.08);
      color: white;
      outline: none;
    }

    input[type="file"] {
      margin-top: 15px;
      color: white;
    }

    .btn {
      padding: 14px 28px;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      font-size: 16px;
      font-weight: bold;
      transition: 0.3s;
      margin-top: 20px;
    }

    .generate-btn {
      background: linear-gradient(45deg, #00c6ff, #0072ff);
      color: white;
    }

    .generate-btn:hover {
      transform: scale(1.05);
      box-shadow: 0 0 20px #0072ff;
    }

    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      margin-top: 40px;
    }

    .card {
      background: rgba(255,255,255,0.05);
      border-radius: 20px;
      overflow: hidden;
      position: relative;
      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      filter: blur(1px);
    }

    .watermark {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 28px;
      font-weight: bold;
      color: rgba(255,255,255,0.7);
      pointer-events: none;
    }

    .download-btn {
      width: 100%;
      background: linear-gradient(45deg, #f59e0b, #f97316);
      color: white;
    }

    .download-btn:hover {
      box-shadow: 0 0 20px orange;
    }

    .payment-modal {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.8);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 1000;
    }

    .payment-box {
      width: 400px;
      background: #111827;
      border-radius: 25px;
      padding: 30px;
      text-align: center;
      animation: pop 0.4s ease;
    }

    @keyframes pop {
      from {
        transform: scale(0.7);
        opacity: 0;
      }
      to {
        transform: scale(1);
        opacity: 1;
      }
    }

    .payment-box img {
      width: 100%;
      border-radius: 20px;
      margin-top: 15px;
    }

    .close-btn {
      background: crimson;
      color: white;
      width: 100%;
    }

    .verify-btn {
      background: limegreen;
      color: white;
      width: 100%;
    }

    .hidden {
      display: none;
    }

    .admin-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #111;
      color: white;
      padding: 12px 18px;
      border-radius: 50px;
      cursor: pointer;
      opacity: 0.25;
      transition: 0.3s;
    }

    .admin-btn:hover {
      opacity: 1;
    }

    .success {
      margin-top: 15px;
      color: lime;
      font-weight: bold;
    }

  </style>
</head>
<body>

  <h1>AI-ster</h1>
  <p class="subtitle">Generate AI images and unlock HD downloads</p>

  <div class="container">

    <h2>Describe Your Image</h2>

    <textarea id="prompt" placeholder="Describe your image..."></textarea>

    <input type="file" id="materialUpload" multiple>

    <br>

    <button class="btn generate-btn" onclick="generateImages()">
      Generate AI Images
    </button>

    <div class="gallery" id="gallery"></div>

  </div>

  <!-- PAYMENT MODAL -->

  <div class="payment-modal" id="paymentModal">

    <div class="payment-box">

      <h2>Unlock HD Download</h2>

      <p style="margin-top:10px; color:#cbd5e1;">
        Pay ₹100 to download high quality images
      </p>

      <img src="scanner.jpeg" alt="UPI QR">

      <p style="margin-top:15px;">
        UPI ID: pranavhingane0-1@oksbi
      </p>

      <button class="btn verify-btn" onclick="showProofSection()">
        I Have Paid
      </button>

      <div id="proofSection" class="hidden">

        <input type="file" id="paymentScreenshot">

        <button class="btn verify-btn" onclick="verifyPayment()">
          Verify Payment
        </button>

        <p id="verifyMessage" class="success"></p>

      </div>

      <button class="btn close-btn" onclick="closePayment()">
        Close
      </button>

    </div>

  </div>

  <!-- ADMIN ACCESS -->

  <div class="admin-btn" onclick="adminAccess()">
    Admin
  </div>

  <script>

    const ADMIN_KEY = "mepranav";

    let selectedDownload = null;

    const demoImages = [
      "https://picsum.photos/500/500?1",
      "https://picsum.photos/500/500?2",
      "https://picsum.photos/500/500?3"
    ];

    function generateImages() {

      let prompt = document.getElementById("prompt").value;

      if(prompt.trim() === "") {
        alert("Please enter image description");
        return;
      }

      let gallery = document.getElementById("gallery");

      gallery.innerHTML = "";

      demoImages.forEach((img, index) => {

        gallery.innerHTML += `

          <div class="card">

            <img src="${img}">

            <div class="watermark">AI-ster</div>

            <button class="btn download-btn" onclick="openPayment('${img}')">
              Download HD
            </button>

          </div>

        `;

      });

    }

    function openPayment(image) {

      let isAdmin = localStorage.getItem("adminMode");

      if(isAdmin === "true") {
        downloadImage(image);
        return;
      }

      selectedDownload = image;

      document.getElementById("paymentModal").style.display = "flex";

    }

    function closePayment() {

      document.getElementById("paymentModal").style.display = "none";

    }

    function showProofSection() {

      document.getElementById("proofSection").classList.remove("hidden");

    }

    function verifyPayment() {

      let file = document.getElementById("paymentScreenshot").files[0];

      if(!file) {
        alert("Please upload payment screenshot");
        return;
      }

      document.getElementById("verifyMessage").innerHTML =
      "Payment screenshot uploaded successfully. Admin verification pending.";

      setTimeout(() => {

        alert("Demo Mode: Payment Approved");

        downloadImage(selectedDownload);

      }, 2000);

    }

    function downloadImage(image) {

      let a = document.createElement("a");

      a.href = image;

      a.download = "AI-ster-image.jpg";

      document.body.appendChild(a);

      a.click();

      document.body.removeChild(a);

      closePayment();

    }

    function adminAccess() {

      let key = prompt("Enter Admin Key");

      if(key === ADMIN_KEY) {

        localStorage.setItem("adminMode", "true");

        alert("Admin Mode Activated");

      } else {

        alert("Wrong Admin Key");

      }

    }

  </script>

</body>
</html>
