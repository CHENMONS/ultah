<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Undangan Ulang Tahun ke-20</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Georgia', serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 600px;
            width: 100%;
            background: white;
            border-radius: 30px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            overflow: hidden;
            animation: fadeIn 1s ease-out;
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 60px 30px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: '🎉';
            position: absolute;
            font-size: 100px;
            opacity: 0.1;
            top: -20px;
            left: -20px;
            animation: float 3s ease-in-out infinite;
        }
        
        .header::after {
            content: '🎂';
            position: absolute;
            font-size: 100px;
            opacity: 0.1;
            bottom: -20px;
            right: -20px;
            animation: float 3s ease-in-out infinite reverse;
        }
        
        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-20px);
            }
        }
        
        .header h1 {
            color: white;
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
            animation: slideDown 0.8s ease-out;
        }
        
        @keyframes slideDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .header p {
            color: rgba(255,255,255,0.9);
            font-size: 1.2em;
            font-style: italic;
        }
        
        .age-badge {
            display: inline-block;
            background: white;
            color: #764ba2;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 3em;
            font-weight: bold;
            margin: 20px 0;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            animation: pulse 2s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }
        
        .content {
            padding: 40px 30px;
        }
        
        .section {
            margin-bottom: 35px;
            animation: fadeInUp 0.8s ease-out backwards;
        }
        
        .section:nth-child(2) {
            animation-delay: 0.2s;
        }
        
        .section:nth-child(3) {
            animation-delay: 0.4s;
        }
        
        .section:nth-child(4) {
            animation-delay: 0.6s;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .section-icon {
            font-size: 2em;
            margin-bottom: 10px;
        }
        
        .section h2 {
            color: #764ba2;
            font-size: 1.5em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .section p {
            color: #555;
            line-height: 1.8;
            font-size: 1.1em;
        }
        
        .detail-box {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 20px;
            border-radius: 15px;
            margin-top: 10px;
            border-left: 5px solid #764ba2;
        }
        
        .detail-box strong {
            color: #764ba2;
            display: block;
            margin-bottom: 5px;
        }
        
        .map-button {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 15px;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }
        
        .map-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.6);
        }
        
        .footer {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 30px;
            text-align: center;
            color: white;
        }
        
        .footer p {
            font-size: 1.1em;
            margin-bottom: 10px;
        }
        
        .decorative-line {
            width: 100px;
            height: 3px;
            background: linear-gradient(90deg, transparent, #764ba2, transparent);
            margin: 20px auto;
        }
        
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background: #764ba2;
            position: absolute;
            animation: confetti-fall 3s linear infinite;
        }
        
        @keyframes confetti-fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }
        
        .rsvp-section {
            background: linear-gradient(135deg, #ffeaa7 0%, #fdcb6e 100%);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            margin-top: 20px;
        }
        
        .rsvp-section h3 {
            color: #2d3436;
            margin-bottom: 10px;
        }
        
        @media (max-width: 600px) {
            .header h1 {
                font-size: 2em;
            }
            
            .age-badge {
                font-size: 2.5em;
                padding: 12px 25px;
            }
            
            .content {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎊 You're Invited! 🎊</h1>
            <p>Perayaan Ulang Tahun</p>
            <div class="age-badge">20</div>
            <p>Tahun Penuh Kenangan</p>
        </div>
        
        <div class="content">
            <div class="section">
                <h2><span class="section-icon">🎉</span> Mari Merayakan Bersama!</h2>
                <p>Dengan penuh kebahagiaan, saya mengundang Anda untuk merayakan ulang tahun ke-20 saya. Mari berbagi kegembiraan, tawa, dan kenangan indah bersama!</p>
                <div class="decorative-line"></div>
            </div>
            
            <div class="section">
                <h2><span class="section-icon">📅</span> Waktu Acara</h2>
                <div class="detail-box">
                    <strong>Tanggal & Waktu:</strong>
                    <p>Pukul 18.00 - Selesai</p>
                    <p style="margin-top: 10px; font-style: italic; color: #764ba2;">
                        Datang tepat waktu untuk kejutan spesial! ✨
                    </p>
                </div>
            </div>
            
            <div class="section">
                <h2><span class="section-icon">📍</span> Lokasi</h2>
                <div class="detail-box">
                    <strong>The Cups & Co</strong>
                    <p>Jl. Gunung Krakatau No.25A, Glugur Darat I</p>
                    <p>Kec. Medan Tim., Kota Medan</p>
                    <p>Sumatera Utara 20238</p>
                    <a href="https://www.google.com/maps/search/?api=1&query=The+Cups+%26+Co+Jl.+Gunung+Krakatau+No.25A+Medan" 
                       target="_blank" 
                       class="map-button">
                        📍 Buka Google Maps
                    </a>
                </div>
            </div>
            
            <div class="section">
                <h2><span class="section-icon">🎁</span> Dress Code</h2>
                <div class="detail-box">
                    <strong>Kasual Chic</strong>
                    <p>Kenakan pakaian favorit Anda dan datang dengan senyuman terbaik! 😊</p>
                </div>
            </div>
            
            <div class="rsvp-section">
                <h3>🌟 Kehadiran Anda Sangat Berarti 🌟</h3>
                <p style="color: #2d3436; margin-top: 10px;">
                    Tanpa kehadiran Anda, perayaan ini tidak akan lengkap!
                </p>
            </div>
        </div>
        
        <div class="footer">
            <p style="font-size: 1.3em; margin-bottom: 15px;">✨ Sampai Jumpa di Perayaan! ✨</p>
            <p style="font-size: 0.9em; opacity: 0.9;">
                Mari ciptakan kenangan indah bersama 🎂
            </p>
        </div>
    </div>
</body>
</html>
