<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CM Shri School - Chief Minister Schools of High Excellence, Research and Innovation</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1e40af;
            --primary-light: #3b82f6;
            --accent: #f59e0b;
            --accent-dark: #d97706;
            --text-dark: #1f2937;
            --text-light: #6b7280;
            --bg-light: #f9fafb;
            --bg-white: #ffffff;
            --border-color: #e5e7eb;
            --success: #10b981;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--text-dark);
            line-height: 1.6;
            background-color: var(--bg-white);
            overflow-x: hidden;
        }

        /* ===== NAVIGATION ===== */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
            z-index: 1000;
            transition: all 0.3s ease;
        }

        .nav-container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .gov-badge {
            background: var(--primary);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 4px;
            font-size: 0.7rem;
            font-weight: 700;
            text-transform: uppercase;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -0.5px;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
            transition: color 0.3s ease;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-buttons {
            display: flex;
            gap: 1rem;
        }

        .btn-admission {
            background: linear-gradient(135deg, var(--success), #059669);
            color: white;
            padding: 0.7rem 1.8rem;
            border: none;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(16, 185, 129, 0.3);
            text-decoration: none;
            display: inline-block;
        }

        .btn-admission:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(16, 185, 129, 0.4);
        }

        .btn-portal {
            background: transparent;
            color: var(--primary);
            padding: 0.7rem 1.8rem;
            border: 2px solid var(--primary);
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-portal:hover {
            background: var(--primary);
            color: white;
        }

        /* ===== HERO SECTION ===== */
        .hero {
            padding: 10rem 2rem 6rem;
            background: linear-gradient(135deg, #1e40af 0%, #3b82f6 50%, #dbeafe 100%);
            color: white;
            text-align: center;
            position: relative;
            overflow: hidden;
            margin-top: 70px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><defs><pattern id="grid" width="50" height="50" patternUnits="userSpaceOnUse"><path d="M 50 0 L 0 0 0 50" fill="none" stroke="rgba(255,255,255,0.05)" stroke-width="1"/></pattern></defs><rect width="1200" height="600" fill="url(%23grid)"/></svg>');
            pointer-events: none;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            margin: 0 auto;
            animation: fadeInUp 1s ease;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.2);
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
            font-weight: 600;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
            line-height: 1.2;
        }

        .hero-subtitle {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            opacity: 0.95;
            font-weight: 600;
        }

        .hero p {
            font-size: 1.1rem;
            margin-bottom: 2rem;
            opacity: 0.9;
            font-weight: 300;
            line-height: 1.8;
        }

        .hero-buttons {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn-primary {
            background: white;
            color: var(--primary);
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 6px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            text-decoration: none;
            display: inline-block;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.15);
        }

        .btn-secondary {
            background: transparent;
            color: white;
            padding: 1rem 2.5rem;
            border: 2px solid white;
            border-radius: 6px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-block;
        }

        .btn-secondary:hover {
            background: white;
            color: var(--primary);
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ===== QUICK LINKS SECTION ===== */
        .quick-links {
            padding: 3rem 2rem;
            background: var(--bg-light);
            border-top: 4px solid var(--accent);
        }

        .quick-links-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .quick-link-card {
            background: white;
            padding: 1.5rem;
            border-radius: 8px;
            text-align: center;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            text-decoration: none;
            color: var(--text-dark);
        }

        .quick-link-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        }

        .quick-link-icon {
            font-size: 2.5rem;
            margin-bottom: 0.8rem;
        }

        .quick-link-card h3 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            font-size: 1.1rem;
        }

        .quick-link-card p {
            color: var(--text-light);
            font-size: 0.9rem;
        }

        /* ===== FEATURES SECTION ===== */
        .features {
            padding: 6rem 2rem;
            background: white;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .section-title p {
            color: var(--text-light);
            font-size: 1.1rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: var(--bg-light);
            padding: 2.5rem;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
            border-top: 4px solid var(--accent);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
            background: white;
        }

        .feature-icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }

        .feature-card h3 {
            font-size: 1.3rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .feature-card p {
            color: var(--text-light);
            line-height: 1.8;
        }

        /* ===== ADMISSION INFO ===== */
        .admission-info {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, #f0f9ff 0%, #dbeafe 100%);
        }

        .admission-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .admission-content h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .admission-content p {
            margin-bottom: 1rem;
            color: var(--text-dark);
            line-height: 1.8;
        }

        .admission-checklist {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            margin-top: 2rem;
        }

        .checklist-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 1rem;
            color: var(--text-dark);
        }

        .checklist-item::before {
            content: '✓';
            display: flex;
            align-items: center;
            justify-content: center;
            width: 30px;
            height: 30px;
            background: var(--success);
            color: white;
            border-radius: 50%;
            font-weight: bold;
            flex-shrink: 0;
        }

        .admission-image {
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            padding: 3rem;
            border-radius: 10px;
            text-align: center;
            font-size: 6rem;
            box-shadow: 0 8px 25px rgba(30, 64, 175, 0.2);
        }

        .admission-btn {
            display: inline-block;
            background: var(--success);
            color: white;
            padding: 1rem 2rem;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 700;
            margin-top: 1.5rem;
            transition: all 0.3s ease;
        }

        .admission-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(16, 185, 129, 0.3);
        }

        /* ===== GOVERNMENT SCHOOL INFO ===== */
        .gov-info {
            padding: 6rem 2rem;
            background: white;
        }

        .gov-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .gov-card {
            background: linear-gradient(135deg, #fef3c7 0%, #fde68a 100%);
            padding: 2rem;
            border-radius: 10px;
            border-left: 5px solid var(--accent);
            transition: all 0.3s ease;
        }

        .gov-card:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(245, 158, 11, 0.2);
        }

        .gov-card h3 {
            color: var(--primary);
            font-size: 1.2rem;
            margin-bottom: 1rem;
        }

        .gov-card p {
            color: var(--text-dark);
            line-height: 1.8;
        }

        /* ===== CONTACT & FOOTER ===== */
        .contact {
            padding: 6rem 2rem;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: white;
        }

        .contact h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .contact-item {
            text-align: center;
            background: rgba(255, 255, 255, 0.1);
            padding: 2rem;
            border-radius: 10px;
            backdrop-filter: blur(10px);
        }

        .contact-item h3 {
            margin-bottom: 0.8rem;
            font-size: 1.2rem;
        }

        .contact-item p {
            opacity: 0.9;
        }

        .contact-item a {
            color: var(--accent);
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .contact-item a:hover {
            opacity: 0.8;
        }

        footer {
            background: #0f172a;
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }

        .footer-section h4 {
            margin-bottom: 1rem;
            color: var(--accent);
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.5rem;
        }

        .footer-section a {
            color: #cbd5e1;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section a:hover {
            color: var(--accent);
        }

        .footer-bottom {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 2rem;
            color: #94a3b8;
        }

        /* ===== RESPONSIVE ===== */
        @media (max-width: 768px) {
            .nav-links {
                gap: 1.5rem;
                font-size: 0.85rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero-buttons {
                flex-direction: column;
            }

            .btn-primary, .btn-secondary {
                width: 100%;
            }

            .admission-grid {
                grid-template-columns: 1fr;
            }

            .hero {
                padding: 8rem 1.5rem 4rem;
                margin-top: 60px;
            }

            .section-title h2 {
                font-size: 2rem;
            }

            .nav-buttons {
                flex-direction: column;
                width: 100%;
            }

            .btn-admission, .btn-portal {
                width: 100%;
            }
        }
    </style>
</head>
<body>

<!-- NAVIGATION -->
<nav>
    <div class="nav-container">
        <div class="logo-section">
            <span class="gov-badge">Delhi Government</span>
            <div class="logo">CM Shri School</div>
        </div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#features">Features</a></li>
            <li><a href="#admission">Admission</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="nav-buttons">
            <a href="https://www.edudel.nic.in/" target="_blank" class="btn-portal">DoE Portal</a>
            <a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank" class="btn-admission">Apply Now</a>
        </div>
    </div>
</nav>

<!-- HERO SECTION -->
<section class="hero" id="home">
    <div class="hero-content">
        <span class="hero-badge">🏆 Chief Minister Schools of High Excellence, Research & Innovation</span>
        <h1>Welcome to CM Shri School</h1>
        <p class="hero-subtitle">World-Class Education. Zero Tuition Fees. 100% Government Supported.</p>
        <p>Transforming Delhi's public education with modern infrastructure, expert faculty, and student-centric learning. Building tomorrow's leaders today.</p>
        <div class="hero-buttons">
            <a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank" class="btn-primary">Registration Portal</a>
            <a href="#features" class="btn-secondary">Learn More</a>
        </div>
    </div>
</section>

<!-- QUICK LINKS -->
<section class="quick-links">
    <div class="quick-links-container">
        <a href="https://www.edudel.nic.in/" target="_blank" class="quick-link-card">
            <div class="quick-link-icon">🏛️</div>
            <h3>Delhi Education</h3>
            <p>Official Directorate of Education Portal</p>
        </a>
        <a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank" class="quick-link-card">
            <div class="quick-link-icon">📝</div>
            <h3>Apply Online</h3>
            <p>CM Shri School Admission 2026-27</p>
        </a>
        <a href="tel:1800118700" class="quick-link-card">
            <div class="quick-link-icon">📞</div>
            <h3>Helpline</h3>
            <p>1800-11-8700 (Mon-Fri, 9 AM-5 PM)</p>
        </a>
    </div>
</section>

<!-- FEATURES SECTION -->
<section class="features" id="features">
    <div class="container">
        <div class="section-title">
            <h2>Why CM Shri Schools?</h2>
            <p>A revolutionary approach to government education in Delhi</p>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">💰</div>
                <h3>Completely Free</h3>
                <p>Zero tuition fees. Quality education accessible to all Delhi children regardless of economic background.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🏗️</div>
                <h3>Modern Infrastructure</h3>
                <p>State-of-the-art smart classrooms, digital labs, sports facilities, and technology-enabled learning spaces.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">👨‍🏫</div>
                <h3>Expert Faculty</h3>
                <p>Highly trained teachers with innovative teaching methods and continuous professional development.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🎓</div>
                <h3>Skill Development</h3>
                <p>Focus on 21st-century skills including coding, robotics, entrepreneurship, and soft skills.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🌍</div>
                <h3>Inclusive Education</h3>
                <p>Safe and supportive environment for all students with special attention to differently-abled learners.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">⭐</div>
                <h3>Holistic Development</h3>
                <p>Beyond academics - sports, arts, cultural activities, and leadership programs for all-round growth.</p>
            </div>
        </div>
    </div>
</section>

<!-- ADMISSION INFORMATION -->
<section class="admission-info" id="admission">
    <div class="container">
        <div class="admission-grid">
            <div class="admission-content">
                <h2>Admission 2026-27</h2>
                <p>CM Shri Schools offer admissions for multiple entry levels through a transparent, merit-based selection process.</p>
                <p><strong>Eligible Classes:</strong> Nursery, Class I, Class VI, Class IX, and Class XI</p>
                <p><strong>Eligibility:</strong> Students must be residents of Delhi. For Classes VI and above, an entrance examination is conducted.</p>
                
                <div class="admission-checklist">
                    <div class="checklist-item">Birth Certificate</div>
                    <div class="checklist-item">Aadhaar Card</div>
                    <div class="checklist-item">Residence Proof (Ration Card / Electricity Bill)</div>
                    <div class="checklist-item">Previous Class Marksheet</div>
                    <div class="checklist-item">Passport Size Photograph</div>
                </div>

                <a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank" class="admission-btn">Start Application</a>
            </div>
            <div class="admission-image">🎒</div>
        </div>
    </div>
</section>

<!-- GOVERNMENT SCHOOL INFORMATION -->
<section class="gov-info">
    <div class="container">
        <div class="section-title">
            <h2>About CM Shri Initiative</h2>
            <p>Delhi Government's commitment to transforming public education</p>
        </div>
        <div class="gov-grid">
            <div class="gov-card">
                <h3>📊 Coverage</h3>
                <p>75 schools upgraded across all districts of Delhi under CM SHRI initiative with plans to expand to 200+ schools by 2027.</p>
            </div>
            <div class="gov-card">
                <h3>🎯 Mission</h3>
                <p>Chief Minister Schools of High Excellence, Research and Innovation - providing world-class education following NEP 2020 guidelines.</p>
            </div>
            <div class="gov-card">
                <h3>📚 CBSE Affiliated</h3>
                <p>All CM Shri schools are CBSE affiliated and recognized as schools of special category with RTE 2009 provision.</p>
            </div>
            <div class="gov-card">
                <h3>🔬 Innovation Focus</h3>
                <p>Emphasis on STEM education, AI-enabled labs, vocational training, and research opportunities for students.</p>
            </div>
            <div class="gov-card">
                <h3>🌱 Sustainability</h3>
                <p>Green campus initiatives, sustainable infrastructure, and environmental education programs in all schools.</p>
            </div>
            <div class="gov-card">
                <h3>🤝 Community</h3>
                <p>Strong parent-teacher associations and community engagement for holistic student development.</p>
            </div>
        </div>
    </div>
</section>

<!-- CONTACT SECTION -->
<section class="contact" id="contact">
    <div class="container">
        <h2>Contact Information</h2>
        <div class="contact-grid">
            <div class="contact-item">
                <h3>🏫 Directorate of Education</h3>
                <p>Government of Delhi<br>Email: <a href="mailto:info@edudel.nic.in">info@edudel.nic.in</a></p>
            </div>
            <div class="contact-item">
                <h3>📱 Helpline</h3>
                <p>Call: <a href="tel:1800118700">1800-11-8700</a><br>Monday to Friday, 9 AM - 5 PM</p>
            </div>
            <div class="contact-item">
                <h3>🌐 Official Portal</h3>
                <p><a href="https://www.edudel.nic.in/" target="_blank">www.edudel.nic.in</a><br>Admission Link: <a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank">Apply Here</a></p>
            </div>
        </div>
    </div>
</section>

<!-- FOOTER -->
<footer>
    <div class="footer-content">
        <div class="footer-section">
            <h4>About</h4>
            <ul>
                <li><a href="https://www.edudel.nic.in/" target="_blank">Directorate of Education</a></li>
                <li><a href="#" onclick="alert('Visit edudel.nic.in')">CM Shri Schools</a></li>
                <li><a href="#" onclick="alert('Visit edudel.nic.in')">Policies</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Admission</h4>
            <ul>
                <li><a href="https://www.edudel.nic.in/cmshriapp/home.aspx" target="_blank">Online Registration</a></li>
                <li><a href="#" onclick="alert('Entrance test details available on edudel.nic.in')">Entrance Test</a></li>
                <li><a href="#" onclick="alert('Check edudel.nic.in for updates')">Eligibility</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Resources</h4>
            <ul>
                <li><a href="https://www.edudel.nic.in/" target="_blank">DoE Portal</a></li>
                <li><a href="tel:1800118700">Helpline: 1800-11-8700</a></li>
                <li><a href="mailto:info@edudel.nic.in">Email Support</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <h4>Follow Us</h4>
            <ul>
                <li><a href="#" onclick="alert('Check official DoE social media')">Facebook</a></li>
                <li><a href="#" onclick="alert('Check official DoE social media')">Instagram</a></li>
                <li><a href="#" onclick="alert('Check official DoE social media')">Twitter</a></li>
            </ul>
        </div>
    </div>
    <div class="footer-bottom">
        <p>&copy; 2026 Delhi Directorate of Education - CM Shri Schools Initiative | Innovate, Inspire, Illuminate</p>
        <p style="margin-top: 1rem; font-size: 0.85rem;">Official Portal: <a href="https://www.edudel.nic.in/" target="_blank" style="color: var(--accent);">www.edudel.nic.in</a></p>
    </div>
</footer>

<script>
    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        });
    });

    // Scroll animation
    window.addEventListener('scroll', function() {
        const nav = document.querySelector('nav');
        if (window.scrollY > 50) {
            nav.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.1)';
        } else {
            nav.style.boxShadow = '0 2px 20px rgba(0, 0, 0, 0.08)';
        }
    });
</script>

</body>
</html>
