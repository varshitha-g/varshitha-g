<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Varshitha Gudimalla - Data Engineer Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 2rem 0;
            margin-bottom: 2rem;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }
        
        .hero {
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            color: #2c3e50;
            margin-bottom: 0.5rem;
            background: linear-gradient(135deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hero .subtitle {
            font-size: 1.3rem;
            color: #7f8c8d;
            margin-bottom: 1rem;
        }
        
        .hero .tagline {
            font-size: 1.1rem;
            color: #34495e;
            font-style: italic;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .stat {
            text-align: center;
            padding: 1rem;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            border-radius: 10px;
            min-width: 150px;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            display: block;
        }
        
        .stat-label {
            font-size: 0.9rem;
            opacity: 0.9;
        }
        
        .section {
            background: white;
            margin: 2rem 0;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
        }
        
        .section h2 {
            color: #2c3e50;
            margin-bottom: 1.5rem;
            font-size: 2rem;
            border-bottom: 3px solid #667eea;
            padding-bottom: 0.5rem;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .tech-category {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 10px;
            border-left: 4px solid #667eea;
        }
        
        .tech-category h3 {
            color: #2c3e50;
            margin-bottom: 1rem;
            font-size: 1.2rem;
        }
        
        .tech-list {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        
        .tech-item {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            font-size: 0.9rem;
            box-shadow: 0 2px 5px rgba(102, 126, 234, 0.3);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 1.5rem;
        }
        
        .project-card {
            border: 1px solid #e9ecef;
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background: white;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
        }
        
        .project-header {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 1.5rem;
        }
        
        .project-title {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
        }
        
        .project-subtitle {
            opacity: 0.9;
            font-size: 0.9rem;
        }
        
        .project-body {
            padding: 1.5rem;
        }
        
        .project-challenge {
            background: #fff3cd;
            padding: 1rem;
            border-left: 4px solid #ffc107;
            margin-bottom: 1rem;
            border-radius: 5px;
        }
        
        .project-solution {
            background: #d1ecf1;
            padding: 1rem;
            border-left: 4px solid #17a2b8;
            margin-bottom: 1rem;
            border-radius: 5px;
        }
        
        .project-impact {
            background: #d4edda;
            padding: 1rem;
            border-left: 4px solid #28a745;
            margin-bottom: 1rem;
            border-radius: 5px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.3rem;
            margin-top: 1rem;
        }
        
        .project-tech-item {
            background: #f8f9fa;
            border: 1px solid #dee2e6;
            padding: 0.2rem 0.6rem;
            border-radius: 15px;
            font-size: 0.8rem;
            color: #495057;
        }
        
        .experience-timeline {
            position: relative;
            margin-top: 2rem;
        }
        
        .experience-timeline::before {
            content: '';
            position: absolute;
            left: 30px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(to bottom, #667eea, #764ba2);
            border-radius: 1px;
        }
        
        .experience-item {
            position: relative;
            margin-bottom: 3rem;
            padding-left: 80px;
        }
        
        .experience-item::before {
            content: '';
            position: absolute;
            left: 21px;
            top: 8px;
            width: 18px;
            height: 18px;
            background: linear-gradient(135deg, #667eea, #764ba2);
            border-radius: 50%;
            border: 3px solid white;
            box-shadow: 0 0 0 3px #667eea20;
        }
        
        .experience-header {
            margin-bottom: 1rem;
        }
        
        .experience-title {
            font-size: 1.4rem;
            color: #2c3e50;
            margin-bottom: 0.3rem;
            font-weight: 600;
        }
        
        .experience-company {
            font-size: 1.1rem;
            color: #667eea;
            font-weight: 500;
            margin-bottom: 0.2rem;
        }
        
        .experience-date {
            font-size: 0.9rem;
            color: #7f8c8d;
            font-style: italic;
        }
        
        .experience-description p {
            margin-bottom: 1rem;
            font-size: 1rem;
            line-height: 1.6;
        }
        
        .experience-description ul {
            list-style: none;
            padding: 0;
        }
        
        .experience-description li {
            position: relative;
            padding-left: 20px;
            margin-bottom: 0.8rem;
            line-height: 1.6;
        }
        
        .experience-description li::before {
            content: '▸';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
        }
        
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(450px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .education-item {
            background: linear-gradient(135deg, #f8f9ff, #fff);
            border: 1px solid #e9ecef;
            border-radius: 15px;
            padding: 2rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .education-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(135deg, #667eea, #764ba2);
        }
        
        .education-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 35px rgba(102, 126, 234, 0.2);
        }
        
        .education-header {
            margin-bottom: 1.5rem;
        }
        
        .education-degree {
            font-size: 1.3rem;
            color: #2c3e50;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }
        
        .education-school {
            font-size: 1.1rem;
            color: #667eea;
            font-weight: 500;
            margin-bottom: 0.3rem;
        }
        
        .education-location {
            font-size: 0.95rem;
            color: #7f8c8d;
            margin-bottom: 0.3rem;
        }
        
        .education-date {
            font-size: 0.9rem;
            color: #95a5a6;
            font-style: italic;
        }
        
        .education-description p {
            margin-bottom: 1.5rem;
            line-height: 1.6;
        }
        
        .coursework {
            margin-bottom: 1.5rem;
        }
        
        .coursework h4 {
            color: #2c3e50;
            margin-bottom: 0.8rem;
            font-size: 1rem;
        }
        
        .coursework-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        
        .coursework-tag {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 0.4rem 0.8rem;
            border-radius: 20px;
            font-size: 0.85rem;
            box-shadow: 0 2px 5px rgba(102, 126, 234, 0.3);
        }
        
        .achievements {
            display: flex;
            flex-direction: column;
            gap: 0.8rem;
        }
        
        .achievement-item {
            display: flex;
            align-items: center;
            gap: 0.8rem;
            background: rgba(102, 126, 234, 0.1);
            padding: 0.8rem;
            border-radius: 10px;
            border-left: 3px solid #667eea;
        }
        
        .achievement-icon {
            font-size: 1.2rem;
            flex-shrink: 0;
        }
        
        .achievement-item span:last-child {
            font-size: 0.9rem;
            line-height: 1.4;
        }
        
        .contact {
            text-align: center;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 3rem;
            border-radius: 15px;
            margin: 2rem 0;
        }
        
        .contact h2 {
            border: none;
            color: white;
            margin-bottom: 1rem;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }
        
        .contact-link {
            color: white;
            text-decoration: none;
            padding: 0.8rem 1.5rem;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 25px;
            transition: background 0.3s ease;
            backdrop-filter: blur(10px);
        }
        
        .contact-link:hover {
            background: rgba(255, 255, 255, 0.3);
        }
        
        .footer {
            text-align: center;
            padding: 2rem 0;
            color: white;
            background: rgba(0, 0, 0, 0.1);
            border-radius: 15px;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }
            
            .stats {
                flex-direction: column;
                align-items: center;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .education-grid {
                grid-template-columns: 1fr;
            }
            
            .education-item {
                min-width: auto;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="hero">
                <h1>Varshitha Gudimalla</h1>
                <p class="subtitle">Data Engineer | Cloud Architecture Enthusiast | ML Pipeline Builder</p>
                <p class="tagline">Transforming complex data challenges into scalable business solutions across healthcare, analytics, and Fortune 500 logistics</p>
                
                <div class="stats">
                    <div class="stat">
                        <span class="stat-number">3</span>
                        <span class="stat-label">Industries Transformed</span>
                    </div>
            </section>
            
            <section class="section">
                <h2>Education</h2>
                
                <div class="education-grid">
                    <div class="education-item">
                        <div class="education-header">
                            <h3 class="education-degree">Masters of Science in Data Science</h3>
                            <div class="education-school">University at Albany</div>
                            <div class="education-location">Albany, New York</div>
                            <div class="education-date">August 2023 – May 2025</div>
                        </div>
                        <div class="education-description">
                            <p><strong>Advanced data science mastery</strong> combining theoretical foundations with practical applications in distributed computing and cloud architecture.</p>
                            <div class="coursework">
                                <h4>Key Coursework:</h4>
                                <div class="coursework-tags">
                                    <span class="coursework-tag">Advanced Statistics</span>
                                    <span class="coursework-tag">Machine Learning</span>
                                    <span class="coursework-tag">Big Data Analytics</span>
                                    <span class="coursework-tag">Data Mining</span>
                                    <span class="coursework-tag">Business Intelligence</span>
                                    <span class="coursework-tag">Statistical Computing</span>
                                </div>
                            </div>
                            <div class="achievements">
                                <div class="achievement-item">
                                    <span class="achievement-icon">🏆</span>
                                    <span>Maintained academic excellence while working full-time</span>
                                </div>
                                <div class="achievement-item">
                                    <span class="achievement-icon">💡</span>
                                    <span>Developed cutting-edge capstone project with real-world ML pipeline</span>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="education-item">
                        <div class="education-header">
                            <h3 class="education-degree">Bachelors of Technology in Computer Science</h3>
                            <div class="education-school">CMR Institute of Technology</div>
                            <div class="education-location">Hyderabad, India</div>
                            <div class="education-date">August 2018 – May 2022</div>
                        </div>
                        <div class="education-description">
                            <p><strong>Comprehensive computer science foundation</strong> that laid the groundwork for a successful career in data engineering and analytics.</p>
                            <div class="coursework">
                                <h4>Core Foundation:</h4>
                                <div class="coursework-tags">
                                    <span class="coursework-tag">Data Structures & Algorithms</span>
                                    <span class="coursework-tag">Database Management Systems</span>
                                    <span class="coursework-tag">Software Engineering</span>
                                    <span class="coursework-tag">Object-Oriented Programming</span>
                                    <span class="coursework-tag">Web Technologies</span>
                                    <span class="coursework-tag">Computer Networks</span>
                                </div>
                            </div>
                            
                        </div>
                    </div>
                </div>
                    <div class="stat">
                        <span class="stat-number">10M+</span>
                        <span class="stat-label">Daily Records Processed</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">80%</span>
                        <span class="stat-label">Processing Time Reduced</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">$50M+</span>
                        <span class="stat-label">Revenue Protected</span>
                    </div>
                </div>
            </div>
        </header>
        
        <main>
            <section class="section">
                <h2>Technical Expertise</h2>
                <div class="tech-grid">
                    <div class="tech-category">
                        <h3>Programming & Processing</h3>
                        <div class="tech-list">
                            <span class="tech-item">Python</span>
                            <span class="tech-item">SQL</span>
                            <span class="tech-item">PySpark</span>
                            <span class="tech-item">Apache Spark</span>
                            <span class="tech-item">Delta Lake</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3>Cloud Platforms</h3>
                        <div class="tech-list">
                            <span class="tech-item">AWS</span>
                            <span class="tech-item">Azure</span>
                            <span class="tech-item">GCP</span>
                            <span class="tech-item">Databricks</span>
                            <span class="tech-item">Snowflake</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3>Workflow Orchestration</h3>
                        <div class="tech-list">
                            <span class="tech-item">Apache Airflow</span>
                            <span class="tech-item">Databricks Workflows</span>
                            <span class="tech-item">Jenkins</span>
                            <span class="tech-item">AWS Step Functions</span>
                        </div>
                    </div>
                    
                    <div class="tech-category">
                        <h3>Data Quality & Visualization</h3>
                        <div class="tech-list">
                            <span class="tech-item">Great Expectations</span>
                            <span class="tech-item">Power BI</span>
                            <span class="tech-item">Tableau</span>
                            <span class="tech-item">MLflow</span>
                            <span class="tech-item">Unity Catalog</span>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="section">
                <h2>Professional Experience</h2>
                
                <div class="experience-timeline">
                    <div class="experience-item">
                        <div class="experience-header">
                            <h3 class="experience-title">Data Engineer</h3>
                            <div class="experience-company">FedEx</div>
                            <div class="experience-date">January 2025 – Present</div>
                        </div>
                        <div class="experience-description">
                            <p><strong>Transforming Fortune 500 logistics data infrastructure</strong> for real-time analytics and ML-driven insights across global shipping networks.</p>
                            <ul>
                                <li>Developing scalable ETL pipelines in Databricks using PySpark, Delta Lake, and Python to process high-volume transactional and PII datasets from logistics, customer interaction, and order management systems</li>
                                <li>Orchestrating automated end-to-end data workflows using Apache Airflow, Databricks Workflows, AWS Step Functions, and Jenkins for daily ingestion, transformation, and validation with minimal manual intervention</li>
                                <li>Implementing robust data quality frameworks using Great Expectations and Delta Lake constraints, ensuring integrity across regulatory PII data pipelines supporting fraud detection, churn modeling, and logistics prediction</li>
                                <li>Collaborating with cross-functional teams to optimize pipeline performance, enforce access control on sensitive data, and enable CI/CD with Git-based version control</li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="experience-item">
                        <div class="experience-header">
                            <h3 class="experience-title">Graduate Student & Research Assistant</h3>
                            <div class="experience-company">University at Albany</div>
                            <div class="experience-date">August 2023 – December 2024</div>
                        </div>
                        <div class="experience-description">
                            <p><strong>Advanced data science mastery</strong> while staying connected to industry trends and maintaining technical excellence.</p>
                            <ul>
                                <li>Completed intensive coursework in Machine Learning, Big Data Analytics, and Statistical Computing while maintaining academic excellence</li>
                                <li>Developed cutting-edge capstone project building end-to-end ML pipeline demonstrating real-world application of distributed computing and cloud architecture</li>
                                <li>Maintained hands-on development with modern data stack, ensuring seamless transition back to industry with fresh academic insights</li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="experience-item">
                        <div class="experience-header">
                            <h3 class="experience-title">Data Engineer</h3>
                            <div class="experience-company">Knowledge Solutions</div>
                            <div class="experience-date">June 2022 – July 2023</div>
                        </div>
                        <div class="experience-description">
                            <p><strong>Revolutionizing customer analytics capabilities</strong> through advanced data processing and predictive insights.</p>
                            <ul>
                                <li>Developed PySpark-based ETL pipelines in Databricks transforming ~50K weekly customer survey and transactional datasets for NPS prediction, churn analysis, and cost optimization</li>
                                <li>Implemented end-to-end orchestration using Apache Airflow and AWS DataSync, automating data movement from on-premise sources into AWS S3 for centralized analytics</li>
                                <li>Built interactive Power BI dashboards tracking CSAT, NPS, and churn KPIs with scheduled updates and Salesforce CRM integration for real-time customer insights</li>
                                <li>Collaborated with data scientists to prepare ML-ready feature tables for fraud detection, sentiment analysis, and retention modeling pipelines</li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="experience-item">
                        <div class="experience-header">
                            <h3 class="experience-title">Data Engineer</h3>
                            <div class="experience-company">CloudEnd Platform Pvt Ltd</div>
                            <div class="experience-date">January 2021 – May 2022</div>
                        </div>
                        <div class="experience-description">
                            <p><strong>Pioneering healthcare data infrastructure</strong> with HIPAA-compliant systems and predictive analytics for improved patient outcomes.</p>
                            <ul>
                                <li>Constructed ETL pipelines using Databricks, AWS Glue, and PySpark to process therapy logs and survey responses into Delta Lake for compliance and analytics</li>
                                <li>Built forecasting pipelines using Python and Prophet in Databricks to predict patient adherence and treatment outcomes, supporting clinical strategy decisions</li>
                                <li>Maintained comprehensive documentation, Git version control, and IAM-based access policies aligned with healthcare data governance standards</li>
                                <li>Scheduled and monitored workflows using Apache Airflow DAGs with deployment automation via Jenkins for reliable nightly refreshes</li>
                            </ul>
                        </div>
                    </div>
                </div>
            
            <section class="section">
                <h2>Featured Projects</h2>
                <div class="projects-grid">
                    <div class="project-card">
                        <div class="project-header">
                            <h3 class="project-title">Global Inflation Monitor</h3>
                            <p class="project-subtitle">Real-time economic intelligence platform</p>
                        </div>
                        <div class="project-body">
                            <div class="project-challenge">
                                <strong>Challenge:</strong> Economic analysts were spending 5 days manually compiling inflation data from 190+ countries, creating dangerous delays during volatile market conditions.
                            </div>
                            <div class="project-solution">
                                <strong>Solution:</strong> Built automated Spark and Snowflake pipeline processing 2M+ daily economic indicators from multiple government and financial APIs.
                            </div>
                            <div class="project-impact">
                                <strong>Impact:</strong> 80% reduction in reporting time (5 days → 4 hours), enabling real-time policy decisions during critical economic periods.
                            </div>
                            <div class="project-tech">
                                <span class="project-tech-item">Python</span>
                                <span class="project-tech-item">Apache Spark</span>
                                <span class="project-tech-item">Snowflake</span>
                                <span class="project-tech-item">Tableau</span>
                                <span class="project-tech-item">AWS</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="project-card">
                        <div class="project-header">
                            <h3 class="project-title">Customer Churn Prediction Engine</h3>
                            <p class="project-subtitle">ML-powered retention intelligence system</p>
                        </div>
                        <div class="project-body">
                            <div class="project-challenge">
                                <strong>Challenge:</strong> Telecom company losing 25% of customers annually with no early warning system, reactive retention strategies costing millions.
                            </div>
                            <div class="project-solution">
                                <strong>Solution:</strong> Developed end-to-end ML pipeline analyzing 500K+ customer behavioral patterns, transaction histories, and engagement metrics.
                            </div>
                            <div class="project-impact">
                                <strong>Impact:</strong> 87% prediction accuracy identifying at-risk customers 60 days in advance, saving $2.3M annually through targeted retention.
                            </div>
                            <div class="project-tech">
                                <span class="project-tech-item">Python</span>
                                <span class="project-tech-item">scikit-learn</span>
                                <span class="project-tech-item">Apache Airflow</span>
                                <span class="project-tech-item">MLflow</span>
                                <span class="project-tech-item">Databricks</span>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="contact">
                <h2>Let's Build Something Amazing Together</h2>
                <p>Ready to transform your data challenges into business victories? With experience across healthcare (CloudEnd Platform), customer analytics (Knowledge Solutions), and enterprise logistics (FedEx), I bring diverse industry insights to every data engineering challenge.</p>
                <div class="contact-links">
                    <a href="mailto:varshithag1908@gmail.com" class="contact-link">📧 Email Me</a>
                    <a href="tel:+15185287072" class="contact-link">Call Me</a>
                    <a href="https://linkedin.com/in/your-profile" class="contact-link">LinkedIn</a>
                    <a href="https://github.com/varshitha-g" class="contact-link">GitHub</a>
                </div>
            </section>
        </main>
        
        <footer class="footer">
            <p>&copy; 2025 Varshitha Gudimalla. Turning data into business impact, one pipeline at a time.</p>
        </footer>
    </div>
</body>
</html>
