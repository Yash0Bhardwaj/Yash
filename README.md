<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Viksit Bharat - Digital Technology for All</title>
    <style>
        /* New Color Theme */
        :root {
            --primary-color: #4169E1;  /* Royal Blue */
            --secondary-color: #1E90FF; /* Dodger Blue */
            --accent-color: #0A0A0A;   /* Near Black */
            --text-color: #E0E0E0;     /* Light Gray */
            --light-color: #121212;    /* Dark Background */
            --card-bg: #1E1E1E;        /* Card Background */
        }
        
        /* Silk Background Canvas */
        #silk-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: var(--accent-color);
            opacity: 0.97;
        }
        
        /* Base Styles */
        body {
            line-height: 1.6;
            color: var(--text-color);
            background: transparent;
            position: relative;
        }
        
        a {
            text-decoration: none;
            color: var(--secondary-color);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: white;
            padding: 12px 25px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }
        
        .btn:hover {
            background: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(65, 105, 225, 0.4);
        }
        
        /* Header Styles */
        header {
            background-color: rgba(10, 10, 10, 0.9);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.3);
            position: fixed;
            width: 100%;
            z-index: 100;
            backdrop-filter: blur(10px);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: bold;
            color: var(--secondary-color);
        }
        
        .logo span {
            color: var(--primary-color);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            font-weight: 500;
            transition: color 0.3s ease;
            color: var(--text-color);
        }
        
        .nav-links a:hover {
            color: var(--secondary-color);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
            color: var(--text-color);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
            position: relative;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: white;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
        }
        
        .hero p {
            font-size: 1.3rem;
            margin-bottom: 30px;
            color: var(--text-color);
        }
        
        /* About Section */
        .about {
            padding: 120px 0;
            background: linear-gradient(to bottom, rgba(10, 10, 10, 0.9), rgba(18, 18, 18, 0.95));
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            color: var(--secondary-color);
            font-size: 2.5rem;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 3px;
            background: var(--primary-color);
            margin: 15px auto 0;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            color: var(--secondary-color);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(65, 105, 225, 0.2);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Initiatives Section */
        .initiatives {
            padding: 120px 0;
            background: var(--light-color);
        }
        
        .initiatives-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }
        
        .initiative-card {
            background: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(65, 105, 225, 0.1);
        }
        
        .initiative-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(65, 105, 225, 0.2);
        }
        
        .card-image {
            height: 200px;
            overflow: hidden;
            position: relative;
        }
        
        .card-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, transparent 70%, rgba(10, 10, 10, 0.8));
        }
        
        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .initiative-card:hover .card-image img {
            transform: scale(1.1);
        }
        
        .card-content {
            padding: 25px;
        }
        
        .card-content h3 {
            margin-bottom: 15px;
            color: var(--secondary-color);
        }
        .infrastructure-section,
.green-energy-section,
.military-section {
    padding: 100px 0;
    background: linear-gradient(to bottom, rgba(18,18,18,0.95), #0A0A0A);
}

.content-wrapper {
    display: flex;
    align-items: center;
    gap: 60px;
    margin-top: 50px;
}

.content-wrapper.reverse {
    flex-direction: row-reverse;
}

.image-container {
    flex: 1;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 15px 30px rgba(0,0,0,0.4);
}

.image-container img {
    width: 100%;
    height: 500px;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.image-container:hover img {
    transform: scale(1.03);
}

.text-content {
    flex: 1;
}

.text-content h3 {
    color: var(--secondary-color);
    font-size: 1.8rem;
    margin-bottom: 25px;
}

.text-content ul {
    margin: 25px 0;
    padding-left: 20px;
}

.text-content li {
    margin-bottom: 12px;
    position: relative;
    padding-left: 25px;
}

.text-content li:before {
    content: "•";
    color: var(--primary-color);
    font-size: 1.5rem;
    position: absolute;
    left: 0;
    top: -5px;
}

.stats {
    display: flex;
    gap: 30px;
    margin-top: 40px;
}

.stat-item {
    text-align: center;
}

.stat-number {
    display: block;
    font-size: 2.2rem;
    font-weight: 700;
    color: var(--primary-color);
    line-height: 1;
}

.stat-label {
    font-size: 0.9rem;
    opacity: 0.8;
}

.impact-statement {
    background: rgba(65,105,225,0.1);
    border-left: 4px solid var(--primary-color);
    padding: 20px;
    margin: 30px 0;
    display: flex;
    gap: 15px;
    align-items: center;
}

.impact-statement i {
    font-size: 2rem;
    color: #4CAF50;
}

/* Military Tech Highlights */
.tech-highlights {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin-top: 30px;
}

.tech-item {
    background: rgba(30, 30, 30, 0.7);
    padding: 20px;
    border-radius: 8px;
    border-left: 3px solid var(--primary-color);
}

.tech-item h4 {
    color: var(--secondary-color);
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.tech-item i {
    color: var(--primary-color);
}

/* Responsive Adjustments */
@media (max-width: 992px) {
    .content-wrapper {
        flex-direction: column;
    }
    
    .content-wrapper.reverse {
        flex-direction: column;
    }
    
    .image-container img {
        height: 400px;
    }
}

@media (max-width: 576px) {
    .stats {
        flex-direction: column;
        gap: 15px;
    }
    
    .image-container img {
        height: 300px;
    }
}
        /* Stories Section */
        .stories {
            padding: 120px 0;
            background: linear-gradient(to bottom, rgba(18, 18, 18, 0.95), rgba(10, 10, 10, 0.9));
        }
        
        .story {
            display: flex;
            align-items: center;
            gap: 50px;
            margin-bottom: 70px;
        }
        
        .story:nth-child(even) {
            flex-direction: row-reverse;
        }
        
        .story-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(65, 105, 225, 0.2);
        }
        
        .story-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .story-text {
            flex: 1;
        }
        
        .story-text h3 {
            color: var(--secondary-color);
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        
        .story-text p {
            margin-bottom: 15px;
        }
        
        /* Get Involved Section */
        .get-involved {
            padding: 120px 0;
            background: var(--light-color);
            text-align: center;
        }
        
        .get-involved p {
            max-width: 700px;
            margin: 0 auto 50px;
            font-size: 1.1rem;
        }
        
        .involvement-options {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 50px;
            flex-wrap: wrap;
        }
        
        .option-card {
            background: var(--card-bg);
            padding: 40px 30px;
            border-radius: 10px;
            width: 320px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease;
            border: 1px solid rgba(65, 105, 225, 0.1);
        }
        
        .option-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(65, 105, 225, 0.2);
        }
        
        .option-card i {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 25px;
            transition: color 0.3s ease;
        }
        
        .option-card:hover i {
            color: var(--secondary-color);
        }
        
        .option-card h3 {
            margin-bottom: 15px;
            color: var(--secondary-color);
        }
        
        /* Footer */
        footer {
            background-color: #0A0A0A;
            color: var(--text-color);
            padding: 80px 0 30px;
            position: relative;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 220px;
        }
        
        .footer-column h3 {
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 15px;
            color: var(--secondary-color);
        }
        
        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 50px;
            height: 2px;
            background-color: var(--primary-color);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 12px;
        }
        
        .footer-column ul li a {
            color: #aaa;
            transition: color 0.3s ease;
        }
        
        .footer-column ul li a:hover {
            color: var(--secondary-color);
        }
        
        .social-links {
            display: flex;
            gap: 20px;
            margin-top: 25px;
        }
        
        .social-links a {
            color: #aaa;
            font-size: 1.3rem;
            transition: color 0.3s ease, transform 0.3s ease;
        }
        
        .social-links a:hover {
            color: var(--secondary-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #777;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 80px;
                left: 0;
                width: 100%;
                background-color: rgba(10, 10, 10, 0.95);
                flex-direction: column;
                align-items: center;
                padding: 30px 0;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
                backdrop-filter: blur(10px);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hamburger {
                display: block;
                font-size: 1.5rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-content, .story {
                flex-direction: column;
            }
            
            .story:nth-child(even) {
                flex-direction: column;
            }
            
            .section-title {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .btn {
                padding: 10px 20px;
                font-size: 0.8rem;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <!-- Silk Background Canvas -->
    <canvas id="silk-bg"></canvas>
    
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Viksit <span>Bharat</span></div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#initiatives">Initiatives</a></li>
                    <li><a href="#stories">Success Stories</a></li>
                    <li><a href="#get-involved">Get Involved</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Digital Technology for All</h1>
                <p>Bridging the digital divide through innovative solutions to create a truly Viksit Bharat</p>
                <a href="#get-involved" class="btn">Join the Movement</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">About Viksit Bharat</h2>
            <div class="about-content">
                <div class="about-text">
                    <h3>Our Vision for a Digitally Inclusive India</h3>
                    <p>The Viksit Bharat initiative aims to harness digital technology to empower every citizen, regardless of their location or socioeconomic status. We believe that access to digital tools and knowledge is a fundamental right in today's world.</p>
                    <p>The digital divide in India manifests in multiple ways - lack of internet access in rural areas, affordability of devices, digital illiteracy, and language barriers. Our mission is to address these challenges through innovative solutions and collaborative efforts.</p>
                    <p>By 2047, we envision an India where every citizen can participate in the digital economy, access quality education and healthcare online, and leverage technology to improve their livelihoods.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789" alt="Digital India">
                </div>
            </div>
        </div>
    </section>

    <!-- Initiatives Section -->
    <section class="initiatives" id="initiatives">
        <div class="container">
            <h2 class="section-title">Our Key Initiatives</h2>
            <div class="initiatives-grid">
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1527689368864-3a821dbccc34" alt="Digital Literacy">
                    </div>
                    <div class="card-content">
                        <h3>Digital Literacy Programs</h3>
                        <p>We conduct training programs in rural and urban underserved communities to teach basic digital skills, internet safety, and how to access government services online.</p>
                        <a href="https://develop-india-viksitbharat.my.canva.site/" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71" alt="Affordable Devices">
                    </div>
                    <div class="card-content">
                        <h3>Affordable Device Access</h3>
                        <p>Our device donation and subsidy programs help bridge the hardware gap by providing refurbished smartphones and tablets to low-income families and students.</p>
                        <a href="https://viksitbharat.my.canva.site/copy-of-affordable-device-access" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1519125323398-675f0ddb6308" alt="G20 Impact">
                    </div>
                    <div class="card-content">
                        <h3>G20 Impact on India's Expansion</h3>
                        <p>India's prospects have grown thanks to G20 initiatives in infrastructure financing, and pandemic response plans are influenced by healthcare collaboration. Additionally, G20-driven changes in the global supply chain have a significant impact on India's export-oriented industries.</p>
                        <a href="https://develop-india-viksitbharat.my.canva.site/g20india" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1631815588090-d4bfec5b1ccb" alt="Medical Sector">
                    </div>
                    <div class="card-content">
                        <h3>India's Booming Medical Sector</h3>
                        <p>India's medical sector is driving growth through medical tourism, pharmaceutical exports, and digital healthcare innovations. With world-class hospitals and affordable treatments, India is becoming a global healthcare destination while creating millions of jobs.</p>
                        <a href="https://develop-india-viksitbharat.my.canva.site/india-medical-sector" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1605000797499-95a51c5269ae" alt="Agriculture Sector">
                    </div>
                    <div class="card-content">
                        <h3>Transforming Agriculture Sector</h3>
                        <p>India's agriculture sector is modernizing with digital tools, precision farming, and agri-tech startups. These innovations are increasing yields, reducing waste, and connecting farmers directly to markets, contributing significantly to India's economic growth and food security.</p>
                        <a href="https://develop-india-viksitbharat.my.canva.site/transforming-agriculture-sector" class="btn">Learn More</a>
                    </div>
                </div>
                <div class="initiative-card">
                    <div class="card-image">
                        <img src="https://images.unsplash.com/photo-1520250497591-112f2f40a3f4" alt="Tourism Sector">
                    </div>
                    <div class="card-content">
                        <h3>Thriving Tourism Sector</h3>
                        <p>India's diverse tourism sector, from heritage sites to eco-tourism, is creating employment and promoting cultural exchange. Digital platforms are making travel more accessible, while infrastructure improvements are attracting more international visitors each year.</p>
                        <a href="https://develop-india-viksitbharat.my.canva.site/thriving-tourism" class="btn">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
<section class="infrastructure-section">
    <div class="container">
        <h2 class="section-title">Infrastructure Development</h2>
        <div class="content-wrapper">
            <div class="image-container">
                <img src="https://images.unsplash.com/photo-1605152276897-4f618f831968" alt="Digital Infrastructure in Rural India">
            </div>
            <div class="text-content">
                <h3>Building the Digital Backbone of Rural India</h3>
                <p>Our infrastructure initiatives focus on creating the physical and digital foundations needed to support a connected Bharat:</p>
                <ul>
                    <li><strong>Broadband for All:</strong> Deploying fiber optic networks to 250,000 gram panchayats with last-mile wireless connectivity</li>
                    <li><strong>Digital Villages:</strong> Establishing 50,000 village-level digital centers with computers, printers and trained operators</li>
                    <li><strong>5G Rural Pilot:</strong> Testing agricultural and healthcare applications in 500 villages</li>
                    <li><strong>Solar-powered Towers:</strong> Installing 10,000 renewable energy-powered mobile towers in off-grid areas</li>
                </ul>
                <div class="stats">
                    <div class="stat-item">
                        <span class="stat-number">98%</span>
                        <span class="stat-label">Villages connected</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">25k+</span>
                        <span class="stat-label">Digital centers</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">4.2M</span>
                        <span class="stat-label">Daily users</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="green-energy-section">
    <div class="container">
        <h2 class="section-title">Green Energy & Sustainability</h2>
        <div class="content-wrapper reverse">
            <div class="image-container">
                <img src="https://images.unsplash.com/photo-1508514177221-188b1cf16e9d" alt="Solar Power in Rural India">
            </div>
            <div class="text-content">
                <h3>Powering Digital Growth with Renewable Energy</h3>
                <p>Our green initiatives ensure technology adoption doesn't come at an environmental cost:</p>
                <ul>
                    <li><strong>Solar Digital Hubs:</strong> 15,000 centers powered entirely by renewable energy</li>
                    <li><strong>E-Waste Management:</strong> Recycling program collecting 85% of obsolete tech</li>
                    <li><strong>Energy-efficient Devices:</strong> Distributing low-power tablets and routers</li>
                    <li><strong>Carbon-neutral Data:</strong> Partnering with cloud providers using renewable energy</li>
                </ul>
                <div class="impact-statement">
                    <i class="fas fa-leaf"></i>
                    <p>Our digital centers reduce CO2 emissions by 60% compared to traditional setups while serving 3 million rural users monthly.</p>
                </div>
                <a href="file:///C:/Users/gamin/OneDrive/Desktop/Yash/GreenPower.html" class="btn">Learn About Our Green Tech</a>
            </div>
        </div>
    </div>
</section>

<section class="military-section">
    <div class="container">
        <h2 class="section-title">Military Technology & National Security</h2>
        <div class="content-wrapper">
            <div class="image-container">
                <img src="https://images.unsplash.com/photo-1550751827-4bd374c3f58b" alt="Indian Military Technology">
            </div>
            <div class="text-content">
                <h3>Strengthening India Through Military Innovation</h3>
                <p>The Indian Armed Forces play a crucial role in national development and security, with recent technological advancements enhancing both defense capabilities and civilian applications:</p>
                <ul>
                    <li><strong>Border Security:</strong> Advanced surveillance systems along the Pakistan border have reduced infiltration by 72% since 2019</li>
                    <li><strong>Drone Technology:</strong> Indigenous UAV development has created 15,000 high-tech jobs while improving surveillance</li>
                    <li><strong>Cybersecurity:</strong> Military-grade encryption now protects critical digital infrastructure nationwide</li>
                    <li><strong>Disaster Response:</strong> Armed Forces have deployed tech-assisted relief in 37 major disasters since 2020</li>
                </ul>
                
                <div class="tech-highlights">
                    <div class="tech-item">
                        <h4><i class="fas fa-drone-alt"></i> Drone Swarm Technology</h4>
                        <p>India's recent demonstration of AI-controlled drone swarms marks a strategic advantage in border surveillance and precision strikes.</p>
                    </div>
                    <div class="tech-item">
                        <h4><i class="fas fa-satellite-dish"></i> Space Defense</h4>
                        <p>With successful ASAT tests and new military satellites, India ensures secure communications and early warning systems.</p>
                    </div>
                    <div class="tech-item">
                        <h4><i class="fas fa-shield-alt"></i> Recent Conflicts</h4>
                        <p>Technological superiority was demonstrated in the 2023 border skirmishes, with minimal casualties through precision drone strikes.</p>
                    </div>
                </div>
                
                <div class="stats">
                    <div class="stat-item">
                        <span class="stat-number">$72B</span>
                        <span class="stat-label">Defense budget (2024)</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">75%</span>
                        <span class="stat-label">Indigenous equipment</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-number">1.4M+</span>
                        <span class="stat-label">Active personnel</span>
                    </div>
                </div>
                
                <div class="impact-statement">
                    <i class="fas fa-microchip"></i>
                    <p>Military R&D has led to 137 civilian technology spin-offs in areas like GPS, weather forecasting, and medical imaging since 2015.</p>
                </div>
            </div>
        </div>
    </div>
</section>

    <!-- Stories Section -->
    <section class="stories" id="stories">
        <div class="container">
            <h2 class="section-title">Success Stories</h2>
            <div class="story">
                <div class="story-image">
                    <img src="https://images.unsplash.com/photo-1521791055366-0d553872125f" alt="Success Story">
                </div>
                <div class="story-text">
                    <h3>Digital Empowerment in Rural Rajasthan</h3>
                    <p>In the village of Nimaj, Rajasthan, our digital literacy program trained 200 women to use smartphones for accessing government schemes, online banking, and starting small businesses. Within six months, 85% of participants reported increased income and better access to services.</p>
                    <p>"I never thought I could learn to use a smartphone at my age. Now I can video call my children in the city and even sell my handicrafts online," says Kamla Devi, a 58-year-old participant.</p>
                    <a href="file:///C:/Users/gamin/AppData/Local/Microsoft/Windows/INetCache/IE/B3R2FZZT/competitionrural3[1].html" class="btn" target="_blank">Learn More</a>
                </div>
            </div>
            <div class="story">
                <div class="story-image">
                    <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644" alt="Success Story">
                </div>
                <div class="story-text">
                    <h3>Farmers Embrace AgriTech</h3>
                    <p>In Maharashtra, we partnered with local farmers to implement IoT-based soil sensors and weather forecasting apps. This technology helped farmers increase yields by 30% while reducing water usage by 25%.</p>
                    <p>"The digital tools tell me exactly when to water my crops and what fertilizers to use. It's like having an agricultural expert in my pocket," shares farmer Rajesh Patil.</p>
                    <a href="file:///C:/Users/gamin/OneDrive/Desktop/Yash/competitionrural5.html" class="btn" target="_blank">Read More Stories</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Get Involved Section -->
    <section class="get-involved" id="get-involved">
        <div class="container">
            <h2 class="section-title">Get Involved</h2>
            <p>Join us in bridging the digital divide and building a Viksit Bharat</p>
            <div class="involvement-options">
                <div class="option-card">
                    <i class="fas fa-hand-holding-usd"></i>
                    <h3>Donate</h3>
                    <p>Your financial contribution helps us provide devices, internet access, and training to underserved communities.</p>
                    <a href="file:///C:/Users/gamin/OneDrive/Desktop/Yash/competition4.html" class="btn" target="_blank">Donate Now</a>
                </div>
                <div class="option-card">
                    <i class="fas fa-hands-helping"></i>
                    <h3>Volunteer</h3>
                    <p>Share your digital skills by teaching in our community centers or mentoring online.</p>
                    <a href="https://chat.whatsapp.com/Gvsl9VfJbmfFmzDcrK15I9" class="btn" target="_blank">Volunteer Today</a>
                </div>
                <div class="option-card">
                    <i class="fas fa-handshake"></i>
                    <h3>Partner</h3>
                    <p>Are you a business or organization? Partner with us to scale our impact.</p>
                    <a href="file:///C:/Users/gamin/OneDrive/Desktop/Yash/Competition5.html" class="btn" target="_blank">Partner With Us</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Viksit Bharat</h3>
                    <p>Working towards a digitally inclusive India where technology empowers every citizen.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#initiatives">Initiatives</a></li>
                        <li><a href="#stories">Success Stories</a></li>
                        <li><a href="#get-involved">Get Involved</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul>
                        <li><i class="fas fa-map-marker-alt"></i> New Delhi, India</li>
                        <li><i class="fas fa-phone"></i> +91 98765 43210</li>
                        <li><i class="fas fa-envelope"></i> contact@viksitbharat.org</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Viksit Bharat Initiative. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Silk Background Animation
        const canvas = document.getElementById('silk-bg');
        const ctx = canvas.getContext('2d');
        
        // Configuration (matches ReactBits Silk parameters)
        const config = {
            speed: 5,        // matches speed={5}
            color: '#7B7481', // matches color="#7B7481"
            noise: 1.5,      // matches noiseIntensity={1.5}
            nodeCount: 60    // number of connection nodes
        };

        // Initialize canvas
        function init() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
            createNodes();
            animate();
        }

        // Create nodes for connections
        const nodes = [];
        function createNodes() {
            for (let i = 0; i < config.nodeCount; i++) {
                nodes.push({
                    x: Math.random() * canvas.width,
                    y: Math.random() * canvas.height,
                    vx: (Math.random() - 0.5) * config.speed,
                    vy: (Math.random() - 0.5) * config.speed
                });
            }
        }

        // Animation loop
        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Update node positions
            nodes.forEach(node => {
                node.x += node.vx;
                node.y += node.vy;
                
                // Bounce off edges
                if (node.x < 0 || node.x > canvas.width) node.vx *= -1;
                if (node.y < 0 || node.y > canvas.height) node.vy *= -1;
            });
            
            // Draw connections
            ctx.strokeStyle = config.color;
            ctx.lineWidth = 0.3;
            
            for (let i = 0; i < nodes.length; i++) {
                for (let j = i + 1; j < nodes.length; j++) {
                    const dx = nodes[i].x - nodes[j].x;
                    const dy = nodes[i].y - nodes[j].y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    
                    // Only draw lines for nearby nodes
                    if (distance < 200) {
                        const opacity = 1 - distance / 200;
                        ctx.globalAlpha = opacity * 0.7;
                        ctx.beginPath();
                        ctx.moveTo(nodes[i].x, nodes[i].y);
                        ctx.lineTo(nodes[j].x, nodes[j].y);
                        ctx.stroke();
                    }
                }
            }
            
            // Draw nodes
            ctx.fillStyle = config.color;
            ctx.globalAlpha = 0.8;
            nodes.forEach(node => {
                ctx.beginPath();
                ctx.arc(node.x, node.y, 1.5, 0, Math.PI * 2);
                ctx.fill();
            });
            
            requestAnimationFrame(animate);
        }

        // Handle resize
        window.addEventListener('resize', () => {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        });

        // Start the animation
        init();

        // Mobile Navigation
        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
