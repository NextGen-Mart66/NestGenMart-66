‎<!DOCTYPE html>
‎<html lang="en">
‎<head>
‎    <meta charset="UTF-8">
‎    <meta name="viewport" content="width=device-width, initial-scale=1.0">
‎    <meta name="description" content="Curated recommendations for modern living. Expert reviews on kitchen gadgets, home organization, fitness gear, smart home devices, and lifestyle essentials.">
‎    <title>The Curated Life | Expert Product Reviews & Recommendations</title>
‎    
‎    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">
‎    
‎    <style>
‎        :root {
‎            --primary: #0D7377;
‎            --primary-dark: #095457;
‎            --secondary: #FF6B6B;
‎            --accent: #FFB800;
‎            --bg: #FAF9F6;
‎            --text: #2D3436;
‎            --text-light: #636e72;
‎            --border: #dfe6e9;
‎            --shadow: 0 4px 20px rgba(0,0,0,0.08);
‎            --shadow-hover: 0 8px 30px rgba(0,0,0,0.12);
‎            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
‎        }
‎
‎        * { margin: 0; padding: 0; box-sizing: border-box; }
‎
‎        body {
‎            font-family: 'Inter', sans-serif;
‎            background: var(--bg);
‎            color: var(--text);
‎            line-height: 1.6;
‎        }
‎
‎        h1, h2, h3 { font-family: 'Playfair Display', serif; font-weight: 700; }
‎
‎        .navbar {
‎            position: sticky;
‎            top: 0;
‎            background: rgba(250, 249, 246, 0.95);
‎            backdrop-filter: blur(10px);
‎            border-bottom: 1px solid var(--border);
‎            z-index: 1000;
‎            padding: 1rem 0;
‎        }
‎
‎        .nav-container {
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            padding: 0 2rem;
‎            display: flex;
‎            justify-content: space-between;
‎            align-items: center;
‎        }
‎
‎        .logo {
‎            font-family: 'Playfair Display', serif;
‎            font-size: 1.8rem;
‎            font-weight: 700;
‎            color: var(--primary);
‎            text-decoration: none;
‎            display: flex;
‎            align-items: center;
‎            gap: 0.5rem;
‎        }
‎
‎        .logo-icon {
‎            width: 40px;
‎            height: 40px;
‎            background: var(--primary);
‎            border-radius: 50%;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            color: white;
‎            font-size: 1.2rem;
‎        }
‎
‎        .nav-links {
‎            display: flex;
‎            gap: 2.5rem;
‎            list-style: none;
‎        }
‎
‎        .nav-links a {
‎            text-decoration: none;
‎            color: var(--text);
‎            font-weight: 500;
‎            font-size: 0.95rem;
‎            transition: var(--transition);
‎            position: relative;
‎        }
‎
‎        .nav-links a::after {
‎            content: '';
‎            position: absolute;
‎            bottom: -5px;
‎            left: 0;
‎            width: 0;
‎            height: 2px;
‎            background: var(--secondary);
‎            transition: var(--transition);
‎        }
‎
‎        .nav-links a:hover::after { width: 100%; }
‎
‎        .nav-cta {
‎            background: var(--secondary);
‎            color: white !important;
‎            padding: 0.6rem 1.5rem;
‎            border-radius: 50px;
‎            font-weight: 600;
‎        }
‎
‎        .nav-cta:hover { background: #ff5252; transform: translateY(-2px); }
‎
‎        .hero {
‎            padding: 5rem 2rem;
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            display: grid;
‎            grid-template-columns: 1fr 1fr;
‎            gap: 4rem;
‎            align-items: center;
‎        }
‎
‎        .hero-content h1 {
‎            font-size: 3.5rem;
‎            line-height: 1.1;
‎            margin-bottom: 1.5rem;
‎        }
‎
‎        .hero-content .highlight {
‎            color: var(--primary);
‎            position: relative;
‎            display: inline-block;
‎        }
‎
‎        .hero-content .highlight::after {
‎            content: '';
‎            position: absolute;
‎            bottom: 5px;
‎            left: 0;
‎            width: 100%;
‎            height: 12px;
‎            background: rgba(255, 184, 0, 0.3);
‎            z-index: -1;
‎        }
‎
‎        .hero-subtitle {
‎            font-size: 1.25rem;
‎            color: var(--text-light);
‎            margin-bottom: 2rem;
‎        }
‎
‎        .hero-stats {
‎            display: flex;
‎            gap: 3rem;
‎            margin-bottom: 2.5rem;
‎        }
‎
‎        .stat { text-align: center; }
‎
‎        .stat-number {
‎            font-size: 2rem;
‎            font-weight: 700;
‎            color: var(--primary);
‎            display: block;
‎        }
‎
‎        .stat-label {
‎            font-size: 0.875rem;
‎            color: var(--text-light);
‎            text-transform: uppercase;
‎            letter-spacing: 0.5px;
‎        }
‎
‎        .hero-cta { display: flex; gap: 1rem; flex-wrap: wrap; }
‎
‎        .btn {
‎            padding: 1rem 2rem;
‎            border-radius: 50px;
‎            text-decoration: none;
‎            font-weight: 600;
‎            transition: var(--transition);
‎            display: inline-flex;
‎            align-items: center;
‎            gap: 0.5rem;
‎        }
‎
‎        .btn-primary {
‎            background: var(--primary);
‎            color: white;
‎            box-shadow: 0 4px 15px rgba(13, 115, 119, 0.3);
‎        }
‎
‎        .btn-primary:hover {
‎            background: var(--primary-dark);
‎            transform: translateY(-2px);
‎        }
‎
‎        .btn-secondary {
‎            background: white;
‎            color: var(--text);
‎            border: 2px solid var(--border);
‎        }
‎
‎        .btn-secondary:hover { border-color: var(--primary); color: var(--primary); }
‎
‎        .hero-visual { position: relative; }
‎
‎        .hero-image-grid {
‎            display: grid;
‎            grid-template-columns: repeat(2, 1fr);
‎            gap: 1rem;
‎            transform: rotate(-3deg);
‎        }
‎
‎        .hero-img {
‎            border-radius: 20px;
‎            overflow: hidden;
‎            box-shadow: var(--shadow);
‎            transition: var(--transition);
‎            aspect-ratio: 1;
‎            background: linear-gradient(135deg, #e0f7fa 0%, #b2ebf2 100%);
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            font-size: 3rem;
‎        }
‎
‎        .hero-img:hover { transform: translateY(-5px) rotate(2deg); }
‎
‎        .floating-badge {
‎            position: absolute;
‎            background: white;
‎            padding: 1rem 1.5rem;
‎            border-radius: 15px;
‎            box-shadow: var(--shadow);
‎            display: flex;
‎            align-items: center;
‎            gap: 0.75rem;
‎            animation: float 3s ease-in-out infinite;
‎        }
‎
‎        .badge-1 { top: 10%; right: -20px; }
‎        .badge-2 { bottom: 20%; left: -30px; animation-delay: 1.5s; }
‎
‎        @keyframes float {
‎            0%, 100% { transform: translateY(0); }
‎            50% { transform: translateY(-10px); }
‎        }
‎
‎        .lifestyles {
‎            padding: 5rem 2rem;
‎            background: white;
‎        }
‎
‎        .section-header {
‎            text-align: center;
‎            max-width: 600px;
‎            margin: 0 auto 3rem;
‎        }
‎
‎        .section-tag {
‎            display: inline-block;
‎            background: rgba(13, 115, 119, 0.1);
‎            color: var(--primary);
‎            padding: 0.5rem 1rem;
‎            border-radius: 50px;
‎            font-size: 0.875rem;
‎            font-weight: 600;
‎            text-transform: uppercase;
‎            letter-spacing: 1px;
‎            margin-bottom: 1rem;
‎        }
‎
‎        .section-title { font-size: 2.5rem; margin-bottom: 1rem; }
‎
‎        .section-subtitle { color: var(--text-light); font-size: 1.1rem; }
‎
‎        .lifestyle-grid {
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            display: grid;
‎            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
‎            gap: 1.5rem;
‎        }
‎
‎        .lifestyle-card {
‎            background: var(--bg);
‎            border-radius: 20px;
‎            padding: 2rem;
‎            text-align: center;
‎            transition: var(--transition);
‎            cursor: pointer;
‎            border: 2px solid transparent;
‎            position: relative;
‎            overflow: hidden;
‎        }
‎
‎        .lifestyle-card::before {
‎            content: '';
‎            position: absolute;
‎            top: 0;
‎            left: 0;
‎            width: 100%;
‎            height: 5px;
‎            background: var(--primary);
‎            transform: scaleX(0);
‎            transition: var(--transition);
‎        }
‎
‎        .lifestyle-card:hover { transform: translateY(-5px); border-color: var(--primary); }
‎        .lifestyle-card:hover::before { transform: scaleX(1); }
‎
‎        .lifestyle-icon {
‎            width: 70px;
‎            height: 70px;
‎            background: white;
‎            border-radius: 50%;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            margin: 0 auto 1rem;
‎            font-size: 2rem;
‎            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
‎        }
‎
‎        .lifestyle-name { font-family: 'Playfair Display', serif; font-size: 1.25rem; margin-bottom: 0.5rem; }
‎
‎        .lifestyle-count { color: var(--text-light); font-size: 0.9rem; }
‎
‎        .featured { padding: 5rem 2rem; max-width: 1200px; margin: 0 auto; }
‎
‎        .products-grid {
‎            display: grid;
‎            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
‎            gap: 2rem;
‎            margin-top: 3rem;
‎        }
‎
‎        .product-card {
‎            background: white;
‎            border-radius: 20px;
‎            overflow: hidden;
‎            box-shadow: var(--shadow);
‎            transition: var(--transition);
‎            position: relative;
‎        }
‎
‎        .product-card:hover { transform: translateY(-8px); box-shadow: var(--shadow-hover); }
‎
‎        .product-badge {
‎            position: absolute;
‎            top: 1rem;
‎            left: 1rem;
‎            background: var(--accent);
‎            color: var(--text);
‎            padding: 0.4rem 0.8rem;
‎            border-radius: 50px;
‎            font-size: 0.75rem;
‎            font-weight: 700;
‎            text-transform: uppercase;
‎            z-index: 10;
‎        }
‎
‎        .product-badge.bestseller { background: var(--secondary); color: white; }
‎
‎        .product-image {
‎            width: 100%;
‎            height: 220px;
‎            background: linear-gradient(135deg, #f5f5f5 0%, #e0e0e0 100%);
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            font-size: 4rem;
‎        }
‎
‎        .product-content { padding: 1.5rem; }
‎
‎        .product-category {
‎            color: var(--primary);
‎            font-size: 0.8rem;
‎            font-weight: 600;
‎            text-transform: uppercase;
‎            letter-spacing: 0.5px;
‎            margin-bottom: 0.5rem;
‎        }
‎
‎        .product-title { font-size: 1.1rem; margin-bottom: 0.5rem; line-height: 1.4; }
‎
‎        .product-rating { display: flex; align-items: center; gap: 0.5rem; margin-bottom: 1rem; }
‎
‎        .stars { color: var(--accent); font-size: 0.9rem; }
‎
‎        .rating-count { color: var(--text-light); font-size: 0.85rem; }
‎
‎        .product-footer {
‎            display: flex;
‎            justify-content: space-between;
‎            align-items: center;
‎            padding-top: 1rem;
‎            border-top: 1px solid var(--border);
‎        }
‎
‎        .product-price { font-size: 1.25rem; font-weight: 700; }
‎
‎        .product-price .original {
‎            font-size: 0.9rem;
‎            color: var(--text-light);
‎            text-decoration: line-through;
‎            margin-left: 0.5rem;
‎            font-weight: 400;
‎        }
‎
‎        .btn-small { padding: 0.6rem 1.2rem; font-size: 0.9rem; }
‎
‎        .trust {
‎            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
‎            color: white;
‎            padding: 4rem 2rem;
‎            margin: 4rem 0;
‎        }
‎
‎        .trust-container {
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            display: grid;
‎            grid-template-columns: 1fr 1fr;
‎            gap: 4rem;
‎            align-items: center;
‎        }
‎
‎        .trust-content h2 { font-size: 2.5rem; margin-bottom: 1.5rem; }
‎
‎        .trust-content p { font-size: 1.1rem; opacity: 0.9; margin-bottom: 2rem; }
‎
‎        .trust-features {
‎            display: grid;
‎            grid-template-columns: 1fr 1fr;
‎            gap: 1.5rem;
‎        }
‎
‎        .trust-feature { display: flex; align-items: flex-start; gap: 1rem; }
‎
‎        .trust-icon {
‎            width: 50px;
‎            height: 50px;
‎            background: rgba(255,255,255,0.2);
‎            border-radius: 12px;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            font-size: 1.5rem;
‎            flex-shrink: 0;
‎        }
‎
‎        .trust-feature h4 { font-size: 1rem; margin-bottom: 0.25rem; }
‎
‎        .trust-feature p { font-size: 0.9rem; opacity: 0.8; margin: 0; }
‎
‎        .trust-badge-large {
‎            background: white;
‎            color: var(--text);
‎            padding: 2rem;
‎            border-radius: 20px;
‎            text-align: center;
‎            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
‎        }
‎
‎        .trust-stamp {
‎            width: 100px;
‎            height: 100px;
‎            background: var(--secondary);
‎            border-radius: 50%;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            margin: 0 auto 1rem;
‎            font-size: 2.5rem;
‎            animation: pulse 2s infinite;
‎        }
‎
‎        @keyframes pulse {
‎            0%, 100% { transform: scale(1); }
‎            50% { transform: scale(1.05); }
‎        }
‎
‎        .trust-badge-large h3 { color: var(--primary); margin-bottom: 0.5rem; }
‎
‎        .trust-badge-large p { color: var(--text-light); font-size: 0.9rem; }
‎
‎        .reviews { padding: 5rem 2rem; background: white; }
‎
‎        .reviews-grid {
‎            max-width: 1200px;
‎            margin: 3rem auto 0;
‎            display: grid;
‎            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
‎            gap: 2rem;
‎        }
‎
‎        .review-card {
‎            display: grid;
‎            grid-template-columns: 120px 1fr;
‎            gap: 1.5rem;
‎            padding: 1.5rem;
‎            background: var(--bg);
‎            border-radius: 15px;
‎            transition: var(--transition);
‎            border: 2px solid transparent;
‎        }
‎
‎        .review-card:hover { border-color: var(--primary); transform: translateX(5px); }
‎
‎        .review-thumb {
‎            width: 120px;
‎            height: 120px;
‎            background: linear-gradient(135deg, #e0f7fa 0%, #b2ebf2 100%);
‎            border-radius: 10px;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            font-size: 2.5rem;
‎        }
‎
‎        .review-content h3 { font-size: 1.1rem; margin-bottom: 0.5rem; }
‎
‎        .review-meta {
‎            display: flex;
‎            gap: 1rem;
‎            margin-bottom: 0.75rem;
‎            font-size: 0.85rem;
‎            color: var(--text-light);
‎        }
‎
‎        .review-excerpt { font-size: 0.95rem; color: var(--text-light); margin-bottom: 1rem; }
‎
‎        .read-more {
‎            color: var(--primary);
‎            text-decoration: none;
‎            font-weight: 600;
‎            font-size: 0.9rem;
‎        }
‎
‎        .newsletter {
‎            padding: 5rem 2rem;
‎            max-width: 800px;
‎            margin: 0 auto;
‎            text-align: center;
‎        }
‎
‎        .newsletter-form {
‎            display: flex;
‎            gap: 1rem;
‎            margin-top: 2rem;
‎            justify-content: center;
‎            flex-wrap: wrap;
‎        }
‎
‎        .newsletter-input {
‎            flex: 1;
‎            min-width: 300px;
‎            padding: 1rem 1.5rem;
‎            border: 2px solid var(--border);
‎            border-radius: 50px;
‎            font-size: 1rem;
‎            font-family: inherit;
‎        }
‎
‎        .newsletter-input:focus { outline: none; border-color: var(--primary); }
‎
‎        .disclaimer { font-size: 0.8rem; color: var(--text-light); margin-top: 1rem; }
‎
‎        footer {
‎            background: var(--text);
‎            color: white;
‎            padding: 4rem 2rem 2rem;
‎        }
‎
‎        .footer-grid {
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            display: grid;
‎            grid-template-columns: 2fr repeat(3, 1fr);
‎            gap: 3rem;
‎            margin-bottom: 3rem;
‎        }
‎
‎        .footer-brand .logo { color: white; margin-bottom: 1rem; }
‎
‎        .footer-brand p { opacity: 0.8; line-height: 1.6; margin-bottom: 1.5rem; }
‎
‎        .social-links { display: flex; gap: 1rem; }
‎
‎        .social-links a {
‎            width: 40px;
‎            height: 40px;
‎            background: rgba(255,255,255,0.1);
‎            border-radius: 50%;
‎            display: flex;
‎            align-items: center;
‎            justify-content: center;
‎            text-decoration: none;
‎            color: white;
‎            transition: var(--transition);
‎        }
‎
‎        .social-links a:hover { background: var(--secondary); transform: translateY(-3px); }
‎
‎        .footer-column h4 { font-size: 1rem; margin-bottom: 1.5rem; color: white; }
‎
‎        .footer-column ul { list-style: none; }
‎
‎        .footer-column li { margin-bottom: 0.75rem; }
‎
‎        .footer-column a {
‎            color: rgba(255,255,255,0.7);
‎            text-decoration: none;
‎            transition: var(--transition);
‎            font-size: 0.95rem;
‎        }
‎
‎        .footer-column a:hover { color: var(--secondary); padding-left: 5px; }
‎
‎        .footer-bottom {
‎            max-width: 1200px;
‎            margin: 0 auto;
‎            padding-top: 2rem;
‎            border-top: 1px solid rgba(255,255,255,0.1);
‎            display: flex;
‎            justify-content: space-between;
‎            align-items: center;
‎            flex-wrap: wrap;
‎            gap: 1rem;
‎            font-size: 0.9rem;
‎            opacity: 0.7;
‎        }
‎
‎        .affiliate-disclosure {
‎            background: rgba(255,255,255,0.05);
‎            padding: 1rem;
‎            border-radius: 10px;
‎            font-size: 0.85rem;
‎            line-height: 1.5;
‎        }
‎
‎        .mobile-menu-btn {
‎            display: none;
‎            background: none;
‎            border: none;
‎            font-size: 1.5rem;
‎            cursor: pointer;
‎            color: var(--text);
‎        }
‎
‎        .sticky-cta {
‎            position: fixed;
‎            bottom: 0;
‎            left: 0;
‎            right: 0;
‎            background: white;
‎            padding: 1rem;
‎            box-shadow: 0 -4px 20px rgba(0,0,0,0.1);
‎            display: flex;
‎            justify-content: center;
‎            gap: 1rem;
‎            z-index: 999;
‎            transform: translateY(100%);
‎            transition: transform 0.3s ease;
‎        }
‎
‎        .sticky-cta.visible { transform: translateY(0); }
‎
‎        .sticky-cta-content {
‎            display: flex;
‎            align-items: center;
‎            
