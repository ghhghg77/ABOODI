# ABOODI
موقي
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ABOOD</title>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap" rel="stylesheet">
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      font-family: 'Cairo', sans-serif;
      overflow: hidden;
      color: white;
    }

    #bg-video {
      position: fixed;
      top: 0;
      left: 0;
      min-width: 100%;
      min-height: 100%;
      object-fit: cover;
      z-index: -1;
    }

    .overlay {
      background: rgba(0, 0, 0, 0.6);
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: 0;
    }

    .container {
      position: relative;
      z-index: 1;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
      text-align: center;
    }

    .profile-img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 2px solid white;
      margin-bottom: 15px;
      object-fit: cover;
    }

    .username {
      font-size: 2rem;
      font-weight: bold;
    }

    .username i {
      color: #bb66cc;
      margin-right: 5px;
    }

    .quote {
      margin: 10px 0 30px;
      font-size: 1.1rem;
      color: #ccc;
    }

    .info-boxes {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }

    .box {
      border-radius: 15px;
      padding: 20px;
      min-width: 200px;
      backdrop-filter: blur(10px);
      color: #fff;
    }

    .snap-box {
      background-color: #FFEB3B;
      color: #000;
      border: 1px solid #fff;
    }

    .insta-box {
      background-color: #C13584;
      border: 1px solid #fff;
    }

    .box-title {
      font-weight: bold;
      margin-bottom: 5px;
    }

    .footer {
      margin-top: 30px;
      font-size: 0.9rem;
      color: #aaa;
      display: flex;
      gap: 15px;
      align-items: center;
      justify-content: center;
    }

    .footer i {
      margin-left: 5px;
    }

    .social {
      margin-top: 20px;
    }

    .social a {
      color: white;
      margin: 0 10px;
      font-size: 1.4rem;
      transition: 0.3s;
    }

    .social a:hover {
      color: #bbb;
    }

    a {
      text-decoration: none;
    }
  </style>
</head>
<body>

<!-- خلفية الفيديو -->
<video autoplay muted loop id="bg-video">
  <source src="videoplayback.webm" type="video/webm">
  متصفحك لا يدعم تشغيل الفيديو.
</video>

<div class="overlay"></div>

<div class="container">
  <!-- الصورة -->
  <img src="https://i.imgur.com/fxQbC8B.png" alt="profile" class="profile-img"> <!-- غيّر الرابط لو تبي صورتك -->
  
  <!-- الاسم -->
  <div class="username"><i class="fas fa-gem"></i> ABOOD</div>
  
  <!-- النص الوصفي -->
  <div class="quote">في نهاية المطاف، ستبقى لحظة عابرة في ذاكرة أحدهم</div>

  <!-- البوكسات -->
  <div class="info-boxes">
    <div class="box snap-box">
      <div class="box-title">Snapchat</div>
      <div><a href="https://www.snapchat.com/add/y-oq2" target="_blank">@y-oq2</a></div>
    </div>
    <div class="box insta-box">
      <div class="box-title">Instagram</div>
      <div><a href="https://www.instagram.com/6p_z" target="_blank" style="color:#fff;">@6p_z</a></div>
    </div>
  </div>

  <!-- روابط السوشال -->
  <div class="social">
    <a href="https://www.snapchat.com/add/y-oq2"><i class="fab fa-snapchat-ghost"></i></a>
    <a href="https://www.instagram.com/6p_z"><i class="fab fa-instagram"></i></a>
    <a href="#"><i class="fab fa-discord"></i></a>
  </div>

  <!-- عدد الزيارات والموقع -->
  <div class="footer">
    <span><i class="fas fa-eye"></i> <span id="visitorCount">0</span></span>
    <span><i class="fas fa-map-marker-alt"></i> Makkah Al-Mukarramah</span>
  </div>
</div>

<!-- سكربت عداد الزيارات -->
<script>
  // عداد الزيارات المحلي (LocalStorage)
  let visits = localStorage.getItem('visitCount');
  if (!visits) {
    visits = 1;
  } else {
    visits = parseInt(visits) + 1;
  }
  localStorage.setItem('visitCount', visits);
  document.getElementById('visitorCount').innerText = visits.toLocaleString();
</script>

</body>
</html>
