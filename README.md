# datafox
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Universal Video Downloader | DATAFOX</title>
    <meta name="description" content="Download videos from multiple platforms with local processing for maximum privacy and performance">
    <meta name="keywords" content="video downloader, youtube downloader, facebook downloader, instagram downloader, tiktok downloader, universal downloader">
    <meta name="author" content="BLACKI">
    <meta name="theme-color" content="#2563eb">
    
    <!-- Open Graph / Social Media Meta Tags -->
    <meta property="og:title" content="DataFox - Universal Video Downloader">
    <meta property="og:description" content="Download videos from multiple platforms with local processing for maximum privacy and performance">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://datafox.app">
    <meta property="og:image" content="https://datafox.app/images/og-image.jpg">
    <meta property="og:site_name" content="DataFox">
    
    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="DataFox - Universal Video Downloader">
    <meta name="twitter:description" content="Download videos from multiple platforms with local processing for maximum privacy and performance">
    <meta name="twitter:image" content="https://datafox.app/images/twitter-card.jpg">
    
    <!-- Favicon Links -->
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    <link rel="manifest" href="/site.webmanifest">
    <link rel="mask-icon" href="/safari-pinned-tab.svg" color="#2563eb">
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- Global Styles -->
    <style>
        :root {
            --primary: #2563eb;
            --primary-hover: #1d4ed8;
            --primary-active: #1e40af;
            --background: #ffffff;
            --surface: #f8fafc;
            --surface-elevated: #ffffff;
            --border: #e2e8f0;
            --text: #1e293b;
            --text-secondary: #64748b;
            --text-tertiary: #94a3b8;
            --error: #dc2626;
            --success: #16a34a;
            --warning: #eab308;
            --radius-sm: 4px;
            --radius-md: 8px;
            --radius-lg: 12px;
            --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
            --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            --transition-fast: 0.15s cubic-bezier(0.4, 0, 0.2, 1);
            --transition-medium: 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            --space-xs: 4px;
            --space-sm: 8px;
            --space-md: 16px;
            --space-lg: 24px;
            --space-xl: 32px;
            --space-2xl: 48px;
            --space-3xl: 64px;
        }

        @media (prefers-color-scheme: dark) {
            :root {
                --primary: #3b82f6;
                --primary-hover: #2563eb;
                --primary-active: #1e40af;
                --background: #0f172a;
                --surface: #1e293b;
                --surface-elevated: #334155;
                --border: #334155;
                --text: #f8fafc;
                --text-secondary: #94a3b8;
                --text-tertiary: #64748b;
            }
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
            -webkit-text-size-adjust: 100%;
        }

        body {
            font-family: 'Inter', system-ui, -apple-system, sans-serif;
            line-height: 1.5;
            background-color: var(--background);
            color: var(--text);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            text-rendering: optimizeLegibility;
        }

        /* Header Styles */
        header {
            background-color: var(--surface);
            border-bottom: 1px solid var(--border);
            padding: var(--space-md) 0;
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(8px);
            background-color: rgba(248, 250, 252, 0.8);
        }

        @media (prefers-color-scheme: dark) {
            header {
                background-color: rgba(30, 41, 59, 0.8);
            }
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: var(--space-md);
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--space-md);
        }

        .logo {
            font-weight: 700;
            font-size: 1.25rem;
            display: flex;
            align-items: center;
            gap: var(--space-sm);
            color: var(--primary);
            text-decoration: none;
        }

        .logo-icon {
            width: 24px;
            height: 24px;
            flex-shrink: 0;
        }

        .logo-fox {
            color: var(--text);
        }

        /* Navigation Styles */
        .nav {
            display: flex;
            gap: var(--space-sm);
        }

        .nav-link {
            color: var(--text-secondary);
            text-decoration: none;
            font-weight: 500;
            transition: color var(--transition-fast);
            padding: var(--space-xs) var(--space-sm);
            border-radius: var(--radius-sm);
            font-size: 0.9375rem;
        }

        .nav-link:hover {
            color: var(--primary);
        }

        .nav-link.active {
            color: var(--primary);
            background-color: rgba(59, 130, 246, 0.1);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: var(--text);
            cursor: pointer;
            padding: var(--space-xs);
        }

        /* Main Content Styles */
        .main {
            flex: 1;
            padding: var(--space-2xl) 0;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--space-md);
            width: 100%;
        }

        .hero {
            text-align: center;
            margin-bottom: var(--space-2xl);
            padding: 0 var(--space-md);
        }

        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: var(--space-md);
            font-weight: 700;
            background: linear-gradient(to right, #2563eb, #3b82f6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1.2;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
        }

        .hero p {
            font-size: 1.125rem;
            color: var(--text-secondary);
            max-width: 700px;
            margin: 0 auto var(--space-md);
        }

        /* Download Card Styles */
        .download-card {
            background-color: var(--surface-elevated);
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            padding: var(--space-xl);
            max-width: 800px;
            margin: 0 auto;
            box-shadow: var(--shadow-sm);
            transition: box-shadow var(--transition-medium);
        }

        .download-card:hover {
            box-shadow: var(--shadow-md);
        }

        .input-group {
            margin-bottom: var(--space-lg);
        }

        .input-label {
            display: block;
            margin-bottom: var(--space-sm);
            font-weight: 500;
            color: var(--text);
            font-size: 0.9375rem;
        }

        .input-field {
            width: 100%;
            padding: var(--space-md);
            border: 1px solid var(--border);
            border-radius: var(--radius-md);
            font-size: 1rem;
            font-family: 'Inter', sans-serif;
            background-color: var(--background);
            color: var(--text);
            transition: border-color var(--transition-fast), box-shadow var(--transition-fast);
        }

        .input-field:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.2);
        }

        .select-field {
            width: 100%;
            padding: var(--space-md);
            border: 1px solid var(--border);
            border-radius: var(--radius-md);
            font-size: 1rem;
            font-family: 'Inter', sans-serif;
            background-color: var(--background);
            color: var(--text);
            appearance: none;
            background-image: url("data:image/svg+xml;charset=UTF-8,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='currentColor' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3e%3cpolyline points='6 9 12 15 18 9'%3e%3c/polyline%3e%3c/svg%3e");
            background-repeat: no-repeat;
            background-position: right var(--space-md) center;
            background-size: 16px;
            cursor: pointer;
        }

        /* Button Styles */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: var(--space-md) var(--space-lg);
            border-radius: var(--radius-md);
            font-size: 1rem;
            font-weight: 500;
            font-family: 'Inter', sans-serif;
            cursor: pointer;
            transition: var(--transition-fast);
            border: none;
            background-color: var(--primary);
            color: white;
            width: 100%;
            position: relative;
            overflow: hidden;
        }

        .btn:hover {
            background-color: var(--primary-hover);
        }

        .btn:active {
            background-color: var(--primary-active);
        }

        .btn:disabled {
            opacity: 0.7;
            cursor: not-allowed;
        }

        .btn-icon {
            margin-right: var(--space-sm);
            width: 18px;
            height: 18px;
            flex-shrink: 0;
        }

        .btn-loading .btn-icon {
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .btn-ripple {
            position: absolute;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.7);
            transform: scale(0);
            animation: ripple 600ms linear;
            pointer-events: none;
        }

        @keyframes ripple {
            to {
                transform: scale(4);
                opacity: 0;
            }
        }

        /* Features Section */
        .features {
            margin-top: var(--space-3xl);
        }

        .section-header {
            text-align: center;
            margin-bottom: var(--space-xl);
        }

        .section-header h2 {
            font-size: 1.75rem;
            margin-bottom: var(--space-sm);
        }

        .section-header p {
            color: var(--text-secondary);
            max-width: 600px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: var(--space-lg);
            margin-top: var(--space-lg);
        }

        .feature-card {
            background-color: var(--surface-elevated);
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            padding: var(--space-lg);
            transition: transform var(--transition-medium), box-shadow var(--transition-medium);
        }

        .feature-card:hover {
            transform: translateY(-4px);
            box-shadow: var(--shadow-md);
        }

        .feature-icon {
            width: 40px;
            height: 40px;
            margin-bottom: var(--space-md);
            color: var(--primary);
        }

        .feature-title {
            font-size: 1.125rem;
            font-weight: 600;
            margin-bottom: var(--space-sm);
        }

        .feature-desc {
            color: var(--text-secondary);
            font-size: 0.9375rem;
            line-height: 1.6;
        }

        /* Platforms Section */
        .platforms {
            margin-top: var(--space-3xl);
        }

        .platforms-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: var(--space-md);
            margin-top: var(--space-lg);
        }

        .platform {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: var(--space-md);
            background-color: var(--surface-elevated);
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            transition: transform var(--transition-fast), box-shadow var(--transition-fast);
            text-decoration: none;
            color: var(--text);
        }

        .platform:hover {
            transform: translateY(-2px);
            box-shadow: var(--shadow-sm);
        }

        .platform-icon {
            width: 32px;
            height: 32px;
            margin-bottom: var(--space-sm);
            flex-shrink: 0;
        }

        .platform-name {
            font-size: 0.875rem;
            font-weight: 500;
            text-align: center;
        }

        /* Processing Queue Styles */
        .processing-queue {
            position: fixed;
            top: var(--space-md);
            right: var(--space-md);
            background-color: var(--surface-elevated);
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            box-shadow: var(--shadow-lg);
            width: 360px;
            max-height: 80vh;
            overflow-y: auto;
            z-index: 1000;
            transform: translateX(calc(100% + var(--space-md)));
            transition: transform var(--transition-medium);
            opacity: 0.95;
            backdrop-filter: blur(8px);
        }

        .processing-queue.visible {
            transform: translateX(0);
        }

        .queue-header {
            padding: var(--space-md);
            border-bottom: 1px solid var(--border);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            background-color: var(--surface-elevated);
            z-index: 1;
        }

        .queue-title {
            font-weight: 600;
            font-size: 0.9375rem;
        }

        .queue-actions {
            display: flex;
            gap: var(--space-xs);
        }

        .queue-btn {
            background: none;
            border: none;
            color: var(--text-secondary);
            cursor: pointer;
            padding: var(--space-xs);
            border-radius: var(--radius-sm);
            transition: color var(--transition-fast), background-color var(--transition-fast);
        }

        .queue-btn:hover {
            color: var(--text);
            background-color: var(--border);
        }

        .queue-btn svg {
            width: 16px;
            height: 16px;
        }

        .queue-items {
            padding: var(--space-xs) 0;
        }

        .queue-item {
            padding: var(--space-md);
            display: flex;
            align-items: center;
            gap: var(--space-md);
            border-bottom: 1px solid var(--border);
            transition: background-color var(--transition-fast);
        }

        .queue-item:last-child {
            border-bottom: none;
        }

        .queue-item:hover {
            background-color: var(--surface);
        }

        .queue-item-icon {
            width: 20px;
            height: 20px;
            color: var(--primary);
            flex-shrink: 0;
        }

        .queue-item-details {
            flex: 1;
            min-width: 0;
        }

        .queue-item-name {
            font-size: 0.875rem;
            font-weight: 500;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }

        .queue-item-status {
            font-size: 0.75rem;
            color: var(--text-secondary);
            margin-top: 2px;
            display: flex;
            justify-content: space-between;
        }

        .queue-item-progress {
            height: 4px;
            background-color: var(--border);
            border-radius: 2px;
            margin-top: var(--space-sm);
            overflow: hidden;
        }

        .queue-item-progress-bar {
            height: 100%;
            background-color: var(--primary);
            width: 0%;
            transition: width 0.6s ease;
        }

        .queue-item-actions {
            display: flex;
            gap: var(--space-xs);
            margin-left: var(--space-sm);
        }

        .queue-item-btn {
            background: none;
            border: none;
            color: var(--text-secondary);
            cursor: pointer;
            padding: var(--space-xs);
            border-radius: var(--radius-sm);
            transition: color var(--transition-fast), background-color var(--transition-fast);
        }

        .queue-item-btn:hover {
            color: var(--text);
            background-color: var(--border);
        }

        .queue-item-btn svg {
            width: 16px;
            height: 16px;
        }

        .queue-badge {
            position: fixed;
            top: var(--space-md);
            right: var(--space-md);
            background-color: var(--primary);
            color: white;
            width: 24px;
            height: 24px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.75rem;
            font-weight: 600;
            cursor: pointer;
            z-index: 1001;
            box-shadow: var(--shadow-md);
            transition: transform var(--transition-fast);
            user-select: none;
        }

        .queue-badge:hover {
            transform: scale(1.1);
        }

        .queue-badge.hidden {
            display: none;
        }

        /* Disclaimer Styles */
        .disclaimer {
            margin-top: var(--space-2xl);
            padding: var(--space-md);
            background-color: rgba(234, 179, 8, 0.1);
            border-left: 4px solid var(--warning);
            border-radius: 0 var(--radius-md) var(--radius-md) 0;
            font-size: 0.875rem;
            line-height: 1.6;
        }

        .disclaimer strong {
            color: var(--warning);
        }

        /* Footer Styles */
        footer {
            background-color: var(--surface);
            border-top: 1px solid var(--border);
            padding: var(--space-xl) 0;
            margin-top: var(--space-3xl);
        }

        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 var(--space-md);
        }

        .footer-links {
            display: flex;
            gap: var(--space-md);
            margin-bottom: var(--space-md);
            flex-wrap: wrap;
            justify-content: center;
        }

        .footer-link {
            color: var(--text-secondary);
            text-decoration: none;
            font-size: 0.875rem;
            transition: color var(--transition-fast);
        }

        .footer-link:hover {
            color: var(--primary);
        }

        .footer-copyright {
            color: var(--text-secondary);
            font-size: 0.8125rem;
            max-width: 800px;
        }

        /* Toast notifications */
        .toast-container {
            position: fixed;
            bottom: var(--space-md);
            left: 50%;
            transform: translateX(-50%);
            z-index: 1000;
            display: flex;
            flex-direction: column;
            gap: var(--space-sm);
            width: 100%;
            max-width: 400px;
            padding: 0 var(--space-md);
        }

        .toast {
            background-color: var(--surface-elevated);
            border-radius: var(--radius-md);
            border: 1px solid var(--border);
            padding: var(--space-md);
            box-shadow: var(--shadow-lg);
            display: flex;
            align-items: center;
            gap: var(--space-md);
            animation: slideIn 0.3s ease forwards;
            opacity: 0;
        }

        @keyframes slideIn {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .toast-icon {
            width: 20px;
            height: 20px;
            flex-shrink: 0;
        }

        .toast.success .toast-icon {
            color: var(--success);
        }

        .toast.error .toast-icon {
            color: var(--error);
        }

        .toast.warning .toast-icon {
            color: var(--warning);
        }

        .toast-message {
            flex: 1;
            font-size: 0.875rem;
        }

        .toast-close {
            background: none;
            border: none;
            color: var(--text-secondary);
            cursor: pointer;
            padding: var(--space-xs);
            border-radius: var(--radius-sm);
        }

        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .fade-in {
            animation: fadeIn 0.3s ease forwards;
        }

        .fade-out {
            animation: fadeIn 0.3s ease reverse forwards;
        }

        .pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            .nav {
                position: fixed;
                top: 72px;
                left: 0;
                right: 0;
                background-color: var(--surface-elevated);
                border-bottom: 1px solid var(--border);
                padding: var(--space-md);
                flex-direction: column;
                gap: var(--space-sm);
                transform: translateY(-100%);
                opacity: 0;
                transition: transform var(--transition-medium), opacity var(--transition-medium);
                pointer-events: none;
            }
            
            .nav.visible {
                transform: translateY(0);
                opacity: 1;
                pointer-events: all;
            }
            
            .download-card {
                padding: var(--space-lg);
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .processing-queue {
                width: calc(100% - var(--space-md) * 2);
                max-height: 60vh;
            }
        }

        /* Mobile-specific styles */
        @media (max-width: 480px) {
            .download-card {
                padding: var(--space-md);
            }
            
            .btn {
                padding: var(--space-md);
                font-size: 0.9375rem;
            }
            
            /* Ensure download links are tappable on mobile */
            a[download] {
                min-width: 44px;
                min-height: 44px;
            }
            
            /* Mobile queue adjustments */
            .processing-queue {
                width: 100%;
                max-height: 70vh;
                bottom: 0;
                top: auto;
                right: 0;
                border-radius: var(--radius-md) var(--radius-md) 0 0;
            }
            
            .queue-badge {
                bottom: var(--space-md);
                top: auto;
            }
        }

        /* Accessibility focus styles */
        button:focus-visible, input:focus-visible, select:focus-visible, a:focus-visible {
            outline: 2px solid var(--primary);
            outline-offset: 2px;
        }

        /* Print Styles */
        @media print {
            header, footer, .processing-queue, .toast-container {
                display: none !important;
            }
            
            body {
                background-color: white !important;
                color: black !important;
            }
            
            .download-card {
                box-shadow: none !important;
                border: none !important;
                padding: 0 !important;
            }
        }
    </style>
</head>
<body>
    <!-- Header with DataFox branding -->
    <header>
        <div class="header-content">
            <a href="#" class="logo">
                <svg class="logo-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M3 3l7.07 16.97 2.51-7.39 7.39-2.51L3 3z"></path>
                    <path d="M13 13l6 6"></path>
                </svg>
                <span>DATA<span class="logo-fox">FOX</span></span>
            </a>
            <button class="mobile-menu-btn" aria-label="Toggle menu">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <line x1="3" y1="12" x2="21" y2="12"></line>
                    <line x1="3" y1="6" x2="21" y2="6"></line>
                    <line x1="3" y1="18" x2="21" y2="18"></line>
                </svg>
            </button>
            <nav class="nav">
                <a href="#features" class="nav-link">Features</a>
                <a href="#platforms" class="nav-link">Platforms</a>
                <a href="#privacy" class="nav-link">Privacy</a>
                <a href="#about" class="nav-link">About</a>
            </nav>
        </div>
    </header>

    <main class="main">
        <div class="container">
            <section class="hero">
                <h1>Universal Video Downloader</h1>
                <p>Download videos from multiple platforms with DataFox's local processing for maximum privacy and performance.</p>
            </section>

            <section class="download-card fade-in">
                <div class="input-group">
                    <label for="video-url" class="input-label">Video URL</label>
                    <input type="url" id="video-url" class="input-field" placeholder="Paste video link here..." autocomplete="off" required>
                </div>

                <div class="input-group">
                    <label for="platform" class="input-label">Select Platform (optional)</label>
                    <select id="platform" class="select-field">
                        <option value="auto">Auto Detect</option>
                        <option value="youtube">YouTube</option>
                        <option value="facebook">Facebook</option>
                        <option value="instagram">Instagram</option>
                        <option value="twitter">Twitter</option>
                        <option value="tiktok">TikTok</option>
                        <option value="bilibili">Bilibili</option>
                        <option value="vk">VK</option>
                        <option value="reddit">Reddit</option>
                        <option value="tumblr">Tumblr</option>
                        <option value="vimeo">Vimeo</option>
                        <option value="twitch">Twitch</option>
                        <option value="soundcloud">SoundCloud</option>
                        <option value="pinterest">Pinterest</option>
                        <option value="dailymotion">Dailymotion</option>
                        <option value="snapchat">Snapchat</option>
                        <option value="rutube">Rutube</option>
                        <option value="xiaohongshu">Xiaohongshu</option>
                        <option value="streamable">Streamable</option>
                        <option value="loom">Loom</option>
                    </select>
                </div>

                <button id="download-btn" class="btn">
                    <svg class="btn-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                        <polyline points="7 10 12 15 17 10"></polyline>
                        <line x1="12" y1="15" x2="12" y2="3"></line>
                    </svg>
                    Download Video
                </button>
            </section>

            <section id="features" class="features">
                <div class="section-header">
                    <h2>DataFox Features</h2>
                    <p>Experience the power of local processing with these advanced features</p>
                </div>
                <div class="features-grid">
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M12 12m-9 0a9 9 0 1 0 18 0a9 9 0 1 0 -18 0"></path>
                            <path d="M12 3a9 9 0 0 1 0 18"></path>
                            <path d="M12 12l6.3 6.3"></path>
                            <path d="M12 12l-6.3 6.3"></path>
                        </svg>
                        <h3 class="feature-title">On-Device Processing</h3>
                        <p class="feature-desc">DataFox processes all media locally in your browser - your data never leaves your device, ensuring maximum privacy.</p>
                    </div>
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M4 5a1 1 0 0 1 1 -1h14a1 1 0 0 1 1 1v14a1 1 0 0 1 -1 1h-14a1 1 0 0 1 -1 -1v-14z"></path>
                            <path d="M7 10v4"></path>
                            <path d="M11 10v4"></path>
                            <path d="M15 10v4"></path>
                        </svg>
                        <h3 class="feature-title">Multi-Platform Support</h3>
                        <p class="feature-desc">Download from 20+ platforms including YouTube, Instagram, TikTok, and more with a single interface.</p>
                    </div>
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M9 12l2 2l4 -4"></path>
                            <path d="M12 3a12 12 0 0 0 8.5 3a12 12 0 0 1 -8.5 15a12 12 0 0 1 -8.5 -15a12 12 0 0 0 8.5 -3"></path>
                        </svg>
                        <h3 class="feature-title">Smart Format Detection</h3>
                        <p class="feature-desc">Automatically detects the best available quality and format for each platform.</p>
                    </div>
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M12 3a12 12 0 0 0 8.5 3a12 12 0 0 1 -8.5 15a12 12 0 0 1 -8.5 -15a12 12 0 0 0 8.5 -3"></path>
                            <path d="M12 11m-1 0a1 1 0 1 0 2 0a1 1 0 1 0 -2 0"></path>
                            <path d="M12 12l0 .01"></path>
                        </svg>
                        <h3 class="feature-title">Privacy Focused</h3>
                        <p class="feature-desc">No tracking, no analytics, no server-side processing. Your downloads stay private.</p>
                    </div>
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M13 3v4h-4v-4h4z"></path>
                            <path d="M8 21v-8h8v8h-8z"></path>
                            <path d="M3 17v-4h4v4h-4z"></path>
                            <path d="M3 11v-4h4v4h-4z"></path>
                            <path d="M17 21v-8h4v8h-4z"></path>
                            <path d="M17 13v-4h4v4h-4z"></path>
                        </svg>
                        <h3 class="feature-title">Batch Processing</h3>
                        <p class="feature-desc">Queue multiple downloads and let DataFox process them automatically.</p>
                    </div>
                    <div class="feature-card">
                        <svg class="feature-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M9 19c-4.3 1.4 -4.3 2.8 -4.3 4.2c0 1.4 2.9 3.8 4.3 4.2"></path>
                            <path d="M15 19c4.3 1.4 4.3 2.8 4.3 4.2c0 1.4 -2.9 3.8 -4.3 4.2"></path>
                            <path d="M9 15c-4.3 -1.4 -4.3 -2.8 -4.3 -4.2c0 -1.4 2.9 -3.8 4.3 -4.2"></path>
                            <path d="M15 15c4.3 -1.4 4.3 -2.8 4.3 -4.2c0 -1.4 -2.9 -3.8 -4.3 -4.2"></path>
                        </svg>
                        <h3 class="feature-title">Advanced Formatting</h3>
                        <p class="feature-desc">Choose from multiple output formats and quality options for each download.</p>
                    </div>
                </div>
            </section>

            <section id="platforms" class="platforms">
                <div class="section-header">
                    <h2>Supported Platforms</h2>
                    <p>DataFox works with all these popular platforms and more</p>
                </div>
                <div class="platforms-grid">
                    <a href="#" class="platform" data-platform="youtube">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/>
                        </svg>
                        <span class="platform-name">YouTube</span>
                    </a>
                    <a href="#" class="platform" data-platform="facebook">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M22.675 0H1.325C.593 0 0 .593 0 1.325v21.351C0 23.407.593 24 1.325 24H12.82v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116c.73 0 1.323-.593 1.323-1.325V1.325C24 .593 23.407 0 22.675 0z"/>
                        </svg>
                        <span class="platform-name">Facebook</span>
                    </a>
                    <a href="#" class="platform" data-platform="instagram">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.272-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 1 0 0 12.324 6.162 6.162 0 0 0 0-12.324zM12 16a4 4 0 1 1 0-8 4 4 0 0 1 0 8zm6.406-11.845a1.44 1.44 0 1 0 0 2.881 1.44 1.44 0 0 0 0-2.881z"/>
                        </svg>
                        <span class="platform-name">Instagram</span>
                    </a>
                    <a href="#" class="platform" data-platform="twitter">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                        </svg>
                        <span class="platform-name">Twitter</span>
                    </a>
                    <a href="#" class="platform" data-platform="tiktok">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12.525.02c1.31-.02 2.61-.01 3.91-.02.08 1.53.63 3.09 1.75 4.17 1.12 1.11 2.7 1.62 4.24 1.79v4.03c-1.44-.05-2.89-.35-4.2-.97-.57-.26-1.1-.59-1.62-.93-.01 2.92.01 5.84-.02 8.75-.08 1.4-.54 2.79-1.35 3.94-1.31 1.92-3.58 3.17-5.91 3.21-1.43.08-2.86-.31-4.08-1.03-2.02-1.19-3.44-3.37-3.65-5.71-.02-.5-.03-1-.01-1.49.18-1.9 1.12-3.72 2.58-4.96 1.66-1.44 3.98-2.13 6.15-1.72.02 1.48-.04 2.96-.04 4.44-.99-.32-2.15-.23-3.02.37-.63.41-1.11 1.04-1.36 1.75-.21.51-.15 1.07-.14 1.61.24 1.64 1.82 3.02 3.5 2.87 1.12-.01 2.19-.66 2.77-1.61.19-.33.4-.67.41-1.06.1-1.79.06-3.57.07-5.36.01-4.03-.01-8.05.02-12.07z"/>
                        </svg>
                        <span class="platform-name">TikTok</span>
                    </a>
                    <a href="#" class="platform" data-platform="bilibili">
                        <span class="platform-name">Bilibili</span>
                    </a>
                    <a href="#" class="platform" data-platform="vk">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M15.072 12.621c-.428 0-.825-.221-.96-.576l-1.06-2.77-1.695 4.622a1.242 1.242 0 0 1-1.156.793 1.143 1.143 0 0 1-1.048-.675l-2.155-4.403-1.125 3.326c-.134.403-.506.675-.93.675H2.106a.947.947 0 0 1-.96-.933c0-.508.427-.933.96-.933h1.49l2.402-7.144c.134-.404.506-.676.93-.676.428 0 .825.221.96.576l1.922 4.147 1.922-4.147c.134-.355.532-.576.96-.576.428 0 .825.221.96.576l2.738 7.144h1.683c.534 0 .96.425.96.933a.947.947 0 0 1-.96.933h-2.307zm6.853-3.327c-.134-.404-.506-.676-.93-.676-.428 0-.825.221-.96.576l-.53 1.382h3.307l-.53-1.382a1.242 1.242 0 0 0-.96-.576c-.428 0-.825.221-.96.576l-2.498 6.48c-.134.355-.08.762.134 1.068.214.305.585.482.96.482.428 0 .825-.221.96-.576l.533-1.382h-3.307l.53 1.382c.134.355.532.576.96.576.428 0 .825-.221.96-.576l2.498-6.48c.134-.355.08-.762-.134-1.068z"/>
                        </svg>
                        <span class="platform-name">VK</span>
                    </a>
                    <a href="#" class="platform" data-platform="reddit">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M24 11.779c0-1.459-1.192-2.645-2.657-2.645H2.657C1.192 9.134 0 10.32 0 11.779v.438c0 1.459 1.192 2.645 2.657 2.645h18.686c1.465 0 2.657-1.186 2.657-2.645v-.438z"/>
                        </svg>
                        <span class="platform-name">Reddit</span>
                    </a>
                    <a href="#" class="platform" data-platform="tumblr">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M19.823 15.441a1.974 1.974 0 0 1-1.974 1.973h-3.21a.394.394 0 0 1-.394-.394v-5.526c0-.217.177-.394.394-.394h1.183c1.086 0 1.974.888 1.974 1.974v2.367zm-8.434-3.157v5.526a.394.394 0 0 1-.394.394H7.788a.394.394 0 0 1-.394-.394v-5.526c0-.217.177-.394.394-.394h1.183c.217 0 .394.177.394.394zm-4.341 1.183v4.343a.394.394 0 0 1-.394.394H3.21a.394.394 0 0 1-.394-.394v-4.343c0-.217.177-.394.394-.394h1.183c.217 0 .394.177.394.394zm12.13-4.736c0 1.086-.888 1.974-1.974 1.974h-1.183a.394.394 0 0 1-.394-.394V7.788a.394.394 0 0 1 .394-.394h1.183c1.086 0 1.974.888 1.974 1.974v1.183zm-4.735 0c0 1.086-.888 1.974-1.974 1.974h-1.183a.394.394 0 0 1-.394-.394V7.788a.394.394 0 0 1 .394-.394h1.183c1.086 0 1.974.888 1.974 1.974v1.183zm-4.736 0c0 1.086-.888 1.974-1.974 1.974H7.788a.394.394 0 0 1-.394-.394V7.788a.394.394 0 0 1 .394-.394h1.183c1.086 0 1.974.888 1.974 1.974v1.183z"/>
                        </svg>
                        <span class="platform-name">Tumblr</span>
                    </a>
                    <a href="#" class="platform" data-platform="vimeo">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M23.977 6.416c-.105 2.338-1.739 5.543-4.894 9.609-3.268 4.247-6.026 6.37-8.29 6.37-1.409 0-2.578-1.294-3.553-3.881L5.322 11.4C4.603 8.816 3.834 7.522 3.01 7.522c-.179 0-.806.378-1.881 1.132L0 7.197c1.185-1.044 2.351-2.084 3.501-3.128C5.08 2.701 6.266 1.984 7.055 1.91c1.867-.18 3.016 1.1 3.447 3.838.465 2.953.789 4.789.971 5.507.539 2.45 1.131 3.674 1.776 3.674.502 0 1.256-.796 2.265-2.385 1.004-1.589 1.54-2.797 1.612-3.628.144-1.371-.395-2.061-1.614-2.061-.574 0-1.167.121-1.777.391 1.186-3.868 3.434-5.757 6.762-5.637 2.473.06 3.628 1.664 3.493 4.797l-.013.01z"/>
                        </svg>
                        <span class="platform-name">Vimeo</span>
                    </a>
                    <a href="#" class="platform" data-platform="twitch">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M11.571 4.714h1.715v5.143H11.57zm4.715 0H18v5.143h-1.714zM6 0L1.714 4.286v15.428h5.143V24l4.286-4.286h3.428L22.286 12V0zm14.571 11.143l-3.428 3.428h-3.429l-3 3v-3H6.857V1.714h13.714Z"/>
                        </svg>
                        <span class="platform-name">Twitch</span>
                    </a>
                    <a href="#" class="platform" data-platform="soundcloud">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm0 22.5c-5.799 0-10.5-4.701-10.5-10.5S6.201 1.5 12 1.5 22.5 6.201 22.5 12 17.799 22.5 12 22.5zm5.045-6.711c-.184.368-.576.6-.984.6H7.939c-.415 0-.8-.232-.984-.6-.184-.368-.12-.816.16-1.112l4.057-4.898c.184-.184.415-.288.672-.288.249 0 .48.104.664.288l4.065 4.89c.272.304.336.752.152 1.12z"/>
                        </svg>
                        <span class="platform-name">SoundCloud</span>
                    </a>
                    <a href="#" class="platform" data-platform="pinterest">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12.001 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.386.6.11.819-.26.819-.578 0-.284-.01-1.04-.017-2.04-3.337.724-4.043-1.608-4.043-1.608-.546-1.386-1.332-1.754-1.332-1.754-1.09-.744.082-.729.082-.729 1.205.086 1.838 1.236 1.838 1.236 1.07 1.835 2.808 1.304 3.492.997.109-.775.419-1.305.762-1.604-2.665-.305-5.467-1.332-5.467-5.93 0-1.31.468-2.381 1.236-3.221-.124-.304-.536-1.524.118-3.176 0 0 1.007-.323 3.3 1.23.956-.266 1.983-.4 3.003-.404 1.02.005 2.046.138 3.005.404 2.29-1.553 3.296-1.23 3.296-1.23.655 1.652.243 2.872.12 3.176.77.84 1.234 1.911 1.234 3.221 0 4.61-2.806 5.621-5.478 5.921.43.37.814 1.103.814 2.222 0 1.606-.015 2.898-.015 3.293 0 .321.217.695.825.578C20.565 21.796 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
                        </svg>
                        <span class="platform-name">Pinterest</span>
                    </a>
                    <a href="#" class="platform" data-platform="dailymotion">
                        <span class="platform-name">Dailymotion</span>
                    </a>
                    <a href="#" class="platform" data-platform="snapchat">
                        <svg class="platform-icon" viewBox="0 0 24 24" fill="currentColor">
                            <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm0 22.5c-5.799 0-10.5-4.701-10.5-10.5S6.201 1.5 12 1.5 22.5 6.201 22.5 12 17.799 22.5 12 22.5zm5.045-6.711c-.184.368-.576.6-.984.6H7.939c-.415 0-.8-.232-.984-.6-.184-.368-.12-.816.16-1.112l4.057-4.898c.184-.184.415-.288.672-.288.249 0 .48.104.664.288l4.065 4.89c.272.304.336.752.152 1.12z"/>
                        </svg>
                        <span class="platform-name">Snapchat</span>
                    </a>
                    <a href="#" class="platform" data-platform="rutube">
                        <span class="platform-name">Rutube</span>
                    </a>
                    <a href="#" class="platform" data-platform="xiaohongshu">
                        <span class="platform-name">Xiaohongshu</span>
                    </a>
                    <a href="#" class="platform" data-platform="streamable">
                        <span class="platform-name">Streamable</span>
                    </a>
                    <a href="#" class="platform" data-platform="loom">
                        <span class="platform-name">Loom</span>
                    </a>
                </div>
            </section>

            <div class="disclaimer">
                <strong>Disclaimer:</strong> DataFox is a tool for downloading videos you have rights to or that are in the public domain. Downloading copyrighted content without permission may violate terms of service and copyright laws. Please respect content creators' rights and only download videos you're authorized to access.
            </div>
        </div>
    </main>

    <div class="processing-queue">
        <div class="queue-header">
            <div class="queue-title">DataFox Processing Queue</div>
            <div class="queue-actions">
                <button class="queue-btn" id="clear-queue" title="Clear all">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M3 6h18"></path>
                        <path d="M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6m3 0V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2"></path>
                    </svg>
                </button>
                <button class="queue-btn queue-close" title="Close">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <line x1="18" y1="6" x2="6" y2="18"></line>
                        <line x1="6" y1="6" x2="18" y2="18"></line>
                    </svg>
                </button>
            </div>
        </div>
        <div class="queue-items" id="queue-items"></div>
    </div>

    <div class="queue-badge hidden" id="queue-badge">0</div>

    <div class="toast-container" id="toast-container"></div>

    <footer>
        <div class="footer-content">
            <div class="footer-links">
                <a href="#privacy" class="footer-link">Privacy Policy</a>
                <a href="#terms" class="footer-link">Terms of Use</a>
                <a href="https://github.com/datafox-app" class="footer-link">GitHub</a>
                <a href="#contact" class="footer-link">Contact</a>
            </div>
            <div class="footer-copyright">
                &copy; 2023 DataFox Universal Video Downloader. All platform logos are property of their respective owners. This is a demo interface for educational purposes only.
            </div>
        </div>
    </footer>

    <script>
        class DataFox {
            constructor() {
                this.queue = [];
                this.initElements();
                this.initEventListeners();
                this.checkUrlParameters();
            }

            initElements() {
                this.downloadBtn = document.getElementById('download-btn');
                this.videoUrlInput = document.getElementById('video-url');
                this.platformSelect = document.getElementById('platform');
                this.queueBadge = document.getElementById('queue-badge');
                this.processingQueue = document.querySelector('.processing-queue');
                this.queueItems = document.getElementById('queue-items');
                this.queueCloseBtn = document.querySelector('.queue-close');
                this.clearQueueBtn = document.getElementById('clear-queue');
                this.toastContainer = document.getElementById('toast-container');
                this.mobileMenuBtn = document.querySelector('.mobile-menu-btn');
                this.nav = document.querySelector('.nav');
            }

            initEventListeners() {
                this.downloadBtn.addEventListener('click', (e) => this.handleDownloadClick(e));
                this.queueCloseBtn.addEventListener('click', () => this.toggleQueue());
                this.clearQueueBtn.addEventListener('click', () => this.clearQueue());
                this.queueBadge.addEventListener('click', () => this.toggleQueue());
                this.mobileMenuBtn.addEventListener('click', () => this.toggleMobileMenu());

                // Handle platform quick selection
                document.querySelectorAll('.platform').forEach(platform => {
                    platform.addEventListener('click', (e) => {
                        e.preventDefault();
                        this.platformSelect.value = platform.dataset.platform;
                        this.videoUrlInput.focus();
                        this.showToast(`Platform set to ${platform.querySelector('.platform-name').textContent}`, 'success');
                    });
                });

                // Add ripple effect to buttons
                document.addEventListener('click', (e) => {
                    if (e.target.classList.contains('btn')) {
                        this.createRipple(e);
                    }
                });
            }

            async handleDownloadClick(e) {
                const url = this.videoUrlInput.value.trim();
                const platform = this.platformSelect.value;

                if (!url) {
                    this.showToast('Please enter a video URL', 'error');
                    this.videoUrlInput.focus();
                    return;
                }

                if (!this.isValidUrl(url)) {
                    this.showToast('Please enter a valid URL', 'error');
                    return;
                }

                this.setButtonLoading(true);

                try {
                    // First check if the URL is from a supported platform
                    if (!this.isSupportedPlatform(url, platform)) {
                        this.showToast('This platform is not supported or URL is invalid', 'error');
                        return;
                    }

                    // Get video info (simulated in this demo)
                    const videoInfo = await this.getVideoInfo(url, platform);
                    
                    // On mobile, we might want to handle the download immediately
                    if (/Android|iPhone|iPad|iPod/i.test(navigator.userAgent)) {
                        this.showToast('Preparing download for mobile...', 'success');
                        await this.downloadItem({
                            id: 'mobile-' + Date.now(),
                            url,
                            platform,
                            fileName: `${this.extractFileNameFromUrl(url, platform)}.${platform === 'soundcloud' ? 'mp3' : 'mp4'}`,
                            status: 'completed'
                        });
                    } else {
                        // On desktop, add to queue
                        this.addToQueue(url, platform, videoInfo);
                    }
                } catch (error) {
                    this.showToast(`Error: ${error.message}`, 'error');
                    console.error('Download error:', error);
                } finally {
                    this.setButtonLoading(false);
                }
            }

            async getVideoInfo(url, platform) {
                // In a real implementation, this would call your backend API
                // For demo purposes, we'll simulate this with a timeout
                return new Promise((resolve) => {
                    setTimeout(() => {
                        const fileName = this.extractFileNameFromUrl(url, platform);
                        resolve({
                            id: Date.now().toString(),
                            url,
                            platform,
                            fileName: `${fileName}.${platform === 'soundcloud' ? 'mp3' : 'mp4'}`,
                            duration: Math.floor(Math.random() * 600) + 60, // Random duration 1-10 mins
                            thumbnail: this.getPlatformThumbnail(platform),
                            qualityOptions: ['1080p', '720p', '480p'] // Simulated quality options
                        });
                    }, 1000);
                });
            }

            getPlatformThumbnail(platform) {
                // Return platform-specific thumbnail placeholder
                const thumbnails = {
                    youtube: 'https://i.ytimg.com/vi/dQw4w9WgXcQ/maxresdefault.jpg',
                    vimeo: 'https://i.vimeocdn.com/video/12345_1280x720.jpg',
                    twitter: 'https://pbs.twimg.com/media/ABC123.jpg',
                    instagram: 'https://scontent.cdninstagram.com/v/t51.2885-15/12345_n.jpg',
                    default: 'https://via.placeholder.com/1280x720.png?text=Video+Thumbnail'
                };
                return thumbnails[platform] || thumbnails.default;
            }

            isSupportedPlatform(url, platform) {
                // Basic URL validation for supported platforms
                const platformPatterns = {
                    youtube: /(youtube\.com|youtu\.be)/,
                    vimeo: /vimeo\.com/,
                    twitter: /twitter\.com|t\.co|x\.com/,
                    instagram: /instagram\.com/,
                    tiktok: /tiktok\.com/,
                    facebook: /facebook\.com/,
                    soundcloud: /soundcloud\.com/,
                    dailymotion: /dailymotion\.com/,
                    twitch: /twitch\.tv/,
                    reddit: /reddit\.com/,
                    vk: /vk\.com/,
                    tumblr: /tumblr\.com/,
                    pinterest: /pinterest\.com/,
                    rutube: /rutube\.ru/,
                    xiaohongshu: /xiaohongshu\.com/,
                    streamable: /streamable\.com/,
                    loom: /loom\.com/
                };

                if (platform === 'auto') {
                    return Object.values(platformPatterns).some(pattern => pattern.test(url));
                }
                
                return platformPatterns[platform]?.test(url) || false;
            }

            addToQueue(url, platform, videoInfo) {
                const queueItem = {
                    id: videoInfo.id,
                    url,
                    platform,
                    fileName: videoInfo.fileName,
                    progress: 0,
                    status: 'processing',
                    info: videoInfo
                };

                this.queue.push(queueItem);
                this.updateQueueBadge();
                this.renderQueueItem(queueItem);
                this.processQueueItem(queueItem);
                this.showToast(`Added to queue: ${videoInfo.fileName}`, 'success');
            }

            async processQueueItem(item) {
                // Simulate processing stages
                const stages = [
                    { name: 'Fetching video data', duration: 1000 },
                    { name: 'Decoding stream', duration: 1500 },
                    { name: 'Processing metadata', duration: 800 },
                    { name: 'Finalizing download', duration: 1200 }
                ];

                for (const stage of stages) {
                    if (!this.queue.find(qi => qi.id === item.id)) break;
                    
                    this.updateQueueItemStatus(item.id, stage.name);
                    
                    // Simulate progress during this stage
                    const startProgress = item.progress;
                    const endProgress = startProgress + (100 / stages.length);
                    
                    await this.animateProgress(item.id, startProgress, endProgress, stage.duration);
                }

                // Mark as completed if still in queue
                if (this.queue.find(qi => qi.id === item.id)) {
                    const queueItem = this.queue.find(qi => qi.id === item.id);
                    queueItem.status = 'completed';
                    queueItem.progress = 100;
                    this.updateQueueItem(item.id);
                    this.showToast(`Processing complete: ${queueItem.fileName}`, 'success');
                }
            }

            async animateProgress(itemId, start, end, duration) {
                const startTime = performance.now();
                const updateProgress = (currentTime) => {
                    const elapsed = currentTime - startTime;
                    const progress = Math.min(start + (end - start) * (elapsed / duration), end);
                    
                    const queueItem = this.queue.find(qi => qi.id === itemId);
                    if (queueItem) {
                        queueItem.progress = progress;
                        this.updateQueueItem(itemId);
                    }
                    
                    if (elapsed < duration) {
                        requestAnimationFrame(updateProgress);
                    }
                };
                requestAnimationFrame(updateProgress);
                
                // Return a promise that resolves after the duration
                return new Promise(resolve => setTimeout(resolve, duration));
            }

            updateQueueItemStatus(itemId, statusText) {
                const queueItem = this.queue.find(item => item.id === itemId);
                if (queueItem) {
                    queueItem.statusText = statusText;
                    this.updateQueueItem(itemId);
                }
            }

            isValidUrl(url) {
                try {
                    new URL(url);
                    return true;
                } catch {
                    return false;
                }
            }

            setButtonLoading(isLoading) {
                if (isLoading) {
                    this.downloadBtn.classList.add('btn-loading');
                    this.downloadBtn.disabled = true;
                } else {
                    this.downloadBtn.classList.remove('btn-loading');
                    this.downloadBtn.disabled = false;
                }
            }

            extractFileNameFromUrl(url, platform) {
                try {
                    const urlObj = new URL(url);
                    const pathParts = urlObj.pathname.split('/').filter(part => part);
                    
                    // Platform-specific filename extraction
                    switch(platform) {
                        case 'youtube':
                            return urlObj.searchParams.get('v') || pathParts[pathParts.length - 1] || 'video';
                        case 'twitter':
                        case 'tiktok':
                            return pathParts[pathParts.length - 1] || 'video';
                        default:
                            return pathParts[pathParts.length - 1] || 'video';
                    }
                } catch {
                    return 'video';
                }
            }

            renderQueueItem(item) {
                const queueItem = document.createElement('div');
                queueItem.className = 'queue-item';
                queueItem.id = `queue-item-${item.id}`;
                queueItem.innerHTML = `
                    <svg class="queue-item-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
                        <polyline points="14 2 14 8 20 8"></polyline>
                    </svg>
                    <div class="queue-item-details">
                        <div class="queue-item-name">${item.fileName}</div>
                        <div class="queue-item-status">
                            <span>${item.statusText || this.getStatusText(item.status)}</span>
                            <span>${Math.round(item.progress)}%</span>
                        </div>
                        <div class="queue-item-progress">
                            <div class="queue-item-progress-bar" style="width: ${item.progress}%"></div>
                        </div>
                    </div>
                    <div class="queue-item-actions">
                        <button class="queue-item-btn" data-action="download" title="Download" ${item.status !== 'completed' ? 'disabled' : ''}>
                            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                                <polyline points="7 10 12 15 17 10"></polyline>
                                <line x1="12" y1="15" x2="12" y2="3"></line>
                            </svg>
                        </button>
                        <button class="queue-item-btn" data-action="remove" title="Remove">
                            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                                <line x1="18" y1="6" x2="6" y2="18"></line>
                                <line x1="6" y1="6" x2="18" y2="18"></line>
                            </svg>
                        </button>
                    </div>
                `;

                this.queueItems.appendChild(queueItem);

                // Add event listeners to action buttons
                queueItem.querySelector('[data-action="download"]').addEventListener('click', () => {
                    this.downloadItem(item);
                });

                queueItem.querySelector('[data-action="remove"]').addEventListener('click', () => {
                    this.removeFromQueue(item.id);
                });
            }

            getStatusText(status) {
                const statusMap = {
                    'processing': 'Processing locally...',
                    'completed': 'Ready to download',
                    'error': 'Error occurred'
                };
                return statusMap[status] || status;
            }

            updateQueueItem(id) {
                const queueItem = this.queue.find(item => item.id === id);
                if (!queueItem) return;

                const itemElement = document.getElementById(`queue-item-${id}`);
                if (!itemElement) return;

                // Update progress bar
                const progressBar = itemElement.querySelector('.queue-item-progress-bar');
                progressBar.style.width = `${queueItem.progress}%`;

                // Update status text
                const statusElement = itemElement.querySelector('.queue-item-status span:first-child');
                statusElement.textContent = queueItem.statusText || this.getStatusText(queueItem.status);

                // Update progress percentage
                const progressElement = itemElement.querySelector('.queue-item-status span:last-child');
                progressElement.textContent = `${Math.round(queueItem.progress)}%`;

                // Enable/disable download button
                const downloadBtn = itemElement.querySelector('[data-action="download"]');
                downloadBtn.disabled = queueItem.status !== 'completed';
            }

            async downloadItem(item) {
                try {
                    this.showToast(`Preparing download: ${item.fileName}`, 'success');
                    
                    // Create a dummy video file (in a real app, this would be the actual video)
                    const blob = new Blob([`This is a simulation of ${item.fileName}\n\n` + 
                                         `Original URL: ${item.url}\n` +
                                         `Platform: ${item.platform}\n` +
                                         `Filename: ${item.fileName}`], { type: 'text/plain' });
                    
                    // Different approach for mobile vs desktop
                    if (/Android|iPhone|iPad|iPod/i.test(navigator.userAgent)) {
                        // Mobile devices - use a different approach
                        const reader = new FileReader();
                        reader.onload = function() {
                            const base64data = reader.result;
                            const link = document.createElement('a');
                            link.href = base64data;
                            link.download = item.fileName;
                            document.body.appendChild(link);
                            
                            // For iOS, we need to trigger the click in a different way
                            if (typeof link.click === 'function') {
                                link.click();
                            } else {
                                const event = new MouseEvent('click', {
                                    view: window,
                                    bubbles: true,
                                    cancelable: true
                                });
                                link.dispatchEvent(event);
                            }
                            
                            setTimeout(() => {
                                document.body.removeChild(link);
                            }, 100);
                        };
                        reader.readAsDataURL(blob);
                    } else {
                        // Desktop browsers - standard approach
                        const url = URL.createObjectURL(blob);
                        const a = document.createElement('a');
                        a.href = url;
                        a.download = item.fileName;
                        document.body.appendChild(a);
                        a.click();
                        
                        setTimeout(() => {
                            document.body.removeChild(a);
                            URL.revokeObjectURL(url);
                        }, 100);
                    }
                    
                    // Remove from queue after download
                    this.removeFromQueue(item.id);
                    
                } catch (error) {
                    this.showToast(`Download failed: ${error.message}`, 'error');
                    console.error('Download error:', error);
                }
            }

            removeFromQueue(id) {
                this.queue = this.queue.filter(item => item.id !== id);
                const itemElement = document.getElementById(`queue-item-${id}`);
                if (itemElement) {
                    itemElement.classList.add('fade-out');
                    setTimeout(() => {
                        itemElement.remove();
                        this.updateQueueBadge();
                    }, 300);
                }
                this.updateQueueBadge();
            }

            clearQueue() {
                this.queue = [];
                this.queueItems.innerHTML = '';
                this.updateQueueBadge();
                this.showToast('Queue cleared', 'success');
            }

            updateQueueBadge() {
                const count = this.queue.length;
                this.queueBadge.textContent = count;
                
                if (count > 0) {
                    this.queueBadge.classList.remove('hidden');
                } else {
                    this.queueBadge.classList.add('hidden');
                    this.processingQueue.classList.remove('visible');
                }
            }

            toggleQueue() {
                this.processingQueue.classList.toggle('visible');
            }

            toggleMobileMenu() {
                this.nav.classList.toggle('visible');
            }

            showToast(message, type = 'success') {
                const toast = document.createElement('div');
                toast.className = `toast ${type}`;
                toast.innerHTML = `
                    <svg class="toast-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                        ${this.getToastIcon(type)}
                    </svg>
                    <div class="toast-message">${message}</div>
                    <button class="toast-close">
                        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <line x1="18" y1="6" x2="6" y2="18"></line>
                            <line x1="6" y1="6" x2="18" y2="18"></line>
                        </svg>
                    </button>
                `;

                this.toastContainer.appendChild(toast);

                // Auto-remove toast after delay
                setTimeout(() => {
                    toast.classList.add('fade-out');
                    setTimeout(() => toast.remove(), 300);
                }, 5000);

                // Close button
                toast.querySelector('.toast-close').addEventListener('click', () => {
                    toast.classList.add('fade-out');
                    setTimeout(() => toast.remove(), 300);
                });
            }

            getToastIcon(type) {
                const icons = {
                    'success': '<path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"></path><polyline points="22 4 12 14.01 9 11.01"></polyline>',
                    'error': '<path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path><line x1="12" y1="9" x2="12" y2="13"></line><line x1="12" y1="17" x2="12.01" y2="17"></line>',
                    'warning': '<path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path><line x1="12" y1="9" x2="12" y2="13"></line><line x1="12" y1="17" x2="12.01" y2="17"></line>'
                };
                return icons[type] || icons['success'];
            }

            createRipple(event) {
                const button = event.currentTarget;
                const circle = document.createElement("span");
                const diameter = Math.max(button.clientWidth, button.clientHeight);
                const radius = diameter / 2;

                circle.style.width = circle.style.height = `${diameter}px`;
                circle.style.left = `${event.clientX - button.getBoundingClientRect().left - radius}px`;
                circle.style.top = `${event.clientY - button.getBoundingClientRect().top - radius}px`;
                circle.classList.add("btn-ripple");

                const ripple = button.getElementsByClassName("btn-ripple")[0];
                if (ripple) {
                    ripple.remove();
                }

                button.appendChild(circle);
            }

            checkUrlParameters() {
                const urlParams = new URLSearchParams(window.location.search);
                const prefilledUrl = urlParams.get('u') || window.location.hash.substring(1);

                if (prefilledUrl) {
                    this.videoUrlInput.value = prefilledUrl;
                    this.showToast('URL detected from link', 'success');
                    
                    // Auto-start download if URL is prefilled
                    setTimeout(() => {
                        this.downloadBtn.click();
                    }, 1000);
                }
            }
        }

        // Initialize DataFox when DOM is loaded
        document.addEventListener('DOMContentLoaded', () => {
            const dataFox = new DataFox();
            
            // Expose to global scope for debugging
            window.dataFox = dataFox;
        });
    </script>
</body>
</html>
