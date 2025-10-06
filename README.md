virtual-lab-muaro-jambi/
├── web-lab/       ← untuk lab berbasis web (HTML)
└── data-lab/      ← untuk lab berbasis notebook (Python)
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Virtual Lab Candi Muaro Jambi</title>
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css">
  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f7f7f7; }
    header { background: #3c6e47; color: white; text-align: center; padding: 15px; }
    #map { height: 400px; margin: 20px; border-radius: 10px; }
    .plant-card { background: white; margin: 20px; padding: 10px; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
  </style>
</head>
<body>

<header>
  <h1>🌿 Virtual Lab Etnobiologi Candi Muaro Jambi</h1>
  <p>Eksplorasi tumbuhan dan lingkungan sekitar situs bersejarah</p>
</header>

<div id="map"></div>

<div class="plant-card">
  <h3>Ficus religiosa (Pohon Bodhi)</h3>
  <p>Simbol spiritual dan sering ditemukan di area suci candi.</p>
</div>

<div class="plant-card">
  <h3>Oroxylum indicum</h3>
  <p>Tumbuhan obat tradisional, digunakan untuk meredakan demam.</p>
</div>

<script>
  const map = L.map('map').setView([-1.553, 103.612], 14);
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(map);
  L.marker([-1.553, 103.612]).addTo(map).bindPopup("Candi Muaro Jambi");
</script>

</body>
</html>
