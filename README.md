<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Download Financial Calculators Website</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        .download-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 3rem;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            max-width: 600px;
            width: 100%;
        }
        
        .download-icon {
            font-size: 4rem;
            color: #667eea;
            margin-bottom: 1.5rem;
        }
        
        h1 {
            color: #2c3e50;
            font-size: 2.2rem;
            margin-bottom: 1rem;
        }
        
        .description {
            color: #6c757d;
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 2rem;
        }
        
        .download-btn {
            display: inline-flex;
            align-items: center;
            gap: 0.8rem;
            background: linear-gradient(135deg, #28a745, #20c997);
            color: white;
            padding: 1rem 2rem;
            text-decoration: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(40, 167, 69, 0.3);
        }
        
        .download-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(40, 167, 69, 0.4);
        }
        
        .file-info {
            margin-top: 2rem;
            padding: 1.5rem;
            background: #f8f9fa;
            border-radius: 12px;
            border-left: 4px solid #007bff;
        }
        
        .file-info h3 {
            color: #2c3e50;
            margin-bottom: 0.8rem;
        }
        
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin-bottom: 1rem;
        }
        
        .info-item {
            text-align: left;
        }
        
        .info-label {
            font-weight: 600;
            color: #495057;
            font-size: 0.9rem;
        }
        
        .info-value {
            color: #6c757d;
            font-size: 0.9rem;
        }
        
        .features {
            text-align: left;
            margin-top: 1rem;
        }
        
        .features li {
            color: #6c757d;
            margin: 0.5rem 0;
            list-style: none;
            position: relative;
            padding-left: 1.5rem;
        }
        
        .features li::before {
            content: "✓";
            color: #28a745;
            font-weight: bold;
            position: absolute;
            left: 0;
        }
        
        .back-link {
            display: inline-block;
            margin-top: 2rem;
            color: #667eea;
            text-decoration: none;
            font-weight: 500;
        }
        
        .back-link:hover {
            text-decoration: underline;
        }
        
        @media (max-width: 768px) {
            .download-card {
                padding: 2rem;
            }
            
            h1 {
                font-size: 1.8rem;
            }
            
            .info-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
</head>
<body>
    <div class="download-card">
        <i class="fas fa-download download-icon"></i>
        <h1>Financial Calculators Website</h1>
        <p class="description">
            Your complete financial calculator suite is ready for download! This production-ready package includes all three calculators optimized for web hosting.
        </p>
        
        <a href="production-build/financial-calculators-website.zip" class="download-btn" download>
            <i class="fas fa-download"></i>
            Download Website (32 KB)
        </a>
        
        <div class="file-info">
            <h3>Package Contents</h3>
            <div class="info-grid">
                <div class="info-item">
                    <div class="info-label">File Size:</div>
                    <div class="info-value">32 KB (compressed)</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Format:</div>
                    <div class="info-value">ZIP Archive</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Files:</div>
                    <div class="info-value">12 total files</div>
                </div>
                <div class="info-item">
                    <div class="info-label">Calculators:</div>
                    <div class="info-value">3 complete tools</div>
                </div>
            </div>
            
            <div class="features">
                <strong>What's Included:</strong>
                <ul>
                    <li>Percentage Calculator (with 3 calculation modes)</li>
                    <li>EMI Calculator (with interactive charts)</li>
                    <li>eCommerce Profit Calculator (complete business analysis)</li>
                    <li>Organized CSS and JavaScript files</li>
                    <li>Complete deployment guide</li>
                    <li>SEO-optimized HTML structure</li>
                    <li>Mobile-responsive design</li>
                    <li>Production-ready code</li>
                </ul>
            </div>
        </div>
        
        <a href="/" class="back-link">
            <i class="fas fa-arrow-left"></i>
            Back to Calculator
        </a>
    </div>
</body>
</html>
