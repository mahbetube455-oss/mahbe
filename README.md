<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ማሕቤ ቢዝነስ ማዕከል | Mahbe Business Center</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root { 
            --blue: #004e92; 
            --yellow: #f7e017; 
            --dark: #002347;
            --white: #ffffff;
        }
        
        body { font-family: 'Segoe UI', 'Ubuntu', sans-serif; margin: 0; background: #f8f9fa; color: #333; overflow-x: hidden; }
        
        /* Fixed Header */
        header { 
            background: var(--white); padding: 10px 5%; display: flex; justify-content: space-between; 
            align-items: center; position: fixed; width: 90%; top: 0; z-index: 1000; 
            box-shadow: 0 2px 15px rgba(0,0,0,0.1); border-bottom: 3px solid var(--blue);
        }
        .logo-area { display: flex; align-items: center; gap: 10px; }
        .logo-img { height: 45px; border-radius: 50%; border: 2px solid var(--blue); }
        .eth-flag { width: 30px; height: 18px; border-radius: 2px; box-shadow: 0 0 3px rgba(0,0,0,0.2); }
        .logo-text { font-weight: 900; color: var(--blue); font-size: 1.1rem; }
        
        nav { display: flex; gap: 8px; }
        nav a { color: #444; text-decoration: none; font-weight: bold; font-size: 0.75rem; cursor: pointer; padding: 5px; transition: 0.3s; }
        nav a:hover { color: var(--blue); transform: translateY(-2px); }

        .content-section { display: none; padding: 110px 5% 60px; animation: fadeIn 0.6s ease-in-out; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(15px); } to { opacity: 1; transform: translateY(0); } }

        /* Home Hero Design */
        .hero-card { 
            background: linear-gradient(135deg, var(--blue), #0066cc); color: white; 
            padding: 40px 20px; border-radius: 30px; text-align: center; 
            box-shadow: 0 15px 35px rgba(0,78,146,0.3); margin-bottom: 30px;
        }
        .hero-img { width: 120px; height: 120px; border-radius: 50%; border: 5px solid var(--yellow); margin-bottom: 15px; }

        /* Testimonial Box */
        .testimonial-box { 
            background: white; padding: 25px; border-radius: 20px; margin: 20px 0;
            border-left: 8px solid var(--yellow); position: relative; box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        .testimonial-box i { color: var(--yellow); font-size: 1.5rem; margin-bottom: 10px; }

        /* Professional Buttons */
        .btn-container { display: flex; flex-direction: column; gap: 12px; margin-top: 20px; }
        .tg-btn { 
            background: var(--yellow); color: #000; padding: 16px; border-radius: 15px; 
            text-decoration: none; font-weight: 800; display: flex; align-items: center; justify-content: center; gap: 10px;
            box-shadow: 0 8px 20px rgba(247, 224, 23, 0.3); transition: 0.3s;
        }
        .tg-btn:hover { transform: scale(1.02); background: #e6d000; }

        /* Service Cards */
        .service-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .service-card { background: var(--dark); color: white; padding: 30px; border-radius: 25px; text-align: center; border-bottom: 5px solid var(--yellow); }
        .service-icon { font-size: 3rem; color: var(--yellow); margin-bottom: 15px; }

        /* Comment Form */
        .comment-form { background: white; padding: 30px; border-radius: 25px; box-shadow: 0 10px 30px rgba(0,0,0,0.1); max-width: 500px; margin: 0 auto; }
        .comment-form input, .comment-form textarea { width: 100%; padding: 15px; margin: 10px 0; border: 1px solid #ddd; border-radius: 12px; box-sizing: border-box; }
        .send-btn { background: var(--blue); color: white; border: none; padding: 15px; width: 100%; border-radius: 50px; font-weight: bold; cursor: pointer; font-size: 1rem; }

ዘ-ዓምደ ሥላሴ, [1/2/2026 11:03 PM]
/* Gallery */
        .gallery-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 15px; }
        .gallery-item img { width: 100%; border-radius: 15px; transition: 0.3s; }
        .gallery-item img:hover { transform: scale(1.05); }

        footer { background: var(--white); padding: 30px; text-align: center; border-top: 1px solid #eee; font-size: 0.9rem; }
    </style>
</head>
<body>

    <header>
        <div class="logo-area">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="logo-img" alt="Logo">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/71/Flag_of_Ethiopia.svg" class="eth-flag" alt="Flag">
            <span class="logo-text">ማሕቤ ቢዝነስ</span>
        </div>
        <nav>
            <a onclick="showSection('home')">Home</a>
            <a onclick="showSection('services')">Services</a>
            <a onclick="showSection('gallery')">Gallery</a>
            <a onclick="showSection('about')">About</a>
            <a onclick="showSection('comment')" style="color: var(--blue);">Comment</a>
        </nav>
    </header>

    <div id="home" class="content-section" style="display: block;">
        <div class="hero-card">
            <img src="https://i.ibb.co/Mk7dRNR1/IMG-20260102-205355-990.png" class="hero-img">
            <h1 style="margin: 0;">እንኳን ደህና መጡ!</h1>
            <p>ለስጋዎም ለነፍስዎም የሚሆኑ ጥራት ያላቸው ስራዎች ማዕከል</p>
        </div>

        <div class="testimonial-box">
            <i class="fas fa-quote-left"></i>
            <p style="font-style: italic; font-size: 1.1rem; line-height: 1.6;">"በጣም የሚገርም እና ደስ የሚል ስራ ነው ከፍጥነታችሁ ጥራታችሁ እኔ ሲፈጥን እንደዚህ ጥራት ይኖረዋል ብየ አልጠበኩም"</p>
            <p style="text-align: right; font-weight: bold; color: var(--blue);">— ከአንዲት ደንበኛ የተሰጠ አስተያየት ⭐⭐⭐⭐⭐</p>
        </div>

        <div class="btn-container">
            <h3 style="text-align: center; margin-bottom: 5px;">አሁኑኑ እዘዙ / እኛን ያግኙ</h3>
            <a href="https://t.me/temu_amen" class="tg-btn"><i class="fab fa-telegram-plane"></i> ዋና መስመር (@temu_amen)</a>
            <a href="https://t.me/mahbe_3" class="tg-btn" style="background: var(--blue); color: white;"><i class="fab fa-telegram-plane"></i> አማራጭ (@mahbe_3)</a>
        </div>
    </div>

    <div id="services" class="content-section">
        <h2 style="text-align: center; color: var(--blue); margin-bottom: 30px;">የምንሰጣቸው አገልግሎቶች</h2>
        <div class="service-grid">
            <div class="service-card">
                <i class="fas fa-palette service-icon"></i>
                <h3>ግራፊክስ ዲዛይን</h3>
                <p>ሎጎ፣ ባነር፣ መጽሐፍ ዲዛይን እና ለማህበራዊ ሚዲያ ማስታወቂያዎች በጥራት እናቀርባለን።</p>
            </div>
            <div class="service-card">
                <i class="fas fa-video service-icon"></i>
                <h3>ቪዲዮ ኤዲቲንግ</h3>
                <p>ለYouTube፣ TikTok እና ለተለያዩ ፕሮግራሞች የሚሆኑ ቪዲዮዎችን በዘመናዊ ጥበብ ኤዲት እናደርጋለን።</p>
            </div>
            <div class="service-card">
                <i class="fas fa-print service-icon"></i>
                <h3>የሕትመት ስራዎች</h3>
                <p>ማንኛውንም የሕትመት ውጤቶች በጥራት እና በታማኝነት ለደንበኞቻችን እናቀርባለን።</p>
            </div>
        </div>
    </div>

    <div id="gallery" class="content-section">
        <h2 style="text-align: center; color: var(--blue);">የስራዎቻችን ማሳያ</h2>
        <div class="gallery-grid">
            <div class="gallery-item"><img src="https://i.ibb.co/zhjkJXpm/20251219-224720.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/1fwpFk6H/20251216-002122.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/QF7PbLyj/20251215-155642.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/XN9qjfN/20251210-224030.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/pj0G79js/20251210-225324.png"></div>
<div class="gallery-item"><img src="https://i.ibb.co/PZBYcCN3/20251209-234129.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/PsqD4xFT/20251202-120100.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LLrvHzJ/20251205-104728.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fYH5CVpV/20251128-093307.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/fzPz8G2s/20251127-100038.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/zTn3fYKp/20260102-164217.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qMk0cqCf/20251230-112306.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/qLhqKJWR/20251230-073553.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/8nwp8rkQ/20251219-132621.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LzZCXn0y/20251205-122512.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/5XVVtK0q/20251122-144552.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/LhnMBPNF/20251120-202649.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/YB2q959t/20251120-200348.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/HTs32qzY/20251119-140559.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/v7RQtHD/20251118-215305.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/WNFRQj2H/20251118-200618.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d0KmLtSN/20251114-122726.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/FLLpDNv5/20251108-122343.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/d46N12Ms/20251109-184251.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/3yv4bm2Z/20251023-182429.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/vgz9sgX/20251005-123849.png"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/r2JxTnM2/20251003-164027.jpg"></div>
            <div class="gallery-item"><img src="https://i.ibb.co/21dLh2P5/20251106-082659.jpg"></div>
        </div>
    </div>

    <div id="about" class="content-section">
        <h2 style="color:var(--blue); text-align: center;">ስለ ማሕቤ ቢዝነስ ማዕከል</h2>
        <div style="background: white; padding: 30px; border-radius: 25px; line-height: 1.8; box-shadow: 0 5px 15px rgba(0,0,0,0.05);">
            <h3 style="color: var(--blue); border-bottom: 2px solid var(--yellow); display: inline-block;">የስማችን ትርጉም</h3>
            <p><strong>ማሕቤ</strong> ማለት ሁለት ታላላቅ ትርጉሞች ያሉት የማዕከል ስም ነው፦</p>
            <ul>
                <li><strong>ማሕፀነ ቤተክርስቲያን ሚዲያ፦</strong> መንፈሳዊ አገልግሎቶችን፣ የቅዳሴ ትምህርቶችን እና ስብከተ ወንጌልን በዘመናዊ ሚዲያ የምናቀርብበት ክፍል ነው።</li>
                <li><strong>ማሕቤ ሕትመት ቤት፦</strong> ማንኛውንም የዲዛይን እና የሕትመት ስራዎች በከፍተኛ ጥራት የምንሰራበት የንግድ ዘርፋችን ነው።</li>
            </ul>
            <p>ዓላማችን ደንበኞቻችንን በታማኝነት፣ በፍጥነት እና በጥራት በማገልገል የላቀ ውጤት እንዲያመጡ መርዳት ነው።</p>
        </div>
    </div>

    <div id="comment" class="content-section">
        <h2 style="text-align: center; color: var(--blue);">አስተያየትዎን ያጋሩን</h2>
        <div class="comment-form">
            <input type="text" id="userName" placeholder="ሙሉ ስምዎን ያስገቡ">
            <textarea id="userComment" rows="5" placeholder="አስተያየትዎን እዚህ ይጻፉ..."></textarea>
            <button class="send-btn" onclick="sendToTelegram()">
                <i class="fab fa-telegram-plane"></i> አስተያየቴን ላክ
            </button>
        </div>
    </div>

    <footer>
        <p>© 2026 ማሕቤ ቢዝነስ ማዕከል <br> 📞 0928525029 / 0971825151</p>
    </footer>

<script>
        function showSection(id) {
            const sections = document.getElementsByClassName('content-section');
            for (let s of sections) { s.style.display = 'none'; }
            document.getElementById(id).style.display = 'block';
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        function sendToTelegram() {
            const name = document.getElementById('userName').value;
            const comment = document.getElementById('userComment').value;
            if (name === "" || comment === "") { alert("እባክዎ ስም እና አስተያየት ያስገቡ!"); return; }
            const msg = ሰላም ማሕቤ! አስተያየት አለኝ%0A%0Aስም፦ ${name}%0Aአስተያየት፦ ${comment};
            window.open(https://t.me/temu_amen?text=${msg}, '_blank');
        }
    </script>
</body>
</html>
