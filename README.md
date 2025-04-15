<!DOCTYPE html>

<html lang="vi">
<head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>KhĂ¡m phĂ¡ cĂ¡c nghá» á»©ng dá»¥ng tin há»c â€“ HÆ°á»›ng nghiá»‡p IT</title>
<meta content="KhĂ¡m phĂ¡ cĂ¡c ngĂ nh nghá» liĂªn quan Ä‘áº¿n tin há»c nhÆ° láº­p trĂ¬nh, an ninh máº¡ng, thiáº¿t káº¿ web... cĂ¹ng Ä‘á»‹nh hÆ°á»›ng thi tuyá»ƒn vĂ  thĂ´ng tin há»¯u Ă­ch." name="description"/>
<link href="favicon.ico" rel="icon" type="image/x-icon"/>
<!-- ThĂªm font Google -->
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&amp;display=swap" rel="stylesheet"/>
<!-- ThĂªm Font Awesome -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet"/>
<style>
        :root {
            --primary-color: #2e7d32;
            --secondary-color: #00bcd4;
            --dark-color: #333;
            --light-color: #f0f4f7;
            --success-color: #4CAF50;
            --card-bg: #e8f5e9;
            --card-border: #c8e6c9;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--light-color);
            color: var(--dark-color);
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            text-align: center;
            padding: 60px 20px;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1555066931-4365d14bab8c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') center/cover;
            opacity: 0.2;
            z-index: 0;
        }

        header h1, header p {
            position: relative;
            z-index: 1;
        }

        header h1 {
            font-size: 2.8em;
            margin-bottom: 20px;
            text-transform: uppercase;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.3em;
            max-width: 800px;
            margin: 0 auto;
        }

        /* Navigation improvements */
        nav {
            background-color: var(--dark-color);
            padding: 15px 0;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .nav-links {
            display: flex;
            gap: 20px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 1.1em;
            font-weight: 500;
            position: relative;
            transition: all 0.3s ease;
            padding: 8px 12px;
            border-radius: 4px;
        }

        nav a:hover {
            color: var(--secondary-color);
            background-color: rgba(255,255,255,0.1);
        }

        nav a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: 0;
            left: 0;
            background-color: var(--secondary-color);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        .dropdown {
            position: relative;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: var(--dark-color);
            min-width: 220px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            z-index: 1;
            border-radius: 4px;
            top: 100%;
            left: 0;
            opacity: 0;
            transform: translateY(10px);
            transition: all 0.3s ease;
        }

        .dropdown:hover .dropdown-content {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }

        .dropdown-content a {
            padding: 12px 16px;
            display: block;
            text-align: left;
            font-size: 1em;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .dropdown-content a:hover {
            background-color: rgba(255,255,255,0.1);
            color: var(--secondary-color);
        }

        /* Main content improvements */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 40px auto;
            padding: 30px;
            background-color: #fff;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
        }

        h2 {
            text-align: center;
            color: var(--primary-color);
            margin-bottom: 40px;
            font-size: 2.2em;
            position: relative;
            padding-bottom: 15px;
        }

        h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
        }

        .careers {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .career-card {
            background-color: var(--card-bg);
            border: 1px solid var(--card-border);
            padding: 25px;
            border-radius: 10px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .career-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-color), var(--secondary-color));
            transition: width 0.3s ease;
        }

        .career-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.12);
        }

        .career-card:hover::before {
            width: 8px;
        }

        .career-card h3 {
            color: var(--primary-color);
            margin-bottom: 15px;
            font-size: 1.5em;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .career-card h3 i {
            color: var(--secondary-color);
        }

        .career-card p {
            margin-bottom: 15px;
        }

        .career-card .details {
            display: none;
            margin-top: 15px;
            padding-top: 15px;
            border-top: 1px dashed #ccc;
        }

        .career-card:hover .details {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* External links section */
        .external-links {
            text-align: center;
            margin: 60px 0 40px;
        }

        .external-links h2 {
            margin-bottom: 30px;
        }

        .resource-cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .resource-card {
            background: white;
            border-radius: 8px;
            padding: 20px;
            width: 280px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .resource-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .resource-card i {
            font-size: 2.5em;
            color: var(--secondary-color);
            margin-bottom: 15px;
        }

        .resource-card h3 {
            margin-bottom: 10px;
            color: var(--primary-color);
        }

        .resource-card a {
            display: inline-block;
            margin-top: 15px;
            color: var(--secondary-color);
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .resource-card a:hover {
            color: var(--primary-color);
            text-decoration: underline;
        }

        /* Contact form improvements */
        .contact {
            background: linear-gradient(135deg, var(--dark-color), #222);
            color: white;
            padding: 60px 40px;
            margin-top: 60px;
            border-radius: 12px;
            position: relative;
            overflow: hidden;
        }

        .contact::before {
            content: '';
            position: absolute;
            top: -50%;
            right: -50%;
            width: 100%;
            height: 200%;
            background: radial-gradient(circle, rgba(0,188,212,0.1) 0%, rgba(0,0,0,0) 70%);
        }

        .contact h2 {
            color: white;
            position: relative;
        }

        .contact h2::after {
            background: linear-gradient(to right, var(--secondary-color), white);
        }

        .contact form {
            max-width: 700px;
            margin: 0 auto;
            position: relative;
        }

        .form-group {
            margin-bottom: 25px;
        }

        .contact label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .contact input,
        .contact textarea,
        .contact select {
            width: 100%;
            padding: 15px;
            border-radius: 8px;
            border: 2px solid rgba(255,255,255,0.2);
            background-color: rgba(255,255,255,0.1);
            color: white;
            font-size: 1em;
            transition: all 0.3s ease;
        }

        .contact input:focus,
        .contact textarea:focus,
        .contact select:focus {
            outline: none;
            border-color: var(--secondary-color);
            background-color: rgba(255,255,255,0.2);
        }

        .contact input::placeholder,
        .contact textarea::placeholder {
            color: rgba(255,255,255,0.7);
        }

        .contact button {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 15px 40px;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.1em;
            font-weight: 500;
            transition: all 0.3s ease;
            display: block;
            margin: 30px auto 0;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .contact button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
            background: linear-gradient(to right, var(--secondary-color), var(--primary-color));
        }

        /* Footer improvements */
        footer {
            background-color: var(--dark-color);
            color: white;
            text-align: center;
            padding: 40px 20px;
            margin-top: 80px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            text-align: left;
        }

        .footer-column h3 {
            color: var(--secondary-color);
            margin-bottom: 20px;
            font-size: 1.3em;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #ddd;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-column ul li a:hover {
            color: var(--secondary-color);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            color: white;
            background-color: rgba(255,255,255,0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background-color: var(--secondary-color);
            transform: translateY(-3px);
        }

        .copyright {
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Back to top button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            background-color: var(--secondary-color);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2em;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 4px 12px rgba(0,0,0,0.2);
            z-index: 999;
        }

        .back-to-top.active {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px);
        }

        /* Responsive improvements */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2em;
            }
            
            header p {
                font-size: 1.1em;
            }
            
            nav .nav-container {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-links {
                flex-direction: column;
                width: 100%;
            }
            
            .dropdown-content {
                position: static;
                width: 100%;
                box-shadow: none;
                display: none;
                opacity: 1;
                transform: none;
            }
            
            .dropdown:hover .dropdown-content {
                display: block;
            }
            
            .container {
                padding: 20px;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
<!-- Back to top button -->
<div class="back-to-top">
<i class="fas fa-arrow-up"></i>
</div>
<header>
<h1>CĂ¡c Nghá» CĂ³ á»¨ng Dá»¥ng Tin Há»c</h1>
<p>KhĂ¡m phĂ¡ nhá»¯ng nghá» nghiá»‡p thĂº vá»‹ vĂ  Ä‘áº§y triá»ƒn vá»ng trong ngĂ nh cĂ´ng nghá»‡ thĂ´ng tin</p>
</header>
<nav>
<div class="nav-container">
<div class="logo">
<a href="https://itviec.com/viec-lam-it?job_selected=bridge-engineer-brse-project-manager-persol-career-tech-studio-vietnam-1016">IT Career</a>
</div>
<div class="nav-links">
<div class="dropdown">
<a href="https://www.topcv.vn/xin-viec-nganh-cong-nghe-thong-tin"><i class="fas fa-home"></i> Trang chá»§</a>
</div>
<div class="dropdown">
<a href="#"><i class="fas fa-info-circle"></i> Giá»›i thiá»‡u</a>
<div class="dropdown-content">
<a href="https://careerviet.vn/vi/talentcommunity/wiki-career/lap-trinh-vien-la-gi-cong-viec-cua-mot-lap-trinh-vien.35A51E5A.html#:~:text=L%E1%BA%ADp%20tr%C3%ACnh%20vi%C3%AAn%20(ti%E1%BA%BFng%20anh,%2C%20m%C3%A1y%20t%C3%ADnh%2C..."><i class="fas fa-code"></i> Láº­p TrĂ¬nh ViĂªn</a>
<a href="https://hrchannels.com/uptalent/ky-su-mang-la-gi.html"><i class="fas fa-network-wired"></i> Ká»¹ SÆ° Máº¡ng</a>
<a href="https://www.hotcourses.vn/study-abroad-info/study-guides/nganh-an-ninh-mang/"><i class="fas fa-shield-alt"></i> An Ninh Máº¡ng</a>
<a href="https://jobsgo.vn/blog/thiet-ke-web-hoc-nganh-gi/"><i class="fas fa-paint-brush"></i> Thiáº¿t Káº¿ Web</a>
</div>
</div>
<div class="dropdown">
<a href="#"><i class="fas fa-briefcase"></i> CĂ¡c nghá»</a>
<div class="dropdown-content">
<a href="https://caodangbachkhoa.edu.vn/xet-tuyen-nganh-lap-trinh-may-tinh/"><i class="fas fa-laptop-code"></i> Láº­p TrĂ¬nh ViĂªn - A00, A01</a>
<a href="https://tuyensinh.vku.udn.vn/cntt-ks"><i class="fas fa-server"></i> Ká»¹ SÆ° Máº¡ng - A00, A01</a>
<a href="https://thuvienphapluat.vn/phap-luat/ho-tro-phap-luat/chi-tieu-tuyen-sinh-dai-hoc-nganh-nghiep-vu-an-ninh-an-ninh-mang-va-pctp-su-dung-cong-nghe-cao-cua--142264.html"><i class="fas fa-user-secret"></i> An Ninh Máº¡ng - A00, A01</a>
<a href="https://portal.vku.udn.vn/tin-tuc-va-hoat-dong/tin-tuc-hoat-dong/nghe-thiet-ke-web-chuyen-nghiep-web-designer.html"><i class="fas fa-desktop"></i> Thiáº¿t Káº¿ Web - A00, A01</a>
<a href="https://tuyensinhhot.com/tuyen-sinh/thong-tin-tuyen-sinh-quang-tri-mang-may-tinh-truong-cao-ang-nghe-a-lat"><i class="fas fa-cogs"></i> Quáº£n Trá»‹ Máº¡ng - A00, A01</a>
<a href="https://tuyensinh.vnuk.udn.vn/tuyen-sinh-dai-hoc/cong-nghe-phan-mem/"><i class="fas fa-mobile-alt"></i> PhĂ¡t Triá»ƒn Pháº§n Má»m - A00, A01</a>
</div>
</div>
<a href="#contact"><i class="fas fa-envelope"></i> LiĂªn há»‡</a>
</div>
</div>
</nav>
<div class="container">
<h2>Giá»›i thiá»‡u vá» cĂ¡c nghá» á»©ng dá»¥ng tin há»c</h2>
<p style="text-align: center; margin-bottom: 30px; max-width: 800px; margin-left: auto; margin-right: auto;">
            NgĂ nh CĂ´ng nghá»‡ thĂ´ng tin Ä‘ang phĂ¡t triá»ƒn máº¡nh máº½ vá»›i nhiá»u cÆ¡ há»™i nghá» nghiá»‡p háº¥p dáº«n. 
            DÆ°á»›i Ä‘Ă¢y lĂ  nhá»¯ng nghá» nghiá»‡p tiĂªu biá»ƒu trong lÄ©nh vá»±c nĂ y mĂ  báº¡n cĂ³ thá»ƒ tham kháº£o.
        </p>
<div class="careers">
<div class="career-card">
<h3><i class="fas fa-laptop-code"></i> Láº­p TrĂ¬nh ViĂªn</h3>
<p>Thiáº¿t káº¿, phĂ¡t triá»ƒn pháº§n má»m vĂ  á»©ng dá»¥ng, lĂ  xÆ°Æ¡ng sá»‘ng cá»§a má»i há»‡ thá»‘ng cĂ´ng nghá»‡ hiá»‡n Ä‘áº¡i.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01, D07</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 15-50 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>CĂ¡c trÆ°á»ng Ä‘Ă o táº¡o:</strong> BĂ¡ch Khoa, Khoa há»c Tá»± nhiĂªn, FPT, ...</p>
</div>
</div>
<div class="career-card">
<h3><i class="fas fa-network-wired"></i> Ká»¹ SÆ° Máº¡ng</h3>
<p>XĂ¢y dá»±ng vĂ  duy trĂ¬ há»‡ thá»‘ng máº¡ng mĂ¡y tĂ­nh, Ä‘áº£m báº£o káº¿t ná»‘i á»•n Ä‘á»‹nh vĂ  báº£o máº­t cho tá»• chá»©c.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 12-40 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>Chá»©ng chá»‰ quan trá»ng:</strong> CCNA, CCNP</p>
</div>
</div>
<div class="career-card">
<h3><i class="fas fa-shield-alt"></i> ChuyĂªn ViĂªn An Ninh Máº¡ng</h3>
<p>Báº£o vá»‡ dá»¯ liá»‡u vĂ  há»‡ thá»‘ng khá»i cĂ¡c cuá»™c táº¥n cĂ´ng máº¡ng, Ä‘áº£m báº£o an toĂ n thĂ´ng tin.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 20-60 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>Ká»¹ nÄƒng cáº§n cĂ³:</strong> Ethical Hacking, Cryptography</p>
</div>
</div>
<div class="career-card">
<h3><i class="fas fa-paint-brush"></i> Thiáº¿t Káº¿ Web</h3>
<p>Táº¡o ra giao diá»‡n vĂ  tráº£i nghiá»‡m ngÆ°á»i dĂ¹ng trĂªn cĂ¡c trang web hiá»‡n Ä‘áº¡i, tháº©m má»¹ vĂ  thĂ¢n thiá»‡n.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01, D14</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 10-35 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>CĂ´ng cá»¥ phá»• biáº¿n:</strong> Figma, Adobe XD, Photoshop</p>
</div>
</div>
<div class="career-card">
<h3><i class="fas fa-database"></i> Quáº£n Trá»‹ CÆ¡ Sá»Ÿ Dá»¯ Liá»‡u</h3>
<p>Quáº£n lĂ½, báº£o trĂ¬ vĂ  tá»‘i Æ°u hĂ³a há»‡ thá»‘ng cÆ¡ sá»Ÿ dá»¯ liá»‡u cho doanh nghiá»‡p.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 15-45 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>Há»‡ quáº£n trá»‹ phá»• biáº¿n:</strong> MySQL, SQL Server, Oracle</p>
</div>
</div>
<div class="career-card">
<h3><i class="fas fa-mobile-alt"></i> PhĂ¡t Triá»ƒn á»¨ng Dá»¥ng Di Äá»™ng</h3>
<p>XĂ¢y dá»±ng cĂ¡c á»©ng dá»¥ng trĂªn ná»n táº£ng iOS vĂ  Android Ä‘Ă¡p á»©ng nhu cáº§u ngÆ°á»i dĂ¹ng.</p>
<div class="details">
<p><strong>Tá»• há»£p xĂ©t tuyá»ƒn:</strong> A00, A01, D01</p>
<p><strong>Má»©c lÆ°Æ¡ng trung bĂ¬nh:</strong> 15-50 triá»‡u VNÄ/thĂ¡ng</p>
<p><strong>CĂ´ng nghá»‡ phá»• biáº¿n:</strong> Flutter, React Native, Swift, Kotlin</p>
</div>
</div>
</div>
</div>
<div class="container">
<div class="external-links">
<h2>TĂ i NguyĂªn Há»¯u Ăch</h2>
<p>KhĂ¡m phĂ¡ thĂªm cĂ¡c nguá»“n tĂ i nguyĂªn Ä‘á»ƒ há»— trá»£ Ä‘á»‹nh hÆ°á»›ng nghá» nghiá»‡p cá»§a báº¡n</p>
<div class="resource-cards">
<div class="resource-card">
<i class="fas fa-graduation-cap"></i>
<h3>HÆ°á»›ng Nghiá»‡p</h3>
<p>CĂ¡c khĂ³a há»c vĂ  tĂ i liá»‡u hÆ°á»›ng nghiá»‡p trong lÄ©nh vá»±c CNTT</p>
<a href="https://www.coursera.org/" target="_blank">Xem thĂªm <i class="fas fa-arrow-right"></i></a>
</div>
<div class="resource-card">
<i class="fas fa-book"></i>
<h3>TĂ i Liá»‡u Há»c Táº­p</h3>
<p>SĂ¡ch vĂ  tĂ i liá»‡u tham kháº£o cho cĂ¡c ngĂ nh nghá» CNTT</p>
<a href="https://www.oreilly.com/" target="_blank">Xem thĂªm <i class="fas fa-arrow-right"></i></a>
</div>
<div class="resource-card">
<i class="fas fa-newspaper"></i>
<h3>Tin Tá»©c CĂ´ng Nghá»‡</h3>
<p>Cáº­p nháº­t xu hÆ°á»›ng vĂ  tin tá»©c má»›i nháº¥t vá» ngĂ nh CNTT</p>
<a href="https://vnexpress.net/" target="_blank">Xem thĂªm <i class="fas fa-arrow-right"></i></a>
</div>
</div>
</div>
</div>
<div class="contact" id="contact">
<h2>LiĂªn Há»‡ TÆ° Váº¥n</h2>
<p style="text-align: center; margin-bottom: 30px; max-width: 700px; margin-left: auto; margin-right: auto;">
            Báº¡n cĂ³ tháº¯c máº¯c vá» ngĂ nh há»c, nghá» nghiá»‡p hoáº·c cáº§n tÆ° váº¥n hÆ°á»›ng nghiá»‡p? 
            HĂ£y Ä‘á»ƒ láº¡i thĂ´ng tin, chĂºng tĂ´i sáº½ liĂªn há»‡ vá»›i báº¡n trong thá»i gian sá»›m nháº¥t.
        </p>
<form>
<div class="form-group">
<label for="name"><i class="fas fa-user"></i> Há» tĂªn</label>
<input id="name" placeholder="Nháº­p há» tĂªn cá»§a báº¡n" required="" type="text"/>
</div>
<div class="form-group">
<label for="email"><i class="fas fa-envelope"></i> Email</label>
<input id="email" placeholder="Nháº­p Ä‘á»‹a chá»‰ email" required="" type="email"/>
</div>
<div class="form-group">
<label for="phone"><i class="fas fa-phone"></i> Sá»‘ Ä‘iá»‡n thoáº¡i</label>
<input id="phone" placeholder="Nháº­p sá»‘ Ä‘iá»‡n thoáº¡i" type="tel"/>
</div>
<div class="form-group">
<label for="interest"><i class="fas fa-star"></i> Báº¡n quan tĂ¢m Ä‘áº¿n nghá» nĂ o?</label>
<select id="interest">
<option value="">-- Chá»n nghá» quan tĂ¢m --</option>
<option value="programmer">Láº­p trĂ¬nh viĂªn</option>
<option value="network">Ká»¹ sÆ° máº¡ng</option>
<option value="security">An ninh máº¡ng</option>
<option value="design">Thiáº¿t káº¿ web</option>
<option value="other">KhĂ¡c</option>
</select>
</div>
<div class="form-group">
<label for="message"><i class="fas fa-comment"></i> Lá»i nháº¯n</label>
<textarea id="message" placeholder="Nháº­p ná»™i dung báº¡n muá»‘n tÆ° váº¥n..." required="" rows="5"></textarea>
</div>
<button type="submit"><i class="fas fa-paper-plane"></i> Gá»­i yĂªu cáº§u</button>
</form>
</div>
<footer>
<div class="footer-content">
<div class="footer-column">
<h3>Vá» ChĂºng TĂ´i</h3>
<p>ChĂºng tĂ´i lĂ  nhĂ³m 4 tĂ i nÄƒng, xĂ¢y dá»±ng website nháº±m Ä‘á»‹nh hÆ°á»›ng nghá» nghiá»‡p trong lÄ©nh vá»±c CĂ´ng nghá»‡ ThĂ´ng tin. Trang web mang Ä‘áº¿n cĂ¡i nhĂ¬n tá»•ng quan vá» cĂ¡c ngĂ nh nghá» nhÆ° láº­p trĂ¬nh, an ninh máº¡ng, thiáº¿t káº¿ web, v.v... NgoĂ i ra, ngÆ°á»i dĂ¹ng cĂ³ thá»ƒ tĂ¬m tháº¥y thĂ´ng tin tuyá»ƒn sinh, ká»¹ nÄƒng cáº§n thiáº¿t vĂ  cĂ¡c tĂ i nguyĂªn há»¯u Ă­ch Ä‘á»ƒ phĂ¡t triá»ƒn báº£n thĂ¢n.</p>
<div class="social-links">
<a href="#"><i class="fab fa-facebook-f"></i></a>
<a href="#"><i class="fab fa-twitter"></i></a>
<a href="#"><i class="fab fa-linkedin-in"></i></a>
<a href="#"><i class="fab fa-youtube"></i></a>
</div>
</div>


<div class="footer-column">
<h3>ThĂ´ng Tin LiĂªn Há»‡</h3>
<ul>
<li><i class="fas fa-map-marker-alt"></i> nhom4tainang</li>
<li><i class="fas fa-phone"></i> 0379426277</li>
<li><i class="fas fa-envelope"></i> motnguolamhet@gmail.com</li>
</ul>
</div>
</div>
<div class="copyright">
<p>Â© 2025 NhĂ³m 4 TĂ i NÄƒng. Báº£n quyá»n thuá»™c vá» nhĂ³m 4 ngÆ°á»i tĂ i lÄƒng(mpk tĂ i lÄƒng) hjhj.</p>
</div>
</footer>
<script>
        // Back to top button
        const backToTopButton = document.querySelector('.back-to-top');
        
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.add('active');
            } else {
                backToTopButton.classList.remove('active');
            }
        });
        
        backToTopButton.addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Form submission handling
        const contactForm = document.querySelector('.contact form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                
                // Here you would normally send the form data to a server
                alert('Cáº£m Æ¡n báº¡n Ä‘Ă£ gá»­i thĂ´ng tin! ChĂºng tĂ´i sáº½ liĂªn há»‡ vá»›i báº¡n sá»›m nháº¥t cĂ³ thá»ƒ.');
                this.reset();
            });
        }
    </script>
</body>
</html>
