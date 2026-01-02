<!--
author:   Mahwish Kanwal, Sabbir Rifat
email:    mahwish.kanwal@ovgu.de, a.rifat@ovgu.de
version:  3.0.0
language: en
narrator: US English Female
comment:  Module 1: Technical Foundations of AI Agents - Deep dive into architecture, components, and operational principles

@style
.stat-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
    margin: 25px 0;
    font-size: 1.4em;
    font-weight: bold;
    text-align: center;
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
    animation: pulse 2s infinite;
}

@keyframes pulse {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.02); }
}

.roadmap-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 25px;
    margin: 30px 0;
    padding: 20px;
}

@media (max-width: 1024px) {
    .roadmap-container {
        grid-template-columns: 1fr;
    }
}

.roadmap-tile {
    background: rgba(173, 216, 230, 0.3);
    border: 2px solid rgba(100, 149, 237, 0.4);
    color: #2c3e50;
    padding: 30px;
    border-radius: 15px;
    box-shadow: 0 8px 20px rgba(100, 149, 237, 0.2);
    transition: all 0.3s ease;
    cursor: pointer;
}

.roadmap-tile:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 12px 30px rgba(100, 149, 237, 0.35);
    background: rgba(173, 216, 230, 0.45);
}

.roadmap-tile h3 {
    font-size: 1.4em;
    margin-bottom: 15px;
    border-bottom: 3px solid rgba(100, 149, 237, 0.5);
    padding-bottom: 10px;
    color: #1e3a5f;
    font-weight: bold;
}

.roadmap-tile ul {
    list-style: none;
    padding-left: 0;
}

.roadmap-tile li {
    padding: 8px 0;
    font-size: 1.05em;
    line-height: 1.6;
    color: #34495e;
}

.roadmap-tile .time {
    background: rgba(100, 149, 237, 0.25);
    padding: 4px 10px;
    border-radius: 5px;
    font-size: 0.85em;
    float: right;
    color: #1e3a5f;
    font-weight: 600;
}

.cycle-step {
    background: linear-gradient(135deg, rgba(236, 240, 253, 0.9) 0%, rgba(220, 230, 255, 0.9) 100%);
    border-left: 5px solid #667eea;
    padding: 25px;
    margin: 20px 0;
    border-radius: 12px;
    box-shadow: 0 4px 15px rgba(102, 126, 234, 0.2);
    transition: all 0.3s ease;
    cursor: pointer;
}

.cycle-step:hover {
    transform: translateX(10px) scale(1.02);
    box-shadow: 0 8px 25px rgba(102, 126, 234, 0.35);
    border-left-width: 8px;
    background: linear-gradient(135deg, rgba(236, 240, 253, 1) 0%, rgba(220, 230, 255, 1) 100%);
}

.cycle-step h4 {
    font-size: 1.4em;
    color: #667eea;
    margin-bottom: 12px;
    font-weight: bold;
}

.cycle-step .step-icon {
    font-size: 2em;
    margin-right: 10px;
    vertical-align: middle;
}

.cycle-step ul {
    margin: 10px 0;
    padding-left: 20px;
}

.cycle-step li {
    margin: 8px 0;
    line-height: 1.6;
    color: #34495e;
}

.cycle-step .step-label {
    background: rgba(102, 126, 234, 0.15);
    padding: 5px 12px;
    border-radius: 6px;
    font-weight: 600;
    color: #667eea;
    display: inline-block;
    margin-bottom: 10px;
}

.cycle-diagram {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
    font-family: Arial, sans-serif;
}

.cycle-box {
    background-color: rgba(70, 130, 220, 0.15);
    border: 2px solid rgba(70, 130, 220, 0.5);
    border-radius: 8px;
    padding: 25px;
    margin: 20px 0;
}

.cycle-box h4 {
    margin: 0 0 15px 0;
    font-size: 24px;
    color: #2c3e50;
    font-weight: bold;
}

.cycle-box p {
    margin: 8px 0;
    font-size: 18px;
    color: #2c3e50;
    line-height: 1.6;
}

.content-list {
    margin-top: 10px;
}

.content-item {
    margin: 8px 0;
    font-size: 18px;
    color: #2c3e50;
    line-height: 1.5;
}

.arrow {
    text-align: center;
    font-size: 32px;
    margin: 10px 0;
    color: #4682dc;
}

.cycle-label {
    text-align: center;
    font-size: 18px;
    font-style: italic;
    margin: 10px 0;
    color: #4682dc;
    font-weight: 600;
}

.feedback-arrow {
    text-align: center;
    font-size: 36px;
    margin: 15px 0;
}

.emoji {
    font-size: 26px;
    margin-right: 8px;
}

.architecture-box {
    background: linear-gradient(135deg, #E8F4F8 0%, #D4E9F2 100%);
    border-left: 10px solid #2980b9;
    padding: 30px;
    margin: 25px 0;
    border-radius: 12px;
    font-size: 1.1em;
    line-height: 1.9;
    box-shadow: 0 4px 8px rgba(0,0,0,0.12);
}

.component-card {
    background: #ffffff;
    border: 3px solid #3498db;
    padding: 25px;
    margin: 20px 0;
    border-radius: 12px;
    box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    transition: transform 0.3s;
}

.component-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
}

.key-point {
    background: linear-gradient(135deg, #E8F5E9 0%, #C8E6C9 100%);
    border-left: 10px solid #27ae60;
    padding: 25px;
    margin: 25px 0;
    border-radius: 12px;
    font-weight: bold;
    font-size: 1.15em;
}

.definition-box {
    background: linear-gradient(135deg, #FFF9E6 0%, #FFE6B2 100%);
    border-left: 10px solid #f39c12;
    padding: 30px;
    margin: 25px 0;
    border-radius: 12px;
    font-size: 1.2em;
    line-height: 1.9;
    box-shadow: 0 4px 8px rgba(0,0,0,0.12);
}

.interactive-box {
    background: linear-gradient(135deg, #fff5f5 0%, #ffe6e6 100%);
    border: 4px dashed #e74c3c;
    padding: 30px;
    margin: 25px 0;
    border-radius: 15px;
    font-size: 1.1em;
}

table {
    border-collapse: collapse;
    width: 100%;
    margin: 25px 0;
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    font-size: 1.05em;
}

th {
    background: linear-gradient(135deg, #2C3E50 0%, #34495E 100%);
    color: white;
    padding: 18px;
    text-align: left;
    font-weight: bold;
    font-size: 1.1em;
}

td {
    padding: 15px 18px;
    border-bottom: 2px solid #E0E0E0;
}

tr:nth-child(even) {
    background-color: #f8f9fa;
}

tr:hover {
    background-color: #e3f2fd;
    transition: background-color 0.3s;
}

.comparison-grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 12px;
    margin: 20px 0;
}

.paradigm-card {
    background: white;
    border: 2px solid #9b59b6;
    border-radius: 10px;
    padding: 12px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    font-size: 0.75em;
    transition: all 0.3s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
}

.paradigm-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.15);
}

.paradigm-card h4 {
    font-size: 1em;
    margin-bottom: 8px;
    color: #9b59b6;
    text-align: center;
}

.paradigm-card ul {
    list-style: none;
    padding: 0;
    margin: 6px 0;
}

.paradigm-card li {
    padding: 2px 0;
    font-size: 1em;
    line-height: 1.3;
}

.paradigm-card strong {
    font-size: 1em;
    color: #2c3e50;
}

.paradigm-card pre {
    font-size: 1em;
    margin: 6px 0;
}

@media (max-width: 1200px) {
    .comparison-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .comparison-grid {
        grid-template-columns: 1fr;
    }
}

.characteristics-header {
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 15px;
    border-radius: 10px;
    margin: 20px 0;
    font-size: 1.1em;
    font-weight: bold;
    box-shadow: 0 6px 15px rgba(102, 126, 234, 0.3);
    animation: pulse 2s infinite;
}

.char-card {
    background: white;
    border-radius: 12px;
    padding: 18px;
    margin: 15px 0;
    box-shadow: 0 6px 15px rgba(0,0,0,0.12);
    transition: all 0.3s ease;
    cursor: pointer;
    border: 2px solid transparent;
    font-size: 1.15em;
}

.char-card:hover {
    transform: translateY(-5px) scale(1.01);
    box-shadow: 0 10px 25px rgba(0,0,0,0.18);
}

.char-autonomy {
    border-color: #f093fb;
    background: linear-gradient(135deg, rgba(240, 147, 251, 0.05) 0%, rgba(245, 87, 108, 0.05) 100%);
}

.char-autonomy:hover {
    border-color: #f5576c;
    background: linear-gradient(135deg, rgba(240, 147, 251, 0.1) 0%, rgba(245, 87, 108, 0.1) 100%);
}

.char-task {
    border-color: #4facfe;
    background: linear-gradient(135deg, rgba(79, 172, 254, 0.05) 0%, rgba(0, 242, 254, 0.05) 100%);
}

.char-task:hover {
    border-color: #00f2fe;
    background: linear-gradient(135deg, rgba(79, 172, 254, 0.1) 0%, rgba(0, 242, 254, 0.1) 100%);
}

.char-reactive {
    border-color: #43e97b;
    background: linear-gradient(135deg, rgba(67, 233, 123, 0.05) 0%, rgba(56, 249, 215, 0.05) 100%);
}

.char-reactive:hover {
    border-color: #38f9d7;
    background: linear-gradient(135deg, rgba(67, 233, 123, 0.1) 0%, rgba(56, 249, 215, 0.1) 100%);
}

.char-icon {
    font-size: 2.2em;
    text-align: center;
    margin-bottom: 8px;
    animation: bounce 2s ease-in-out infinite;
}

.char-title {
    font-size: 1.3em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 10px;
    color: #2c3e50;
}

.char-definition {
    background: rgba(102, 126, 234, 0.1);
    padding: 10px;
    border-radius: 8px;
    margin: 10px 0;
    font-weight: 600;
    font-size: 1em;
    color: #667eea;
}

.autonomy-levels {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    margin: 12px 0;
}

.level-box {
    flex: 1;
    padding: 12px;
    border-radius: 8px;
    text-align: center;
    transition: all 0.3s ease;
}

.level-low {
    background: linear-gradient(135deg, #ffeaa7 0%, #fdcb6e 100%);
    border: 2px solid #fdcb6e;
}

.level-low:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 20px rgba(253, 203, 110, 0.4);
}

.level-medium {
    background: linear-gradient(135deg, #74b9ff 0%, #0984e3 100%);
    border: 2px solid #0984e3;
    color: white;
}

.level-medium:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 20px rgba(9, 132, 227, 0.4);
}

.level-high {
    background: linear-gradient(135deg, #00b894 0%, #00cec9 100%);
    border: 2px solid #00b894;
    color: white;
}

.level-high:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 20px rgba(0, 184, 148, 0.4);
}

.level-box h4 {
    margin: 0 0 6px 0;
    font-size: 1.05em;
}

.level-box p {
    margin: 3px 0;
    font-size: 0.85em;
    line-height: 1.3;
}

@media (max-width: 768px) {
    .autonomy-levels {
        flex-direction: column;
    }
}

.architecture-header {
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 15px;
    border-radius: 10px;
    margin: 20px 0;
    font-size: 1.1em;
    font-weight: bold;
    box-shadow: 0 6px 15px rgba(102, 126, 234, 0.3);
    animation: pulse 2s infinite;
}

.layer-stack {
    position: relative;
    margin: 25px auto;
    max-width: 1000px;
}

.layer-card {
    background: white;
    border-radius: 12px;
    padding: 18px;
    margin: 15px 0;
    box-shadow: 0 6px 15px rgba(0,0,0,0.12);
    transition: all 0.3s ease;
    cursor: pointer;
    border: 2px solid transparent;
    position: relative;
}

.layer-card:hover {
    transform: translateY(-5px) scale(1.01);
    box-shadow: 0 10px 25px rgba(0,0,0,0.18);
}

.layer-app {
    border-color: #ff6b6b;
    background: linear-gradient(135deg, rgba(255, 107, 107, 0.05) 0%, rgba(238, 82, 83, 0.05) 100%);
}

.layer-app:hover {
    border-color: #ee5253;
    background: linear-gradient(135deg, rgba(255, 107, 107, 0.1) 0%, rgba(238, 82, 83, 0.1) 100%);
}

.layer-orch {
    border-color: #4facfe;
    background: linear-gradient(135deg, rgba(79, 172, 254, 0.05) 0%, rgba(0, 242, 254, 0.05) 100%);
}

.layer-orch:hover {
    border-color: #00f2fe;
    background: linear-gradient(135deg, rgba(79, 172, 254, 0.1) 0%, rgba(0, 242, 254, 0.1) 100%);
}

.layer-reason {
    border-color: #48dbfb;
    background: linear-gradient(135deg, rgba(72, 219, 251, 0.05) 0%, rgba(0, 184, 217, 0.05) 100%);
}

.layer-reason:hover {
    border-color: #00b8d9;
    background: linear-gradient(135deg, rgba(72, 219, 251, 0.1) 0%, rgba(0, 184, 217, 0.1) 100%);
}

.layer-icon {
    font-size: 1.8em;
    text-align: center;
    margin-bottom: 8px;
    animation: bounce 2s ease-in-out infinite;
}

.layer-title {
    font-size: 1.1em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 10px;
    color: #2c3e50;
}

.layer-purpose {
    background: rgba(102, 126, 234, 0.1);
    padding: 10px;
    border-radius: 8px;
    margin: 10px 0;
    font-weight: 600;
    font-size: 0.85em;
    color: #667eea;
    text-align: center;
}

.layer-features {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 8px;
    margin: 12px 0;
}

.feature-item {
    background: rgba(255, 255, 255, 0.8);
    padding: 8px 10px;
    border-radius: 6px;
    font-size: 0.75em;
    border-left: 2px solid #667eea;
    line-height: 1.3;
}

.tech-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 15px;
    justify-content: center;
}

.tech-tag {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 8px 15px;
    border-radius: 20px;
    font-size: 0.85em;
    font-weight: 600;
}

.layer-connector {
    text-align: center;
    font-size: 1.5em;
    color: #667eea;
    margin: -8px 0;
    animation: slide-down 2s ease-in-out infinite;
}

@media (max-width: 768px) {
    .layer-features {
        grid-template-columns: 1fr;
    }
}

/* Evolution Section Styles */
.evolution-container {
    margin: 40px 0;
}

.evolution-header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 25px;
    border-radius: 15px;
    text-align: center;
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: 30px;
    box-shadow: 0 8px 20px rgba(102, 126, 234, 0.3);
    animation: pulse 2s infinite;
}

.evolution-comparison {
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    gap: 30px;
    margin: 30px 0;
    align-items: center;
}

.evolution-side {
    background: white;
    border-radius: 20px;
    padding: 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
    transition: all 0.3s ease;
}

.evolution-side:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.25);
}

.traditional-agent {
    border: 3px solid #e74c3c;
    background: linear-gradient(135deg, rgba(231, 76, 60, 0.05) 0%, rgba(192, 57, 43, 0.05) 100%);
}

.agentic-ai {
    border: 3px solid #27ae60;
    background: linear-gradient(135deg, rgba(39, 174, 96, 0.05) 0%, rgba(46, 213, 115, 0.05) 100%);
}

.evo-title {
    font-size: 1.4em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 20px;
    padding: 10px;
    border-radius: 10px;
}

.traditional-agent .evo-title {
    background: rgba(231, 76, 60, 0.1);
    color: #c0392b;
}

.agentic-ai .evo-title {
    background: rgba(39, 174, 96, 0.1);
    color: #27ae60;
}

.evo-diagram {
    text-align: center;
    margin: 20px 0;
}

.single-agent-box {
    background: linear-gradient(135deg, #ff6b6b 0%, #ee5253 100%);
    color: white;
    padding: 20px;
    border-radius: 15px;
    margin: 0 auto;
    max-width: 200px;
    box-shadow: 0 6px 15px rgba(238, 82, 83, 0.3);
}

.agent-layer {
    padding: 8px;
    margin: 5px 0;
    background: rgba(255, 255, 255, 0.2);
    border-radius: 8px;
    font-weight: 600;
}

.multi-agent-structure {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}

.orchestrator-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 15px 25px;
    border-radius: 12px;
    font-weight: bold;
    box-shadow: 0 6px 15px rgba(102, 126, 234, 0.3);
}

.agent-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 12px;
    margin: 15px 0;
}

.specialist-agent {
    background: linear-gradient(135deg, #55efc4 0%, #00b894 100%);
    color: white;
    padding: 12px;
    border-radius: 10px;
    font-size: 0.85em;
    text-align: center;
    font-weight: 600;
    box-shadow: 0 4px 10px rgba(0, 184, 148, 0.3);
}

.shared-memory-box {
    background: linear-gradient(135deg, #fdcb6e 0%, #e67e22 100%);
    color: white;
    padding: 12px;
    border-radius: 10px;
    font-weight: 600;
    text-align: center;
    box-shadow: 0 4px 10px rgba(230, 126, 34, 0.3);
}

.evo-arrow {
    font-size: 3em;
    color: #667eea;
    animation: pulse-horizontal 2s ease-in-out infinite;
}

@keyframes pulse-horizontal {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.2); }
}

.evo-features {
    margin-top: 15px;
    padding: 15px;
    background: rgba(102, 126, 234, 0.05);
    border-radius: 10px;
}

.evo-features ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

.evo-features li {
    padding: 6px 0;
    padding-left: 20px;
    position: relative;
}

.evo-features li:before {
    content: "✓";
    position: absolute;
    left: 0;
    font-weight: bold;
}

.traditional-agent .evo-features li:before {
    color: #e74c3c;
}

.agentic-ai .evo-features li:before {
    color: #27ae60;
}

@media (max-width: 1024px) {
    .evolution-comparison {
        grid-template-columns: 1fr;
        gap: 20px;
    }
    
    .evo-arrow {
        transform: rotate(90deg);
    }
}

/* Enhancement Cards */
.enhancement-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
    margin: 30px 0;
}

.enhancement-card {
    background: white;
    border-radius: 20px;
    padding: 30px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.12);
    transition: all 0.3s ease;
    border: 3px solid transparent;
}

.enhancement-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.2);
}

.enhancement-1 {
    border-color: #9b59b6;
    background: linear-gradient(135deg, rgba(155, 89, 182, 0.05) 0%, rgba(142, 68, 173, 0.05) 100%);
}

.enhancement-2 {
    border-color: #3498db;
    background: linear-gradient(135deg, rgba(52, 152, 219, 0.05) 0%, rgba(41, 128, 185, 0.05) 100%);
}

.enhancement-3 {
    border-color: #e67e22;
    background: linear-gradient(135deg, rgba(230, 126, 34, 0.05) 0%, rgba(211, 84, 0, 0.05) 100%);
}

.enhancement-4 {
    border-color: #1abc9c;
    background: linear-gradient(135deg, rgba(26, 188, 156, 0.05) 0%, rgba(22, 160, 133, 0.05) 100%);
}

.enhancement-title {
    font-size: 1.3em;
    font-weight: bold;
    margin-bottom: 20px;
    padding: 12px;
    border-radius: 10px;
    text-align: center;
}

.enhancement-1 .enhancement-title {
    background: rgba(155, 89, 182, 0.15);
    color: #8e44ad;
}

.enhancement-2 .enhancement-title {
    background: rgba(52, 152, 219, 0.15);
    color: #2980b9;
}

.enhancement-3 .enhancement-title {
    background: rgba(230, 126, 34, 0.15);
    color: #d35400;
}

.enhancement-4 .enhancement-title {
    background: rgba(26, 188, 156, 0.15);
    color: #16a085;
}

.enhancement-content {
    font-size: 0.95em;
    line-height: 1.7;
}

.framework-box {
    background: rgba(102, 126, 234, 0.08);
    padding: 15px;
    border-radius: 10px;
    margin: 15px 0;
    border-left: 4px solid #667eea;
}

.framework-box h5 {
    color: #667eea;
    margin-bottom: 10px;
    font-size: 1.1em;
}

.code-flow {
    background: #2c3e50;
    color: #ecf0f1;
    padding: 15px;
    border-radius: 8px;
    font-family: 'Courier New', monospace;
    font-size: 0.85em;
    line-height: 1.8;
    margin: 10px 0;
    overflow-x: auto;
}

.memory-table {
    margin: 15px 0;
    width: 100%;
}

.memory-table table {
    font-size: 0.9em;
}

.analogy-box {
    background: rgba(52, 152, 219, 0.08);
    border: 2px dashed #3498db;
    padding: 15px;
    border-radius: 10px;
    margin: 15px 0;
}

.analogy-structure {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
    margin: 15px 0;
    text-align: center;
}

.role-box {
    background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
    color: white;
    padding: 10px;
    border-radius: 8px;
    font-size: 0.85em;
    font-weight: 600;
}

.ceo-box {
    grid-column: span 4;
    background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);
}

.dept-box {
    background: linear-gradient(135deg, #9b59b6 0%, #8e44ad 100%);
}

.example-highlight {
    background: rgba(39, 174, 96, 0.1);
    border-left: 4px solid #27ae60;
    padding: 12px;
    margin: 10px 0;
    border-radius: 6px;
}

@media (max-width: 1024px) {
    .enhancement-grid {
        grid-template-columns: 1fr;
    }
    
    .analogy-structure {
        grid-template-columns: repeat(2, 1fr);
    }
    
    .ceo-box {
        grid-column: span 2;
    }
}

@media (max-width: 768px) {
    .analogy-structure {
        grid-template-columns: 1fr;
    }
    
    .ceo-box {
        grid-column: span 1;
    }
}

/* Agent Comparison Styles */
.agent-comparison-container {
    margin: 30px 0;
}

.agent-comparison-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 25px;
    margin: 25px 0;
}

.agent-box {
    background: white;
    border-radius: 20px;
    padding: 25px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.12);
    transition: all 0.3s ease;
    border: 3px solid transparent;
    display: flex;
    flex-direction: column;
}

.agent-box:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 40px rgba(0,0,0,0.2);
}

.traditional-box {
    border-color: #e74c3c;
    background: linear-gradient(135deg, rgba(231, 76, 60, 0.05) 0%, rgba(192, 57, 43, 0.05) 100%);
}

.traditional-box:hover {
    border-color: #c0392b;
}

.llm-box {
    border-color: #27ae60;
    background: linear-gradient(135deg, rgba(39, 174, 96, 0.05) 0%, rgba(46, 213, 115, 0.05) 100%);
}

.llm-box:hover {
    border-color: #229954;
}

.agent-box-title {
    font-size: 1.3em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 15px;
    padding: 12px;
    border-radius: 10px;
}

.traditional-box .agent-box-title {
    background: rgba(231, 76, 60, 0.15);
    color: #c0392b;
}

.llm-box .agent-box-title {
    background: rgba(39, 174, 96, 0.15);
    color: #27ae60;
}

.agent-code {
    background: #2c3e50;
    color: #ecf0f1;
    padding: 15px;
    border-radius: 10px;
    font-family: 'Courier New', monospace;
    font-size: 0.8em;
    line-height: 1.6;
    margin: 15px 0;
    overflow-x: auto;
    flex-grow: 1;
}

.agent-code .keyword {
    color: #e74c3c;
}

.agent-code .string {
    color: #2ecc71;
}

.agent-code .function {
    color: #3498db;
}

.agent-code .comment {
    color: #95a5a6;
}

.agent-verdict {
    text-align: center;
    font-size: 1.1em;
    font-weight: bold;
    margin-top: 15px;
    padding: 10px;
    border-radius: 8px;
}

.traditional-box .agent-verdict {
    background: rgba(231, 76, 60, 0.1);
    color: #c0392b;
}

.llm-box .agent-verdict {
    background: rgba(39, 174, 96, 0.1);
    color: #27ae60;
}

@media (max-width: 1024px) {
    .agent-comparison-grid {
        grid-template-columns: 1fr;
    }
}

/* Pattern Cards */
.pattern-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 25px;
    margin: 30px 0;
}

.pattern-card {
    background: white;
    border-radius: 15px;
    padding: 25px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
    border: 3px solid transparent;
}

.pattern-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 30px rgba(0,0,0,0.18);
}

.pattern-1 {
    border-color: #9b59b6;
    background: linear-gradient(135deg, rgba(155, 89, 182, 0.05) 0%, rgba(142, 68, 173, 0.05) 100%);
}

.pattern-2 {
    border-color: #3498db;
    background: linear-gradient(135deg, rgba(52, 152, 219, 0.05) 0%, rgba(41, 128, 185, 0.05) 100%);
}

.pattern-3 {
    border-color: #e67e22;
    background: linear-gradient(135deg, rgba(230, 126, 34, 0.05) 0%, rgba(211, 84, 0, 0.05) 100%);
}

.pattern-4 {
    border-color: #1abc9c;
    background: linear-gradient(135deg, rgba(26, 188, 156, 0.05) 0%, rgba(22, 160, 133, 0.05) 100%);
}

.pattern-title {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: 15px;
    padding: 10px;
    border-radius: 8px;
    text-align: center;
}

.pattern-1 .pattern-title {
    background: rgba(155, 89, 182, 0.15);
    color: #8e44ad;
}

.pattern-2 .pattern-title {
    background: rgba(52, 152, 219, 0.15);
    color: #2980b9;
}

.pattern-3 .pattern-title {
    background: rgba(230, 126, 34, 0.15);
    color: #d35400;
}

.pattern-4 .pattern-title {
    background: rgba(26, 188, 156, 0.15);
    color: #16a085;
}

.pattern-flow {
    background: #f8f9fa;
    padding: 15px;
    border-radius: 8px;
    margin: 15px 0;
    font-family: 'Courier New', monospace;
    font-size: 0.9em;
    line-height: 1.8;
    border-left: 4px solid;
}

.pattern-1 .pattern-flow {
    border-left-color: #9b59b6;
}

.pattern-2 .pattern-flow {
    border-left-color: #3498db;
}

.pattern-3 .pattern-flow {
    border-left-color: #e67e22;
}

.pattern-4 .pattern-flow {
    border-left-color: #1abc9c;
}

.pattern-example {
    background: rgba(102, 126, 234, 0.05);
    padding: 12px;
    border-radius: 6px;
    margin-top: 10px;
    font-size: 0.9em;
    line-height: 1.6;
}

@media (max-width: 1024px) {
    .pattern-grid {
        grid-template-columns: 1fr;
    }
}

/* Quiz Styles */
.quiz-container {
    margin: 30px 0;
}

.quiz-question {
    background: white;
    border-left: 5px solid #667eea;
    padding: 25px;
    margin: 20px 0;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
}

.quiz-question:hover {
    box-shadow: 0 6px 20px rgba(0,0,0,0.12);
    transform: translateX(5px);
}

.component-header {
    text-align: center;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 30px;
    border-radius: 15px;
    margin: 30px 0;
    font-size: 1.5em;
    font-weight: bold;
    box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
    animation: pulse 2s infinite;
}

.component-stack {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    margin: 40px auto;
    max-width: 100%;
}

.component-card {
    background: white;
    border-radius: 15px;
    padding: 20px;
    box-shadow: 0 8px 20px rgba(0,0,0,0.12);
    transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    cursor: pointer;
    border: 3px solid transparent;
    height: 100%;
    display: flex;
    flex-direction: column;
}

.component-card:hover {
    transform: translateY(-8px) scale(1.03);
    box-shadow: 0 15px 35px rgba(0,0,0,0.2);
}

.comp-perception {
    border-color: #a29bfe;
    background: linear-gradient(135deg, rgba(162, 155, 254, 0.05) 0%, rgba(116, 103, 239, 0.05) 100%);
}

.comp-perception:hover {
    border-color: #7467ef;
    background: linear-gradient(135deg, rgba(162, 155, 254, 0.15) 0%, rgba(116, 103, 239, 0.15) 100%);
}

.comp-reasoning {
    border-color: #74b9ff;
    background: linear-gradient(135deg, rgba(116, 185, 255, 0.05) 0%, rgba(9, 132, 227, 0.05) 100%);
}

.comp-reasoning:hover {
    border-color: #0984e3;
    background: linear-gradient(135deg, rgba(116, 185, 255, 0.15) 0%, rgba(9, 132, 227, 0.15) 100%);
}

.comp-action {
    border-color: #55efc4;
    background: linear-gradient(135deg, rgba(85, 239, 196, 0.05) 0%, rgba(0, 184, 148, 0.05) 100%);
}

.comp-action:hover {
    border-color: #00b894;
    background: linear-gradient(135deg, rgba(85, 239, 196, 0.15) 0%, rgba(0, 184, 148, 0.15) 100%);
}

.comp-learning {
    border-color: #fdcb6e;
    background: linear-gradient(135deg, rgba(253, 203, 110, 0.05) 0%, rgba(230, 126, 34, 0.05) 100%);
}

.comp-learning:hover {
    border-color: #e67e22;
    background: linear-gradient(135deg, rgba(253, 203, 110, 0.15) 0%, rgba(230, 126, 34, 0.15) 100%);
}

.comp-icon {
    font-size: 2.5em;
    text-align: center;
    margin-bottom: 10px;
    animation: bounce 2s ease-in-out infinite;
}

.comp-title {
    font-size: 1.1em;
    font-weight: bold;
    text-align: center;
    margin-bottom: 12px;
    color: #2c3e50;
    min-height: 2.5em;
}

.comp-description {
    background: rgba(102, 126, 234, 0.1);
    padding: 8px 10px;
    border-radius: 8px;
    margin: 10px 0;
    font-weight: 600;
    color: #667eea;
    text-align: center;
    font-size: 0.85em;
}

.comp-features {
    list-style: none;
    padding: 0;
    margin: 10px 0;
    font-size: 0.8em;
    flex-grow: 1;
}

.comp-feature {
    background: rgba(255, 255, 255, 0.8);
    padding: 6px 10px;
    margin: 4px 0;
    border-radius: 6px;
    border-left: 3px solid #667eea;
}

.comp-note {
    background: linear-gradient(135deg, #fff5e6 0%, #ffe6cc 100%);
    padding: 8px 12px;
    border-radius: 8px;
    margin-top: 10px;
    font-style: italic;
    color: #e67e22;
    font-weight: 600;
    font-size: 0.75em;
}

.component-connector {
    display: none;
}

@media (max-width: 1024px) {
    .component-stack {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 768px) {
    .component-stack {
        grid-template-columns: 1fr;
    }
}

.interaction-container {
    margin: 30px 0;
}

.interaction-step {
    background: white;
    border-radius: 15px;
    padding: 25px;
    margin: 20px 0;
    box-shadow: 0 8px 20px rgba(0,0,0,0.12);
    transition: all 0.3s ease;
    border-left: 5px solid #667eea;
}

.interaction-step:hover {
    transform: translateX(5px);
    box-shadow: 0 10px 25px rgba(0,0,0,0.18);
}

.step-perception {
    border-left-color: #a29bfe;
    background: linear-gradient(135deg, rgba(162, 155, 254, 0.03) 0%, rgba(116, 103, 239, 0.03) 100%);
}

.step-reasoning {
    border-left-color: #74b9ff;
    background: linear-gradient(135deg, rgba(116, 185, 255, 0.03) 0%, rgba(9, 132, 227, 0.03) 100%);
}

.step-action {
    border-left-color: #55efc4;
    background: linear-gradient(135deg, rgba(85, 239, 196, 0.03) 0%, rgba(0, 184, 148, 0.03) 100%);
}

.step-learning {
    border-left-color: #fdcb6e;
    background: linear-gradient(135deg, rgba(253, 203, 110, 0.03) 0%, rgba(230, 126, 34, 0.03) 100%);
}

.step-title {
    font-size: 1.4em;
    font-weight: bold;
    color: #2c3e50;
    margin-bottom: 15px;
    display: flex;
    align-items: center;
    gap: 10px;
}

.step-content {
    background: rgba(248, 249, 250, 0.8);
    padding: 15px;
    border-radius: 10px;
    font-family: 'Courier New', monospace;
    font-size: 0.9em;
    line-height: 1.6;
    color: #2c3e50;
}
@end

-->

# Module 1: Technical Foundations
> **Building Blocks of AI Agents**
>
> *Understanding Architecture, Components & Operational Principles*
> 
> Duration: 75 minutes | Interactive Workshop Format

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

- [X] Define AI Agents and distinguish them from traditional automation
- [X] Explain the Perceive-Reason-Act cycle and its importance
- [X] Identify the three core characteristics of AI agents
- [X] Understand the three-layer software architecture
- [X] Compare AI Agents vs Agentic AI paradigms
- [X] Recognize the role of LLMs in modern agent systems
- [X] Apply architectural knowledge to real-world scenarios

---

## 📊 Workshop Roadmap

<div class="roadmap-container">

<div class="roadmap-tile">

### 🎯 Part 1: FUNDAMENTALS <span class="time"> 25 min</span>

- 🤖 What are AI Agents? 
- 🔄 The Perceive-Reason-Act Cycle 
- 🎯 Three Core Characteristics 

</div>

<div class="roadmap-tile">

### 🏗️ Part 2: ARCHITECTURE <span class="time"> 25 min</span>

- 🏗️ Three-Layer Software Stack 

- 🧩 Core Architectural Components 

- 🔬 Four Technological Paradigms

</div>

<div class="roadmap-tile">

### 🚀 Part 3: PROGRESSION <span class="time"> 25 min</span>

- 🚀 From AI Agents to Agentic AI 
- 🧠 Role of LLMs as Reasoning Engines 
- 💡 Interactive Architecture Design Challenge

</div>

</div>

---

## Part 1: Fundamentals

### What are AI Agents? 🤖

<div class="definition-box">

**AI Agents** are **autonomous software entities engineered for goal-directed task execution within bounded digital environments**.

**Key Definition Elements:**

- 🎯 **Goal-Directed**: Operate toward specific objectives
- 🤖 **Autonomous**: Function with minimal human intervention
- 🔧 **Software Entities**: Digital systems, not necessarily embodied
- 🌐 **Bounded Environments**: Operate within defined constraints

</div>

#### What Makes Them Special?

AI Agents differ fundamentally from traditional software:

| **Traditional Software** | **AI Agents** |
|--------------------------|---------------|
| Follows fixed rules | Adapts to context |
| Deterministic execution | Probabilistic reasoning |
| Manual updates required | Self-adjusting behavior |
| Static workflows | Dynamic decision-making |
| No learning capability | Can improve over time |

<div class="key-point">
💡 Critical Distinction:

**Unlike conventional automation scripts that follow deterministic workflows, AI agents demonstrate _"reactive intelligence"_ and _"adaptability"_, allowing them to interpret dynamic inputs and reconfigure outputs accordingly.**

</div>

---

### The Perceive-Reason-Act Cycle 🔄

Every AI agent operates through a continuous feedback loop:

<div class="cycle-diagram">

<div class="cycle-box">
<h4><span class="emoji">🌍</span> ENVIRONMENT & CONTEXT</h4>
<p>External world: users, systems, APIs, data sources, sensors, interfaces</p>
</div>

<div class="arrow">↓</div>
<div class="cycle-label">Signals, Data, Events</div>

<div class="cycle-box">
<h4><span class="emoji">📥</span> 1️⃣ PERCEIVE - Input Processing</h4>
<div class="content-list">
<div class="content-item">• Sensors</div>
<div class="content-item">• APIs</div>
<div class="content-item">• User Input</div>
<div class="content-item">• Data Streams</div>
<div class="content-item">• Gather data from environment</div>
<div class="content-item">• Receive user inputs</div>
<div class="content-item">• Monitor system states</div>
<div class="content-item">• Parse structured/unstructured data</div>
<div class="content-item">• Contextualize information</div>
</div>
</div>

<div class="arrow">↓</div>
<div class="cycle-label">Processed Information</div>

<div class="cycle-box">
<h4><span class="emoji">🧠</span> 2️⃣ REASON - Cognitive Processing</h4>
<div class="content-list">
<div class="content-item">• Context Analysis</div>
<div class="content-item">• Planning</div>
<div class="content-item">• Decision-Making</div>
<div class="content-item">• Learning</div>
<div class="content-item">• Analyze context</div>
<div class="content-item">• Identify patterns</div>
<div class="content-item">• Evaluate options</div>
<div class="content-item">• Make informed decisions</div>
<div class="content-item">• Plan action sequences</div>
<div class="content-item">• Apply domain knowledge</div>
</div>
</div>

<div class="arrow">↓</div>
<div class="cycle-label">Action Plan</div>

<div class="cycle-box">
<h4><span class="emoji">⚡</span> 3️⃣ ACT - Execution Phase</h4>
<div class="content-list">
<div class="content-item">• Tool Use</div>
<div class="content-item">• API Calls</div>
<div class="content-item">• Database Operations</div>
<div class="content-item">• Generate Output</div>
<div class="content-item">• Execute decisions</div>
<div class="content-item">• Invoke external tools</div>
<div class="content-item">• Generate outputs</div>
<div class="content-item">• Update system states</div>
<div class="content-item">• Communicate results</div>
<div class="content-item">• Trigger workflows</div>
</div>
</div>

<div class="arrow">↓</div>
<div class="cycle-label">Actions, Changes, Results</div>

<div class="cycle-box">
<h4><span class="emoji">🔄</span> ENVIRONMENT & CONTEXT</h4>
<p>Effects propagate back - State changes observed</p>
</div>

<div class="feedback-arrow">🔁</div>

<div class="cycle-box">
<h4><span class="emoji">📊</span> FEEDBACK LOOP</h4>
<p><strong>Continuous Learning & Adaptation</strong></p>
<p>Agent improves through experience and observation</p>
</div>

</div>

#### Detailed Breakdown:

{{1}}
<div class="cycle-step">

#### <span class="step-icon">📥</span> STEP 1: PERCEIVE Phase

<span class="step-label">Input Processing</span>

**What:** Data ingestion and preprocessing

**How it works:**
- Gather data from environment through sensors, APIs, user interfaces
- Receive and parse user inputs
- Monitor system states and data streams
- Parse structured/unstructured data
- Contextualize information for reasoning

**Output:** Structured, contextualized information ready for analysis

**Example:** Customer service bot reads email content, analyzes sentiment, extracts key entities (product ID, issue type, customer history)

</div>

{{2}}
<div class="cycle-step">

#### <span class="step-icon">🧠</span> STEP 2: REASON Phase

<span class="step-label">Cognitive Processing</span>

**What:** Analysis, planning, and decision-making

**How it works:**
- Analyze context using LLMs, rule engines, knowledge graphs
- Identify patterns and evaluate options
- Make informed decisions based on available data
- Plan action sequences with prioritization
- Apply domain knowledge and reasoning

**Output:** Action plan with prioritized steps

**Example:** Bot determines this is a billing issue, checks refund policy, calculates resolution options, selects optimal response

</div>

{{3}}
<div class="cycle-step">

#### <span class="step-icon">⚡</span> STEP 3: ACT Phase

<span class="step-label">Execution Phase</span>

**What:** Execution of decisions

**How it works:**
- Invoke external tools and APIs
- Execute database operations
- Generate outputs and messages
- Update system states
- Communicate results to users/systems
- Trigger downstream workflows

**Output:** Observable changes in environment

**Example:** Bot initiates refund, updates customer record, sends confirmation email, logs interaction

</div>

{{4}}
<div class="cycle-step">

#### <span class="step-icon">🔄</span> FEEDBACK LOOP

<span class="step-label">Continuous Adaptation</span>

**What:** Learning and improvement mechanism

**How it works:**
- Observe effects of actions in environment
- Collect feedback from users and systems
- Update internal models and preferences
- Refine decision-making strategies
- Adapt behavior based on outcomes

**Result:** Agent becomes more effective over time through experience

**Example:** If user corrects bot's suggestion, the system learns the preferred response pattern for similar future cases

</div>

---

#### 🎮 Interactive Exercise 1: Identify the Phases

For each scenario, identify which phase (Perceive, Reason, or Act) is being described:

[[Perceive] [Reason] [Act]]
[   ( )      ( )      (X)   ] A coding assistant inserts a code snippet into your editor. **Hint:** Is the agent gathering data, analyzing, or executing an action?
[   (X)      ( )      ( )   ] A medical diagnosis agent reads patient lab results. **Hint:** What is the first step - collecting information, analyzing it, or taking action?
[   ( )      (X)      ( )   ] A supply chain optimizer calculates optimal delivery routes. **Hint:** Is this processing input, performing analysis, or executing a task?
[   ( )      ( )      (X)   ] An email agent drafts and sends a meeting confirmation. **Hint:** Is the agent gathering data, making decisions, or performing an output action?
[   (X)      ( )      ( )   ] A content moderation bot scans uploaded images **Hint:** What's happening - data collection, decision-making, or action execution?
[   ( )      (X)      ( )   ] A trading algorithm evaluates market conditions  **Hint:** Think about the cognitive process - is it input, analysis, or output?
***
<div class="key-point">



</div>

***

<details>
<summary>✅ **Correct Answer - Click to Reveal**</summary>

<div class="key-point" style="font-size: 0.95em;">

**Answers & Explanations:**

1. Act - **The assistant is executing an action (inserting code) into your environment. This is the final execution phase.**

2. Perceive - **Reading lab results is data gathering/input processing - the first phase where the agent collects information.**

3. Reason - **Calculating routes involves analysis, planning, and decision-making based on data - this is cognitive processing.**

4. Act - **Drafting and sending emails are execution actions that produce output and change the environment.**

5. Perceive - **Scanning images is input processing where the agent gathers visual data from the environment.**

6. Reason - **Evaluating market conditions is analysis and decision-making - processing information to determine next steps.**

Key Insight: **Most agents cycle through these phases multiple times in a single task. A supply chain optimizer might perceive current inventory (P), reason about reorder timing (R), act by placing orders (A), then perceive delivery confirmations (P) to start the cycle again.**

</div>

</details>

***

### Three Core Characteristics 🎯

<div class="characteristics-header">
✨ THREE PILLARS OF AI AGENT DESIGN ✨
</div>

{{1}}
<div class="char-card char-autonomy">

<div class="char-icon">🤖</div>
<div class="char-title">1️⃣ AUTONOMY</div>

<div class="char-definition">
<strong>Definition:</strong> Ability to function with minimal human intervention after deployment.
</div>

**Levels of Autonomy:**

<div class="autonomy-levels">

<div class="level-box level-low">
<h4>🟡 LOW</h4>
<p><strong>Constant human input</strong></p>
<p>Ex: Autocomplete</p>
</div>

<div class="level-box level-medium">
<h4>🔵 MEDIUM</h4>
<p><strong>Independent with oversight</strong></p>
<p>Ex: Email filtering</p>
</div>

<div class="level-box level-high">
<h4>🟢 HIGH</h4>
<p><strong>Fully autonomous</strong></p>
<p>Ex: Self-driving car</p>
</div>

</div>

**Business Impact:**
- ✅ 24/7 operation • ✅ Scales efficiently
- ⚠️ Requires testing • ⚠️ Needs governance

</div>

{{2}}
<div class="char-card char-task">

<div class="char-icon">🎯</div>
<div class="char-title">2️⃣ TASK-SPECIFICITY</div>

<div class="char-definition">
<strong>Definition:</strong> Purpose-built for narrow, well-defined tasks within bounded domains.
</div>

**Why It Matters:** Efficiency • Reliability • Explainability • Compliance

**Spectrum of Specificity:**

| Type | Scope | Example | Flexibility |
|------|-------|---------|-------------|
| **Specialist** | Single task | Tax calculation | Very Low |
| **Domain Expert** | Related tasks | HR automation | Low-Med |
| **Generalist** | Multiple domains | Personal AI | Med-High |
| **Universal** | Open-ended | AGI (theory) | Very High |

<div class="key-point" style="font-size: 0.9em; padding: 12px;">
💡 **Current Reality:** Nearly all production agents are specialists or domain experts.
</div>

</div>

{{3}}
<div class="char-card char-reactive">

<div class="char-icon">⚡</div>
<div class="char-title">3️⃣ REACTIVITY & ADAPTATION</div>

<div class="char-definition">
<strong>Definition:</strong> Ability to respond to dynamic inputs and adjust behavior accordingly.
</div>

**Two Dimensions:**

**A) Reactivity** - Real-time responsiveness

```ascii
User Input → [Agent] → Response
     ↑                     ↓
     └───── Feedback ──────┘
```

**B) Adaptation** - Learning from experience

```ascii
Experience → Learning → Behavior Change
    ↑                          ↓
    └──── Feedback Loop ───────┘
```

**Mechanisms:**
- 🔄 Context Buffers • 📊 Feedback Loops
- 🎯 Heuristic Adjustment • 🧠 Model Fine-Tuning

</div>

---

#### 🎮 Interactive Exercise 2: Characteristic Analysis


<div style="
  background-color: rgba(30, 144, 255, 0.12);
  border-left: 6px solid #1e90ff;
  padding: 16px 20px;
  margin: 18px 0;
  font-size: 1.4em;
  font-weight: 700;
">
Scenario 1: Email Spam Filter
</div>


[[Low] [Medium] [High]]
[( )   (X)      ( )  ] **Autonomy Level**
[[High - Single Task] [Medium] [Low - Generalist]]
[(X)                  ( )      ( )              ] **Task Specificity**
[[Learning from user corrections] [Static rules] [No adaptation]]
[(X)                              ( )            ( )             ] **Reactivity**

---

<div style="
  background-color: rgba(30, 144, 255, 0.12);
  border-left: 6px solid #1e90ff;
  padding: 16px 20px;
  margin: 18px 0;
  font-size: 1.4em;
  font-weight: 700;
">
Scenario 2: Autonomous Warehouse Robot
</div>


[[Low] [Medium] [High - Minimal supervision]]
[( )   ( )      (X)                         ] **Autonomy Level**
[[High - Item retrieval/transport] [Medium] [Low]]
[(X)                               ( )      ( ) ] **Task Specificity**
[[Responds to obstacles, new items] [Static paths] [No adjustment]]
[(X)                                ( )            ( )            ] **Reactivity**

---
<div style="
  background-color: rgba(30, 144, 255, 0.12);
  border-left: 6px solid #1e90ff;
  padding: 16px 20px;
  margin: 18px 0;
  font-size: 1.4em;
  font-weight: 700;
">
Scenario 3: Meeting Scheduling Assistant
</div>


[[Low] [Medium - Confirms before booking] [High]]
[( )   (X)                               ( )   ] **Autonomy Level**
[[High - Calendar management] [Medium] [Low]]
[(X)                          ( )      ( ) ] **Task Specificity**
[[Learns preferences, adapts to conflicts] [Fixed rules] [No learning]]
[(X)                                       ( )           ( )         ] **Reactivity**

---

## Part 2: Architecture

### Three-Layer Software Architecture 🏗️

<div class="architecture-header">
🏗️ THREE-LAYER AI AGENT ARCHITECTURE
</div>

<div class="layer-stack">

{{1}}
<div class="layer-card layer-app">

<div class="layer-icon">🎨</div>
<div class="layer-title">APPLICATION LAYER</div>
<div class="layer-purpose">User-facing interfaces and system integrations</div>

<div class="layer-features">
<div class="feature-item">📱 UIs (Web/Mobile/Voice)</div>
<div class="feature-item">🔌 REST/GraphQL APIs</div>
<div class="feature-item">🔐 Auth & Sessions</div>
<div class="feature-item">⚡ Rate Limiting</div>
<div class="feature-item">📊 Input Translation</div>
<div class="feature-item">✨ Output Formatting</div>
</div>

<p style="font-size: 0.85em; margin-top: 10px;"><strong>Example:</strong> "Cancel subscription" → Auth user → Extract intent → Route workflow → Return response</p>

</div>

<div class="layer-connector">↓</div>

{{2}}
<div class="layer-card layer-orch">

<div class="layer-icon">🎭</div>
<div class="layer-title">ORCHESTRATION LAYER</div>
<div class="layer-purpose">Workflow coordination, memory & tool management</div>

<div class="layer-features">
<div class="feature-item">🧩 Task Decomposition</div>
<div class="feature-item">🧠 Memory (Short/Long-term)</div>
<div class="feature-item">🔧 Tool Library Mgmt</div>
<div class="feature-item">🔄 Multi-Agent Coord.</div>
<div class="feature-item">⚠️ Error Handling</div>
<div class="feature-item">📡 Protocols (MCP, A2A)</div>
</div>

<p style="font-size: 0.85em; margin-top: 10px;"><strong>Example:</strong> "Summarize AI research" → Plans: [Search → Filter → Summarize] → Recalls prefs → Invokes tools</p>

</div>

<div class="layer-connector">↓</div>

{{3}}
<div class="layer-card layer-reason">

<div class="layer-icon">🧠</div>
<div class="layer-title">REASONING LAYER</div>
<div class="layer-purpose">AI models for decision-making & problem-solving</div>

<div class="layer-features">
<div class="feature-item">🤖 LLMs (GPT-4, Claude)</div>
<div class="feature-item">👁️ Computer Vision</div>
<div class="feature-item">📈 Predictive Models</div>
<div class="feature-item">⚙️ Rule Engines</div>
<div class="feature-item">🔍 Knowledge Graphs</div>
<div class="feature-item">🎯 Optimization Algos</div>
</div>

<p style="font-size: 0.85em; margin-top: 10px;"><strong>Example:</strong> "Red dresses <$100" → LLM extracts intent → KG queries DB → Model ranks → LLM responds</p>

</div>

</div>

---

### Core Architectural Components 🧩

<div class="component-header">
🧩 FOUR-COMPONENT ARCHITECTURAL MODEL
</div>

<p style="text-align: center; font-style: italic; color: #667eea; margin: 20px 0;">

</p>

<div class="component-stack">

<div class="component-card comp-perception">
<div class="comp-icon">📥</div>
<div class="comp-title">1️⃣ PERCEPTION</div>
<div class="comp-description">Input Processing</div>
<ul class="comp-features">
<li class="comp-feature">📝 Natural language</li>
<li class="comp-feature">🌐 API streams</li>
<li class="comp-feature">📄 File uploads</li>
<li class="comp-feature">🤖 Sensor data</li>
<li class="comp-feature">🗄️ Database queries</li>
<li class="comp-feature">🧹 Data cleaning</li>
<li class="comp-feature">🔄 Format conversion</li>
<li class="comp-feature">🏷️ Entity extraction</li>
</ul>
</div>

<div class="component-card comp-reasoning">
<div class="comp-icon">🧠</div>
<div class="comp-title">2️⃣ REASONING (KRR)</div>
<div class="comp-description">Cognitive Processing</div>
<ul class="comp-features">
<li class="comp-feature">🌲 Rule-based logic</li>
<li class="comp-feature">📊 Planning graphs</li>
<li class="comp-feature">⚡ Function calling</li>
<li class="comp-feature">🔗 Prompt chaining</li>
<li class="comp-feature">💭 Chain-of-Thought</li>
<li class="comp-feature">🎯 ReAct framework</li>
<li class="comp-feature">🛠️ Tool decision logic</li>
</ul>
</div>

<div class="component-card comp-action">
<div class="comp-icon">⚡</div>
<div class="comp-title">3️⃣ ACTION</div>
<div class="comp-description">Execution Phase</div>
<ul class="comp-features">
<li class="comp-feature">📧 Send messages</li>
<li class="comp-feature">💾 Update databases</li>
<li class="comp-feature">🌐 Query APIs</li>
<li class="comp-feature">📝 Generate outputs</li>
<li class="comp-feature">🔄 Trigger workflows</li>
<li class="comp-feature">🤖 Agent executor</li>
<li class="comp-feature">🔧 Tool middleware</li>
<li class="comp-feature">👁️ Response observation</li>
</ul>
</div>

<div class="component-card comp-learning">
<div class="comp-icon">📚</div>
<div class="comp-title">4️⃣ LEARNING</div>
<div class="comp-description">Adaptation</div>
<ul class="comp-features">
<li class="comp-feature">⚙️ Parameter tuning</li>
<li class="comp-feature">🕒 Context retention</li>
<li class="comp-feature">💭 Memory buffers</li>
<li class="comp-feature">📊 Tool scoring</li>
<li class="comp-feature">🔄 Feedback loops</li>
<li class="comp-feature">🎯 Preference learning</li>
</ul>
<div class="comp-note">
⚠️ Limited in traditional AI agents
</div>
</div>

</div>

#### Component Interaction Example: Email Assistant

Let's trace a request through all four components:

**User Request:** "Draft a professional email declining a meeting invitation for tomorrow due to conflict"

<div class="interaction-container">

{{1}}
<div class="interaction-step step-perception">
<div class="step-title">📥 1️⃣ PERCEPTION</div>
<div class="step-content">
Input: Natural language text
↓
Processing:
• Parse: user wants to decline meeting
• Extract: meeting_date = tomorrow
• Extract: reason = schedule conflict
• Extract: tone_requirement = professional
↓
Output: Structured request object
{
  action: "draft_email",
  purpose: "decline_meeting",
  constraints: {date: "tomorrow", tone: "professional", reason: "conflict"}
}
</div>
</div>

{{2}}
<div class="interaction-step step-reasoning">
<div class="step-title">🧠 2️⃣ REASONING</div>
<div class="step-content">
Input: Structured request
↓
Reasoning Chain:
1. Recall user's email signature from memory
2. Check calendar for meeting details
3. Determine appropriate apology level
4. Select email template type
5. Plan content structure: [greeting] [decline] [reason] [apology] [alternative] [closing]
↓
Output: Email generation plan with parameters
</div>
</div>

{{3}}
<div class="interaction-step step-action">
<div class="step-title">⚡ 3️⃣ ACTION</div>
<div class="step-content">
Input: Generation plan
↓
Execution:
1. Invoke calendar_api.get_meeting("tomorrow")
2. Call llm.generate_email(template="decline", params={...})
3. Format output with user signature
4. (Optional) Send via email_api.send() or present to user
↓
Output: Formatted email in draft state
</div>
</div>

{{4}}
<div class="interaction-step step-learning">
<div class="step-title">📚 4️⃣ LEARNING</div>
<div class="step-content">
Input: User interaction with draft
↓
Observation:
• User edits: Changed "unfortunately" to "regrettably"
• User keeps: Overall structure and reasoning
↓
Adaptation:
• Update tone preference: user prefers "regrettably"
• Reinforce: Current decline email structure is good
• Store: User typically offers alternatives when declining
↓
Output: Updated user preference model
</div>
</div>

</div>

---

### Four Technological Paradigms 🔬

<div class="comparison-grid">

<div class="paradigm-card">
<h4>💻 1. Classical Software</h4>

**Characteristics:**
<ul>
<li>• Deterministic logic</li>
<li>• Rule-based execution</li>
<li>• Predictable outcomes</li>
</ul>

**In AI Agents:**
<ul>
<li>• Input validation</li>
<li>• Error handling</li>
<li>• State management</li>
</ul>

**Example:**
```python
if tier == "premium":
    allow_access()
else:
    show_upgrade()
```
</div>

<div class="paradigm-card">
<h4>🧠 2. Neural Networks</h4>

**Characteristics:**
<ul>
<li>• Pattern recognition</li>
<li>• Statistical learning</li>
<li>• Probabilistic outputs</li>
</ul>

**In AI Agents:**
<ul>
<li>• Image classification</li>
<li>• Anomaly detection</li>
<li>• Sentiment analysis</li>
</ul>

**Example:**
Computer vision identifies products in images for inventory
</div>

<div class="paradigm-card">
<h4>🤖 3. Foundation Models</h4>

**Characteristics:**
<ul>
<li>• General-purpose reasoning</li>
<li>• NL understanding</li>
<li>• Few-shot learning</li>
</ul>

**In AI Agents:**
<ul>
<li>• Intent understanding</li>
<li>• Response generation</li>
<li>• Task decomposition</li>
</ul>

**Example:**
GPT-4 interprets ambiguous requests and generates action plans
</div>

<div class="paradigm-card">
<h4>🤖 4. Autonomous Control</h4>

**Characteristics:**
<ul>
<li>• Self-planning</li>
<li>• Minimal oversight</li>
<li>• Real-time decisions</li>
</ul>

**In AI Agents:**
<ul>
<li>• Robotic navigation</li>
<li>• Autonomous vehicles</li>
<li>• Adaptive game AI</li>
</ul>

**Example:**
Warehouse robot plans optimal path while avoiding obstacles
</div>

</div>

<div class="key-point">

💡 Critical Insight: **Modern AI agents are hybrid systems that combine all four paradigms. A customer service bot might use:**

- **Classical software for authentication**
- **Neural networks for sentiment analysis**
- **LLMs for response generation**
- **Autonomous control for conversation flow management**

</div>

---

## Part 3: Evolution & Practice

### From AI Agents to Agentic AI 🚀

<div class="evolution-container">

<div class="evolution-header">
📈 ARCHITECTURAL EVOLUTION: From Single Agents to Multi-Agent Systems
</div>


<div class="evolution-comparison">

<div class="evolution-side traditional-agent">
<div class="evo-title">🔴 TRADITIONAL AI AGENT<br/>(Single Entity)</div>

<div class="evo-diagram">
<div class="single-agent-box">
<div class="agent-layer">👁️ Perception</div>
<div style="text-align: center; font-size: 1.5em; margin: 5px 0;">↓</div>
<div class="agent-layer">🧠 Reasoning</div>
<div style="text-align: center; font-size: 1.5em; margin: 5px 0;">↓</div>
<div class="agent-layer">⚡ Action</div>
</div>
</div>

<div class="evo-features">
<ul>
<li>Single task loop</li>
<li>No inter-agent communication</li>
<li>Limited to predefined capabilities</li>
<li>Monolithic architecture</li>
</ul>
</div>
</div>

<div class="evo-arrow">→</div>

<div class="evolution-side agentic-ai">
<div class="evo-title">🟢 AGENTIC AI<br/>(Multi-Agent System)</div>

<div class="evo-diagram">
<div class="multi-agent-structure">
<div class="orchestrator-box">🎯 ORCHESTRATOR (Meta-Agent)</div>
<div style="font-size: 1.5em; color: #667eea;">↓</div>
<div class="agent-grid">
<div class="specialist-agent">🔧 Agent A<br/><small>Task 1</small></div>
<div class="specialist-agent">🔬 Agent B<br/><small>Task 2</small></div>
<div class="specialist-agent">📊 Agent C<br/><small>Task 3</small></div>
<div class="specialist-agent">🎨 Agent D<br/><small>Task 4</small></div>
</div>
<div style="font-size: 1.5em; color: #667eea;">↓</div>
<div class="shared-memory-box">💾 SHARED MEMORY & CONTEXT</div>
</div>
</div>

<div class="evo-features">
<ul>
<li>Multi-agent collaboration</li>
<li>Distributed intelligence</li>
<li>Specialized task execution</li>
<li>Scalable & modular</li>
</ul>
</div>
</div>

</div>

</div>

---

#### Key Enhancements in Agentic AI


<div class="enhancement-grid">

<div class="enhancement-card enhancement-1">
<div class="enhancement-title">1️⃣ Ensemble of Specialized Agents</div>

<div class="enhancement-content">
<p><strong>Concept:</strong> Instead of one monolithic agent, Agentic AI uses multiple specialized agents working together.</p>

<div class="analogy-box">
<strong>💼 Corporate Structure Analogy:</strong>
<div class="analogy-structure">
<div class="role-box ceo-box">👔 CEO (Orchestrator)</div>
<div class="role-box dept-box">💻 CTO<br/><small>Technical</small></div>
<div class="role-box dept-box">💰 CFO<br/><small>Financial</small></div>
<div class="role-box dept-box">📱 CMO<br/><small>Marketing</small></div>
<div class="role-box dept-box">⚙️ COO<br/><small>Operations</small></div>
</div>
<p style="margin-top: 10px; font-size: 0.9em;"><em>Each "department" = Specialized agent with role-bound behavior, modular & reusable</em></p>
</div>

<div class="example-highlight">
<strong>🎯 Example - MetaGPT:</strong>
<ul style="margin: 8px 0; padding-left: 20px; font-size: 0.9em;">
<li><strong>CEO Agent:</strong> Breaks down project requirements</li>
<li><strong>CTO Agent:</strong> Designs technical architecture</li>
<li><strong>Engineer Agents:</strong> Write specific code modules</li>
<li><strong>QA Agent:</strong> Tests and validates outputs</li>
</ul>
</div>
</div>
</div>

<div class="enhancement-card enhancement-2">
<div class="enhancement-title">2️⃣ Advanced Reasoning & Planning</div>

<div class="enhancement-content">
<p><strong>Iterative reasoning frameworks enable complex problem-solving:</strong></p>

<div class="framework-box">
<h5>🔄 ReAct Framework</h5>
<div class="code-flow">
Thought → Action → Observation → Thought → Action → ...

<strong>Example:</strong>
Thought: "I need to find papers on AI safety"
Action: web_search("AI safety research 2024")
Observation: Found 10 results, mostly ArXiv
Thought: "Filter for peer-reviewed only"
Action: filter_results(source="peer_reviewed")
Observation: 5 papers remain
Thought: "Summarize key findings"
Action: summarize(papers, focus="safety")
</div>
</div>

<div class="framework-box">
<h5>🧮 Chain-of-Thought (CoT)</h5>
<div class="code-flow">
<strong>Problem:</strong> Calculate 15% tip on $47.80 meal

Step 1: Convert 15% → 0.15
Step 2: $47.80 × 0.15
Step 3: = $7.17
Step 4: Round → $7.00 or $7.20

<strong>Answer:</strong> Tip ≈ $7
</div>
</div>
</div>
</div>

<div class="enhancement-card enhancement-3">
<div class="enhancement-title">3️⃣ Persistent Memory Architectures</div>

<div class="enhancement-content">
<p><strong>Unlike traditional agents, Agentic AI maintains rich memory systems:</strong></p>

### 🧠 Memory Types in AI Agents

| Memory Type | Description | Example Use |
|------------|------------|-------------|
| **Episodic** 📅 | Task-specific history | User searched hotels in Paris in March |
| **Semantic** 📚 | Long-term facts | User prefers 4-star hotels, vegetarian |
| **Procedural**🔧 | How-to knowledge | Flight booking → dates → prices → seat → pay |


<div class="framework-box">
<h5>🔍 Vector-Based Memory for RAG</h5>
<div class="code-flow">
User Query: "What did we discuss about Q3?"
    ↓
Embedding: [0.23, -0.45, 0.67, ...]
    ↓
Vector Search: Find similar embeddings
    ↓
Retrieve: Past Q3 conversation chunks
    ↓
Response: LLM + Retrieved Context
</div>
</div>
</div>
</div>

<div class="enhancement-card enhancement-4">
<div class="enhancement-title">4️⃣ Orchestration Layers / Meta-Agents</div>

<div class="enhancement-content">
<p><strong>Orchestrators coordinate multiple subordinate agents:</strong></p>

<div class="framework-box">
<h5>🎯 Meta-Agent Responsibilities</h5>
<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 10px; margin: 15px 0;">
<div style="background: rgba(102,126,234,0.1); padding: 10px; border-radius: 8px; font-size: 0.9em;">
✓ Task decomposition
</div>
<div style="background: rgba(102,126,234,0.1); padding: 10px; border-radius: 8px; font-size: 0.9em;">
✓ Agent assignment
</div>
<div style="background: rgba(102,126,234,0.1); padding: 10px; border-radius: 8px; font-size: 0.9em;">
✓ Dependency management
</div>
<div style="background: rgba(102,126,234,0.1); padding: 10px; border-radius: 8px; font-size: 0.9em;">
✓ Conflict resolution
</div>
<div style="grid-column: span 2; background: rgba(102,126,234,0.1); padding: 10px; border-radius: 8px; font-size: 0.9em; text-align: center;">
✓ Result synthesis
</div>
</div>
</div>

<div style="text-align: center; margin: 15px 0;">
<div style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); color: white; padding: 12px; border-radius: 10px; margin-bottom: 10px; font-weight: bold;">META-AGENT</div>
<div style="font-size: 2em; color: #667eea;">↓</div>
<div style="display: flex; justify-content: space-around; gap: 10px;">
<div style="background: linear-gradient(135deg, #55efc4 0%, #00b894 100%); color: white; padding: 10px; border-radius: 8px; flex: 1; font-size: 0.85em;">Agent 1</div>
<div style="background: linear-gradient(135deg, #55efc4 0%, #00b894 100%); color: white; padding: 10px; border-radius: 8px; flex: 1; font-size: 0.85em;">Agent 2</div>
<div style="background: linear-gradient(135deg, #55efc4 0%, #00b894 100%); color: white; padding: 10px; border-radius: 8px; flex: 1; font-size: 0.85em;">Agent 3</div>
</div>
</div>

<div class="example-highlight">
<strong>🎯 Example - ChatDev:</strong>
<p style="margin: 8px 0; font-size: 0.9em;">CEO meta-agent distributes subtasks to departmental agents, integrates their outputs into unified software product.</p>
</div>
</div>
</div>

</div>

---

### Role of LLMs as Reasoning Engines 🧠

Large Language Models have become the cognitive core of modern AI agents:

#### Why LLMs Transform Agent Capabilities

<div class="stat-box">
LLMs enable AI agents to move from reactive scripting to genuine reasoning
</div>

<div class="agent-comparison-container">

<div class="agent-comparison-grid">

<div class="agent-box traditional-box">
<div class="agent-box-title">🔴 Traditional Agent (Pre-LLM)</div>

<div class="agent-code">
<span class="keyword">def</span> <span class="function">process_query</span>(query):
    <span class="keyword">if</span> <span class="string">"refund"</span> <span class="keyword">in</span> query.lower():
        <span class="keyword">return</span> <span class="string">"Initiating refund..."</span>
    <span class="keyword">elif</span> <span class="string">"tracking"</span> <span class="keyword">in</span> query.lower():
        <span class="keyword">return</span> <span class="string">"Retrieving tracking..."</span>
    <span class="keyword">else</span>:
        <span class="keyword">return</span> <span class="string">"I don't understand"</span>
</div>

<div class="agent-verdict">
❌ Brittle, limited to predefined patterns
</div>
</div>

<div class="agent-box llm-box">
<div class="agent-box-title">🟢 LLM-Powered Agent</div>

<div class="agent-code">
<span class="keyword">def</span> <span class="function">process_query</span>(query):
    intent = llm.<span class="function">analyze_intent</span>(query)
    context = llm.<span class="function">extract_entities</span>(query)
    plan = llm.<span class="function">create_action_plan</span>(
        intent, context
    )
    result = <span class="function">execute_plan</span>(plan)
    response = llm.<span class="function">generate_response</span>(
        result
    )
    <span class="keyword">return</span> response
</div>

<div class="agent-verdict">
✅ Flexible, handles novel situations
</div>
</div>

</div>

</div>

---

#### Five Key Capabilities LLMs Bring

1. **Natural Language Understanding**
   - Parse ambiguous requests
   - Handle multiple languages
   - Understand context and nuance

2. **Planning & Decomposition**
   - Break complex tasks into subtasks
   - Determine execution order
   - Handle dependencies

3. **Tool Selection & Use**
   - Choose appropriate APIs/functions
   - Generate correct parameters
   - Interpret tool outputs

4. **Reasoning & Inference**
   - Draw logical conclusions
   - Apply common sense
   - Handle edge cases

5. **Natural Response Generation**
   - Produce human-like text
   - Adapt tone appropriately
   - Explain decisions

---

#### LLM Integration Patterns

<div class="pattern-grid">

<div class="pattern-card pattern-1">
<div class="pattern-title">🎯 Pattern 1: LLM-as-Planner</div>

<div class="pattern-flow">
User Goal → LLM decomposes → Subtasks → Classical execution
</div>

<div class="pattern-example">
<strong>Example:</strong> "Plan my day"<br/>
→ [check_calendar, prioritize_tasks, schedule_breaks, send_reminders]
</div>
</div>

<div class="pattern-card pattern-2">
<div class="pattern-title">⚖️ Pattern 2: LLM-as-Judge</div>

<div class="pattern-flow">
Multiple options → LLM evaluates → Selects best → Execute
</div>

<div class="pattern-example">
<strong>Example:</strong> 3 customer response drafts<br/>
→ LLM picks most appropriate tone → Send selected response
</div>
</div>

<div class="pattern-card pattern-3">
<div class="pattern-title">🔄 Pattern 3: LLM-as-Translator</div>

<div class="pattern-flow">
Structured data → LLM converts → Natural language → User
</div>

<div class="pattern-example">
<strong>Example:</strong> SQL results → LLM generates<br/>
→ "Your sales increased 23% in Q4, driven by product X"
</div>
</div>

<div class="pattern-card pattern-4">
<div class="pattern-title">🔁 Pattern 4: Hybrid Loop</div>

<div class="pattern-flow">
User request → LLM plans → Executes tool → LLM interprets → Next step → Loop until goal achieved
</div>

<div class="pattern-example">
<strong>Example:</strong> Complex multi-step tasks requiring iterative refinement and tool usage
</div>
</div>

</div>

---

### 💡 Interactive Architecture Design Challenge

<div class="interactive-box">

**🎯 CHALLENGE: Design an AI Agent Architecture**

**Scenario:** Your company wants to build an **Automated Meeting Summarizer** that:
1. Joins video calls
2. Transcribes speech
3. Identifies action items
4. Sends summary emails to participants
5. Creates calendar reminders for follow-ups

**Your Task:** Design the architecture using the three-layer model and identify key components.

**Guiding Questions:**
1. What happens at each layer (Application, Orchestration, Reasoning)?
2. Which technological paradigms are needed?
3. What tools/APIs would the agent invoke?
4. Where does the LLM fit in?
5. How does the Perceive-Reason-Act cycle work here?

</div>

#### Sample Solution (Click to Reveal)

<details>
<summary>💡 Click here to see suggested architecture</summary>

```ascii
┌──────────────────────────────────────────────────────────┐
│              APPLICATION LAYER                           │
├──────────────────────────────────────────────────────────┤
│ • Video conferencing integration (Zoom/Teams API)        │
│ • Email client (Gmail/Outlook API)                       │
│ • Calendar API (Google Calendar, Outlook)                │
│ • Web dashboard for configuration                        │
└────────────────┬─────────────────────────────────────────┘
                 ↓
┌──────────────────────────────────────────────────────────┐
│              ORCHESTRATION LAYER                         │
├──────────────────────────────────────────────────────────┤
│ Workflow Manager:                                        │
│ 1. Join meeting (video API)                              │
│ 2. Start transcription service                           │
│ 3. Stream audio → transcription → LLM                    │
│ 4. Maintain meeting context in memory                    │
│ 5. Post-meeting: trigger summarization pipeline          │
│ 6. Invoke email sender with formatted summary            │
│ 7. Create calendar events for action items               │
│                                                          │
│ Tools: meeting_join, transcribe_audio, send_email,       │
│        create_calendar_event, get_attendee_list          │
└────────────────┬─────────────────────────────────────────┘
                 ↓
┌──────────────────────────────────────────────────────────┐
│              REASONING LAYER                             │
├──────────────────────────────────────────────────────────┤
│ LLM (GPT-4/Claude):                                      │
│ • Identify speaker transitions                           │
│ • Extract key discussion points                          │
│ • Detect action items with assignments                   │
│ • Determine priority/urgency                             │
│ • Generate concise summary                               │
│                                                          │
│ NLP Model:                                               │
│ • Named entity recognition (people, dates, projects)     │
│                                                          │
│ Audio Model:                                             │
│ • Speech-to-text (Whisper, AssemblyAI)                   │
└──────────────────────────────────────────────────────────┘
```

**Perceive-Reason-Act Cycle:**

1. **Perceive:** Audio stream + metadata (attendees, meeting title)
2. **Reason:** LLM identifies key points, action items, decisions
3. **Act:** Send emails, create calendar events
4. **Perceive:** Feedback loop if recipients respond or reschedule
5. **Reason:** Update understanding of action item status
6. **Act:** Send reminders or update task tracking system

**Technological Paradigms Used:**

- **Classical Software:** API calls, error handling, scheduling
- **Neural Networks:** Speech recognition, speaker diarization
- **Foundation Models (LLMs):** Summarization, action item extraction
- **Autonomous Control:** Meeting join/leave timing, workflow orchestration

</details>

---

## 📚 Module 1 Summary

<div class="key-point">

### Key Takeaways

✅ **AI Agents** are autonomous, task-specific, reactive software entities that perceive, reason, and act

✅ **Perceive-Reason-Act Cycle** is the fundamental operational loop of all AI agents

✅ **Three-Layer Architecture** (Application, Orchestration, Reasoning) provides the structural foundation

✅ **Four Subsystems** (Perception, KRR, Action, Learning) enable complete agent functionality

✅ **Agentic AI** represents an evolution to multi-agent, collaborative systems with advanced reasoning

✅ **LLMs** serve as reasoning engines, enabling natural language understanding, planning, and flexible behavior

</div>

---

## 🎯 Self-Assessment Quiz

Test your understanding:

<div class="quiz-container">

<div class="quiz-question">

**1. What is the primary difference between traditional automation and AI agents?**

[[ ]] Speed of execution
[[X]] Adaptive intelligence and context-awareness
[[ ]] Cost efficiency
[[ ]] Programming language used
[[?]] Think about what makes AI agents "intelligent" - it's their ability to adapt and understand context, not just execute predefined rules.
***************

✅ **Correct!** AI agents excel at adaptive intelligence and context-awareness, allowing them to handle dynamic situations unlike traditional automation which follows fixed rules.

***************

</div>

<div class="quiz-question">

**2. In the Perceive-Reason-Act cycle, where does tool invocation happen?**

[[ ]] Perceive phase
[[ ]] Reason phase
[[X]] Act phase
[[ ]] All phases
[[?]] Tool invocation is an action - think about which phase involves executing actions on the environment.
***************

✅ **Correct!** Tool invocation happens in the Act phase, where the agent executes its planned actions on the environment.

***************

</div>

<div class="quiz-question">

**3. Which layer manages workflow coordination and dependencies?**

[[ ]] Application Layer
[[X]] Orchestration Layer
[[ ]] Reasoning Layer
[[ ]] None of the above
[[?]] Think about which layer sits between the user-facing application and the core reasoning engine.
***************

✅ **Correct!** The Orchestration Layer manages workflow coordination, task decomposition, and dependencies between different components.

***************

</div>

<div class="quiz-question">

**4. What is a key enhancement of Agentic AI over traditional AI agents?**

[[ ]] Faster processing speed
[[ ]] Lower cost
[[X]] Multi-agent collaboration and shared memory
[[ ]] Simpler architecture
[[?]] Agentic AI is about multiple agents working together - what capability enables this collaboration?
***************

✅ **Correct!** Agentic AI systems enable multiple specialized agents to collaborate through shared memory and coordinated workflows, unlike single traditional agents.

***************

</div>

<div class="quiz-question">

**5. Which technological paradigm is primarily responsible for natural language understanding in modern agents?**

[[ ]] Classical Software
[[ ]] Neural Networks
[[X]] Foundation Models (LLMs)
[[ ]] Autonomous Control
[[?]] Think about which technology enables agents to understand and generate human-like text and reasoning.
***************

✅ **Correct!** Foundation Models (LLMs) like GPT-4 provide the natural language understanding and reasoning capabilities that power modern AI agents.

***************

</div>

</div>

---

## 🔗 Bridge to Module 2

In the next module, we'll explore:

🎯 **Design, Ethics & Human-Centered AI** 

>  Critical Examination of AI Agents in Academia

> Beyond the Hype: Responsible Design & Implementation

---

## 📖 Additional Resources


**Research Papers:**

- Elsevier (2025) - "Agentic AI in Academia: How to Adopt for Research, Learning and Innovation"
- Monigatti (2025) - "Making Sense of Memory in AI Agents"


**Technical Frameworks:**

- Red Hat (2025) - "Maximize AI Innovation with Open Source Models"
- LangChain Documentation
- LangGraph for Multi-Agent Systems


**Industry Reports:**

- World Economic Forum (2025) - "AI Agents in Action: Foundations for Evaluation and Governance"
- QuantumBlack McKinsey (2025) - "The State of AI in 2025: Agents, Innovation and Transformation"


---

> **🎓 Congratulations on completing Module 1!**
>
> You now understand the technical foundations of AI agents. Ready to learn how to classify and evaluate them?
>
> **Continue to Module 2: Functional Classification** →
