# Business Plan Builder - Professional Website

I'll create a comprehensive, modern website for business planning that includes all essential sections with a clean, professional design.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Business Plan Builder | Create Your Winning Strategy</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Montserrat:wght@700;800&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #0f172a;
            --accent: #f97316;
            --light: #f8fafc;
            --gray: #64748b;
            --light-gray: #e2e8f0;
            --success: #10b981;
            --border-radius: 12px;
            --box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--secondary);
            background-color: #f1f5f9;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            line-height: 1.2;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        .btn {
            display: inline-block;
            padding: 12px 28px;
            background: var(--primary);
            color: white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 16px;
            box-shadow: var(--box-shadow);
        }

        .btn:hover {
            background: var(--primary-dark);
            transform: translateY(-3px);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            box-shadow: none;
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 36px;
            margin-bottom: 15px;
            color: var(--secondary);
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
            font-size: 18px;
        }

        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 28px;
            font-weight: 800;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
        }

        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .mobile-menu {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding: 180px 0 100px;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: -50px;
            right: -50px;
            width: 300px;
            height: 300px;
            border-radius: 50%;
            background: rgba(37, 99, 235, 0.1);
        }

        .hero-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .hero-text {
            flex: 1;
            max-width: 600px;
        }

        .hero-text h1 {
            font-size: 48px;
            margin-bottom: 20px;
            color: var(--secondary);
        }

        .hero-text p {
            font-size: 18px;
            color: var(--gray);
            margin-bottom: 30px;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: flex-end;
        }

        .hero-image img {
            max-width: 100%;
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
        }

        /* Features Section */
        .features {
            background-color: white;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .feature-card {
            background: white;
            border-radius: var(--border-radius);
            padding: 30px;
            text-align: center;
            box-shadow: var(--box-shadow);
            transition: var(--transition);
        }

        .feature-card:hover {
            transform: translateY(-10px);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: rgba(37, 99, 235, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: var(--primary);
            font-size: 28px;
        }

        .feature-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
        }

        /* Business Plan Sections */
        .plan-sections {
            background-color: #f8fafc;
        }

        .sections-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }

        .section-card {
            background: white;
            border-radius: var(--border-radius);
            padding: 25px;
            box-shadow: var(--box-shadow);
            transition: var(--transition);
            border-top: 4px solid var(--primary);
        }

        .section-card:hover {
            transform: translateY(-5px);
        }

        .section-card h3 {
            font-size: 20px;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }

        .section-card h3 i {
            margin-right: 10px;
            color: var(--primary);
        }

        /* Testimonials */
        .testimonials {
            background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
            color: white;
        }

        .testimonials .section-title h2,
        .testimonials .section-title p {
            color: white;
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .testimonial-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: var(--border-radius);
            padding: 30px;
            position: relative;
        }

        .testimonial-card::before {
            content: """;
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 80px;
            font-family: Georgia, serif;
            color: rgba(255, 255, 255, 0.2);
            line-height: 1;
        }

        .testimonial-content {
            margin-bottom: 20px;
            font-style: italic;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--accent);
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            font-weight: bold;
            color: white;
        }

        .author-info h4 {
            font-size: 18px;
            margin-bottom: 5px;
        }

        .author-info p {
            font-size: 14px;
            opacity: 0.8;
        }

        /* CTA Section */
        .cta {
            text-align: center;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            padding: 100px 0;
        }

        .cta h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }

        .cta p {
            font-size: 18px;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 40px;
        }

        /* Footer */
        footer {
            background: var(--secondary);
            color: white;
            padding: 60px 0 30px;
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-col h3 {
            font-size: 22px;
            margin-bottom: 25px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--accent);
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #cbd5e1;
            text-decoration: none;
            transition: var(--transition);
        }

        .footer-links a:hover {
            color: white;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #94a3b8;
            font-size: 14px;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-text {
                margin-bottom: 50px;
            }
            
            .hero-text p {
                margin-left: auto;
                margin-right: auto;
            }
            
            .nav-links {
                display: none;
            }
            
            .mobile-menu {
                display: block;
            }
        }

        @media (max-width: 768px) {
            .hero-text h1 {
                font-size: 36px;
            }
            
            section {
                padding: 60px 0;
            }
            
            .section-title h2 {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">
                    <i class="fas fa-chart-line"></i>
                    PlanPro
                </a>
                <ul class="nav-links">
                    <li><a href="#features">Features</a></li>
                    <li><a href="#sections">Plan Sections</a></li>
                    <li><a href="#testimonials">Testimonials</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="mobile-menu">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Create a Winning Business Plan in Minutes</h1>
                    <p>Our proven framework helps entrepreneurs and startups develop comprehensive, investor-ready business plans that drive growth and secure funding.</p>
                    <div class="hero-buttons">
                        <a href="#sections" class="btn">Get Started</a>
                        <a href="#features" class="btn btn-outline">Learn More</a>
                    </div>
                </div>
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80" alt="Business Plan">
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Our Business Plan Builder?</h2>
                <p>Our platform provides everything you need to create a professional business plan that stands out</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-rocket"></i>
                    </div>
                    <h3>Investor-Ready Templates</h3>
                    <p>Access professionally designed templates that meet investor expectations and industry standards.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-chart-pie"></i>
                    </div>
                    <h3>Financial Forecasting</h3>
                    <p>Build detailed financial projections with our intuitive tools and automated calculations.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-users"></i>
                    </div>
                    <h3>Market Analysis</h3>
                    <p>Conduct thorough market research with our integrated tools and industry benchmarks.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-sync-alt"></i>
                    </div>
                    <h3>Real-Time Collaboration</h3>
                    <p>Work with your team simultaneously on the same plan with cloud-based collaboration.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-file-export"></i>
                    </div>
                    <h3>Export Options</h3>
                    <p>Download your plan as PDF, Word, or PowerPoint with one click for presentations.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-headset"></i>
                    </div>
                    <h3>Expert Support</h3>
                    <p>Get help from business planning experts whenever you need guidance or feedback.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Business Plan Sections -->
    <section class="plan-sections" id="sections">
        <div class="container">
            <div class="section-title">
                <h2>Essential Business Plan Components</h2>
                <p>Every successful business plan includes these critical sections</p>
            </div>
            <div class="sections-grid">
                <div class="section-card">
                    <h3><i class="fas fa-briefcase"></i> Executive Summary</h3>
                    <p>A concise overview of your business, mission, and key objectives that captures investor interest.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-industry"></i> Company Description</h3>
                    <p>Detailed information about your business, including history, structure, and vision.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-bullseye"></i> Market Analysis</h3>
                    <p>Research on your industry, target market, competitors, and market opportunities.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-lightbulb"></i> Products & Services</h3>
                    <p>Description of what you offer, your value proposition, and intellectual property.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-chart-line"></i> Marketing Strategy</h3>
                    <p>Your approach to reaching customers, pricing strategy, and sales channels.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-users"></i> Management Team</h3>
                    <p>Profiles of key team members, their experience, and organizational structure.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-calculator"></i> Financial Plan</h3>
                    <p>Projected income statements, cash flow, balance sheets, and funding requirements.</p>
                </div>
                <div class="section-card">
                    <h3><i class="fas fa-road"></i> Implementation Timeline</h3>
                    <p>Key milestones, deadlines, and operational plans for executing your strategy.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials -->
    <section class="testimonials" id="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Success Stories</h2>
                <p>See how entrepreneurs have transformed their ideas into thriving businesses</p>
            </div>
            <div class="testimonial-grid">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "PlanPro helped me secure $500K in seed funding. The financial forecasting tools were incredibly accurate and impressed our investors."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">SJ</div>
                        <div class="author-info">
                            <h4>Sarah Johnson</h4>
                            <p>Founder, TechStart Inc.</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "As a first-time entrepreneur, I was overwhelmed by the business planning process. This platform made it simple and guided me step-by-step."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">MR</div>
                        <div class="author-info">
                            <h4>Michael Rodriguez</h4>
                            <p>CEO, GreenSolutions</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        "The market analysis section helped us identify a gap in the market we hadn't considered. We pivoted our strategy and doubled our projected revenue."
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">TP</div>
                        <div class="author-info">
                            <h4>Tanya Patel</h4>
                            <p>Co-Founder, HealthTech Innovations</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="contact">
        <div class="container">
            <h2>Ready to Build Your Business Plan?</h2>
            <p>Join thousands of entrepreneurs who have used our platform to turn their ideas into reality</p>
            <a href="#" class="btn">Start Your Free Trial</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h3>PlanPro</h3>
                    <p>Creating winning business plans since 2015. Our mission is to empower entrepreneurs with the tools they need to succeed.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>Resources</h3>
                    <ul class="footer-links">
                        <li><a href="#">Business Plan Templates</a></li>
                        <li><a href="#">Financial Calculators</a></li>
                        <li><a href="#">Industry Reports</a></li>
                        <li><a href="#">Startup Guides</a></li>
                        <li><a href="#">Blog</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Company</h3>
                    <ul class="footer-links">
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Our Team</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Partners</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h3>Support</h3>
                    <ul class="footer-links">
                        <li><a href="#">Help Center</a></li>
                        <li><a href="#">FAQs</a></li>
                        <li><a href="#">Community Forum</a></li>
                        <li><a href="#">Webinars</a></li>
                        <li><a href="#">Contact Support</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 PlanPro. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple mobile menu toggle
        document.querySelector('.mobile-menu').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>


