# Hygiene-Calculator-For-Crew-HSET-PT.-STM-Job-Site-WBN
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alat Bantu Hygiene Inspection Untuk Crew HSET PT. STM Job Site WBN</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            --warning: #f39c12;
            --danger: #e74c3c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background-color: var(--primary);
            color: white;
            padding: 20px 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin-left: 10px;
        }
        
        .logo-icon {
            font-size: 2rem;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 20px;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary);
        }
        
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 60px 0;
            text-align: center;
            margin-bottom: 30px;
            border-radius: 0 0 10px 10px;
        }
        
        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        
        .card {
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 20px;
            transition: transform 0.3s;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 15px;
            border-bottom: 1px solid #eee;
            padding-bottom: 10px;
        }
        
        .card-title {
            font-size: 1.3rem;
            color: var(--primary);
        }
        
        .card-icon {
            font-size: 1.5rem;
            color: var(--secondary);
        }
        
        .parameter {
            margin-bottom: 15px;
        }
        
        .parameter-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .parameter-name {
            font-weight: 500;
        }
        
        .parameter-value {
            font-weight: bold;
        }
        
        .progress-bar {
            height: 10px;
            background-color: #eee;
            border-radius: 5px;
            overflow: hidden;
        }
        
        .progress {
            height: 100%;
            border-radius: 5px;
        }
        
        .safe {
            background-color: var(--success);
        }
        
        .warning {
            background-color: var(--warning);
        }
        
        .danger {
            background-color: var(--danger);
        }
        
        .status {
            display: inline-block;
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: bold;
        }
        
        .status-safe {
            background-color: rgba(46, 204, 113, 0.2);
            color: var(--success);
        }
        
        .status-warning {
            background-color: rgba(243, 156, 18, 0.2);
            color: var(--warning);
        }
        
        .status-danger {
            background-color: rgba(231, 76, 60, 0.2);
            color: var(--danger);
        }
        
        .form-section {
            background: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 25px;
            margin-bottom: 30px;
        }
        
        .form-title {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 1px solid #eee;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        input, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        button {
            background-color: var(--secondary);
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 500;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: #2980b9;
        }
        
        .results {
            margin-top: 30px;
        }
        
        .results-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        
        .results-table th, .results-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        
        .results-table th {
            background-color: var(--light);
            color: var(--dark);
            font-weight: 600;
        }
        
        .results-table tr:hover {
            background-color: #f9f9f9;
        }
        
        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 15px;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 10px;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <span class="logo-icon">⚒️</span>
                    <h1>Alat Bantu Analisis Hygiene Bagi Crew HSET Job Site WBN</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#dashboard">Dashboard</a></li>
                        <li><a href="#kebisingan">Tes Kebisingan</a></li>
                        <li><a href="#cahaya">Tes Cahaya</a></li>
                        <li><a href="#udara">Kualitas Udara</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h2>Alat Bantu Calculator Hygiene Untuk Crew HSET Job Site WBN</h2>
            <p>Platform untuk menganalisis dan memantau parameter lingkungan kerja di area pertambangan untuk memastikan keselamatan dan kesehatan pekerja</p>
        </div>
    </section>
    
    <div class="container">
        <section id="dashboard" class="dashboard">
            <div class="card">
                <div class="card-header">
                    <h3 class="card-title">Kebisingan</h3>
                    <span class="card-icon">🔊</span>
                </div>
                <div class="parameter">
                    <div class="parameter-label">
                        <span class="parameter-name">Level Kebisingan</span>
                        <span class="parameter-value">85 dB</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress warning" style="width: 70%"></div>
                    </div>
                    <div class="parameter-label">
                        <span>Status:</span>
                        <span class="status status-warning">Perlu Perhatian</span>
                    </div>
                </div>
                <p>Paparan maksimal: 8 jam pada 85 dB</p>
            </div>
            
            <div class="card">
                <div class="card-header">
                    <h3 class="card-title">Intensitas Cahaya</h3>
                    <span class="card-icon">💡</span>
                </div>
                <div class="parameter">
                    <div class="parameter-label">
                        <span class="parameter-name">Tingkat Pencahayaan</span>
                        <span class="parameter-value">350 lux</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress safe" style="width: 60%"></div>
                    </div>
                    <div class="parameter-label">
                        <span>Status:</span>
                        <span class="status status-safe">Aman</span>
                    </div>
                </div>
                <p>Standar area kerja: 200-500 lux</p>
            </div>
            
            <div class="card">
                <div class="card-header">
                    <h3 class="card-title">Kualitas Udara</h3>
                    <span class="card-icon">💨</span>
                </div>
                <div class="parameter">
                    <div class="parameter-label">
                        <span class="parameter-name">Debu Partikulat</span>
                        <span class="parameter-value">3.2 mg/m³</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress danger" style="width: 80%"></div>
                    </div>
                    <div class="parameter-label">
                        <span>Status:</span>
                        <span class="status status-danger">Berbahaya</span>
                    </div>
                </div>
                <p>Batas aman: ≤ 2.5 mg/m³</p>
            </div>
        </section>
        
        <section id="kebisingan" class="form-section">
            <h2 class="form-title">Analisis Tingkat Kebisingan</h2>
            <form id="noiseForm">
                <div class="form-group">
                    <label for="location">Lokasi Pengukuran</label>
                    <input type="text" id="location" placeholder="Contoh: Area Penambangan Bawah Tanah Level 3" required>
                </div>
                
                <div class="form-group">
                    <label for="noiseLevel">Tingkat Kebisingan (dB)</label>
                    <input type="number" id="noiseLevel" min="0" max="150" step="0.1" placeholder="Contoh: 85.5" required>
                </div>
                
                <div class="form-group">
                    <label for="exposureTime">Waktu Paparan (jam)</label>
                    <input type="number" id="exposureTime" min="0" max="24" step="0.5" placeholder="Contoh: 8" required>
                </div>
                
                <div class="form-group">
                    <label for="equipment">Peralatan yang Digunakan</label>
                    <select id="equipment" required>
                        <option value="">Pilih Peralatan</option>
                        <option value="drill">Mesin Bor</option>
                        <option value="excavator">Excavator</option>
                        <option value="crusher">Mesin Penghancur</option>
                        <option value="conveyor">Conveyor Belt</option>
                        <option value="other">Lainnya</option>
                    </select>
                </div>
                
                <button type="submit">Analisis Kebisingan</button>
            </form>
            
            <div class="results" id="noiseResults" style="display: none;">
                <h3>Hasil Analisis Kebisingan</h3>
                <table class="results-table">
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Nilai</th>
                            <th>Status</th>
                            <th>Rekomendasi</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Tingkat Kebisingan</td>
                            <td id="resultNoiseLevel">-</td>
                            <td id="resultNoiseStatus">-</td>
                            <td id="resultNoiseRecommendation">-</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>
        
        <section id="cahaya" class="form-section">
            <h2 class="form-title">Analisis Intensitas Cahaya</h2>
            <form id="lightForm">
                <div class="form-group">
                    <label for="lightLocation">Lokasi Pengukuran</label>
                    <input type="text" id="lightLocation" placeholder="Contoh: Ruang Kontrol Utama" required>
                </div>
                
                <div class="form-group">
                    <label for="lightIntensity">Intensitas Cahaya (lux)</label>
                    <input type="number" id="lightIntensity" min="0" max="5000" step="1" placeholder="Contoh: 350" required>
                </div>
                
                <div class="form-group">
                    <label for="areaType">Jenis Area Kerja</label>
                    <select id="areaType" required>
                        <option value="">Pilih Jenis Area</option>
                        <option value="office">Kantor/Administrasi</option>
                        <option value="control">Ruang Kontrol</option>
                        <option value="workshop">Bengkel/Workshop</option>
                        <option value="mining">Area Penambangan</option>
                        <option value="processing">Area Pengolahan</option>
                    </select>
                </div>
                
                <button type="submit">Analisis Pencahayaan</button>
            </form>
            
            <div class="results" id="lightResults" style="display: none;">
                <h3>Hasil Analisis Pencahayaan</h3>
                <table class="results-table">
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Nilai</th>
                            <th>Status</th>
                            <th>Rekomendasi</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Intensitas Cahaya</td>
                            <td id="resultLightIntensity">-</td>
                            <td id="resultLightStatus">-</td>
                            <td id="resultLightRecommendation">-</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>
        
        <section id="udara" class="form-section">
            <h2 class="form-title">Analisis Kualitas Udara</h2>
            <form id="airForm">
                <div class="form-group">
                    <label for="airLocation">Lokasi Pengukuran</label>
                    <input type="text" id="airLocation" placeholder="Contoh: Terowongan Utama" required>
                </div>
                
                <div class="form-group">
                    <label for="dustLevel">Tingkat Debu (mg/m³)</label>
                    <input type="number" id="dustLevel" min="0" max="50" step="0.1" placeholder="Contoh: 2.5" required>
                </div>
                
                <div class="form-group">
                    <label for="gasLevel">Tingkat Gas Berbahaya (ppm)</label>
                    <input type="number" id="gasLevel" min="0" max="1000" step="1" placeholder="Contoh: 25" required>
                </div>
                
                <div class="form-group">
                    <label for="ventilation">Sistem Ventilasi</label>
                    <select id="ventilation" required>
                        <option value="">Pilih Status Ventilasi</option>
                        <option value="good">Baik</option>
                        <option value="moderate">Cukup</option>
                        <option value="poor">Buruk</option>
                        <option value="none">Tidak Ada</option>
                    </select>
                </div>
                
                <button type="submit">Analisis Kualitas Udara</button>
            </form>
            
            <div class="results" id="airResults" style="display: none;">
                <h3>Hasil Analisis Kualitas Udara</h3>
                <table class="results-table">
                    <thead>
                        <tr>
                            <th>Parameter</th>
                            <th>Nilai</th>
                            <th>Status</th>
                            <th>Rekomendasi</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>Tingkat Debu</td>
                            <td id="resultDustLevel">-</td>
                            <td id="resultDustStatus">-</td>
                            <td id="resultDustRecommendation">-</td>
                        </tr>
                        <tr>
                            <td>Tingkat Gas Berbahaya</td>
                            <td id="resultGasLevel">-</td>
                            <td id="resultGasStatus">-</td>
                            <td id="resultGasRecommendation">-</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>
    </div>
    
    <footer>
        <div class="container">
            <p>&copy; 2025 Sistem Analisis Hygiene Industri Pertambangan. By Nanda Fachry - Safety Officer System and Compliance.</p>
        </div>
    </footer>
    
    <script>
        // Fungsi untuk analisis kebisingan
        document.getElementById('noiseForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const noiseLevel = parseFloat(document.getElementById('noiseLevel').value);
            const exposureTime = parseFloat(document.getElementById('exposureTime').value);
            
            let status, recommendation;
            
            if (noiseLevel <= 80) {
                status = 'Aman';
                recommendation = 'Tingkat kebisingan dalam batas aman. Tetap gunakan APD jika diperlukan.';
            } else if (noiseLevel <= 85 && exposureTime <= 8) {
                status = 'Perlu Perhatian';
                recommendation = 'Batasi paparan maksimal 8 jam. Gunakan pelindung telinga.';
            } else if (noiseLevel <= 90 && exposureTime <= 4) {
                status = 'Berisiko';
                recommendation = 'Batasi paparan maksimal 4 jam. Wajib menggunakan pelindung telinga.';
            } else {
                status = 'Berbahaya';
                recommendation = 'Paparan harus dibatasi maksimal 2 jam. Perlu evaluasi engineering control.';
            }
            
            document.getElementById('resultNoiseLevel').textContent = noiseLevel + ' dB';
            document.getElementById('resultNoiseStatus').innerHTML = `<span class="status status-${status.toLowerCase().replace(' ', '-')}">${status}</span>`;
            document.getElementById('resultNoiseRecommendation').textContent = recommendation;
            
            document.getElementById('noiseResults').style.display = 'block';
        });
        
        // Fungsi untuk analisis pencahayaan
        document.getElementById('lightForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const lightIntensity = parseInt(document.getElementById('lightIntensity').value);
            const areaType = document.getElementById('areaType').value;
            
            let minStandard, maxStandard, status, recommendation;
            
            switch(areaType) {
                case 'office':
                    minStandard = 300;
                    maxStandard = 500;
                    break;
                case 'control':
                    minStandard = 300;
                    maxStandard = 500;
                    break;
                case 'workshop':
                    minStandard = 200;
                    maxStandard = 300;
                    break;
                case 'mining':
                    minStandard = 100;
                    maxStandard = 200;
                    break;
                case 'processing':
                    minStandard = 150;
                    maxStandard = 300;
                    break;
                default:
                    minStandard = 200;
                    maxStandard = 500;
            }
            
            if (lightIntensity >= minStandard && lightIntensity <= maxStandard) {
                status = 'Aman';
                recommendation = 'Tingkat pencahayaan sesuai standar untuk area ini.';
            } else if (lightIntensity < minStandard) {
                status = 'Kurang';
                recommendation = 'Tingkat pencahayaan di bawah standar. Tambah sumber cahaya atau intensitas lampu.';
            } else {
                status = 'Berlebih';
                recommendation = 'Tingkat pencahayaan melebihi standar. Kurangi intensitas untuk menghindari silau.';
            }
            
            document.getElementById('resultLightIntensity').textContent = lightIntensity + ' lux';
            document.getElementById('resultLightStatus').innerHTML = `<span class="status status-${status.toLowerCase()}">${status}</span>`;
            document.getElementById('resultLightRecommendation').textContent = recommendation;
            
            document.getElementById('lightResults').style.display = 'block';
        });
        
        // Fungsi untuk analisis kualitas udara
        document.getElementById('airForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const dustLevel = parseFloat(document.getElementById('dustLevel').value);
            const gasLevel = parseInt(document.getElementById('gasLevel').value);
            const ventilation = document.getElementById('ventilation').value;
            
            // Analisis debu
            let dustStatus, dustRecommendation;
            if (dustLevel <= 2.5) {
                dustStatus = 'Aman';
                dustRecommendation = 'Tingkat debu dalam batas aman.';
            } else if (dustLevel <= 5) {
                dustStatus = 'Perlu Perhatian';
                dustRecommendation = 'Gunakan masker debu. Evaluasi sistem ventilasi.';
            } else {
                dustStatus = 'Berbahaya';
                dustRecommendation = 'Wajib menggunakan respirator. Perbaiki sistem ventilasi segera.';
            }
            
            // Analisis gas
            let gasStatus, gasRecommendation;
            if (gasLevel <= 25) {
                gasStatus = 'Aman';
                gasRecommendation = 'Tingkat gas dalam batas aman.';
            } else if (gasLevel <= 50) {
                gasStatus = 'Perlu Perhatian';
                gasRecommendation = 'Monitor terus tingkat gas. Pastikan ventilasi berfungsi baik.';
            } else {
                gasStatus = 'Berbahaya';
                gasRecommendation = 'Evakuasi area jika diperlukan. Perbaiki sistem ventilasi segera.';
            }
            
            // Rekomendasi berdasarkan ventilasi
            if (ventilation === 'poor' || ventilation === 'none') {
                if (dustStatus !== 'Aman' || gasStatus !== 'Aman') {
                    dustRecommendation += ' SISTEM VENTILASI PERLU DIPERBAIKI SEGERA.';
                    gasRecommendation += ' SISTEM VENTILASI PERLU DIPERBAIKI SEGERA.';
                }
            }
            
            document.getElementById('resultDustLevel').textContent = dustLevel + ' mg/m³';
            document.getElementById('resultDustStatus').innerHTML = `<span class="status status-${dustStatus.toLowerCase().replace(' ', '-')}">${dustStatus}</span>`;
            document.getElementById('resultDustRecommendation').textContent = dustRecommendation;
            
            document.getElementById('resultGasLevel').textContent = gasLevel + ' ppm';
            document.getElementById('resultGasStatus').innerHTML = `<span class="status status-${gasStatus.toLowerCase().replace(' ', '-')}">${gasStatus}</span>`;
            document.getElementById('resultGasRecommendation').textContent = gasRecommendation;
            
            document.getElementById('airResults').style.display = 'block';
        });
    </script>
</body>
</html>
