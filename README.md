Financial Calculators Website
Overview
A modern, responsive web-based financial calculator suite featuring three main calculators:

Percentage Calculator: Performs real-time percentage calculations with multiple modes (Find X% of Y, What percent is X of Y, Increase/Decrease by %)
EMI Calculator: Calculate loan EMI, total interest, and payment breakdown with interactive charts and sliders
eCommerce Profit Calculator: Calculate net profit, profit margins, markup percentages, and break-even prices for product sales
The application provides intuitive interfaces with instant visual feedback, explanations, and modern UI design across all devices.

User Preferences
Preferred communication style: Simple, everyday language.

System Architecture
Frontend Architecture
Pure Client-Side Application: Built using vanilla HTML5, CSS3, and JavaScript without any frameworks or build tools
Multi-Page Application: Three main calculator pages with shared styling and cross-navigation
Component-Based JavaScript: Object-oriented design with separate calculator classes (PercentageCalculator, EMICalculator, and ProfitCalculator) that handle logic and UI interactions
Real-Time Calculations: Event-driven architecture that recalculates results instantly as users type, providing immediate feedback
Interactive Elements: Range sliders, dropdowns, and input synchronization for enhanced user experience
Data Visualization: Chart.js integration for EMI breakdown visualization with animated pie charts
Responsive Design: Mobile-first CSS approach with flexbox layouts and CSS Grid for optimal viewing across all device sizes
UI/UX Design Patterns
Mode-Based Interface: Tab-like switching between different calculation types (Find X% of Y, What percent is X of Y, Increase/Decrease by %)
Glassmorphism Design: Modern UI aesthetic using backdrop filters, transparency effects, and gradient backgrounds
Progressive Enhancement: Core functionality works without JavaScript, with enhanced features added progressively
Accessibility: Semantic HTML structure with proper labeling and keyboard navigation support
State Management
Local State: Calculator state managed entirely in browser memory using JavaScript object properties
No Persistence: Calculations are session-based with no data storage requirements
Event-Driven Updates: UI updates triggered by input events and mode changes
Styling Architecture
CSS Custom Properties: Consistent theming and easy maintenance through CSS variables
Animation Framework: CSS animations and transitions for smooth user interactions
Modular CSS: Organized stylesheet with clear separation between layout, components, and utilities
External Dependencies
Third-Party Libraries
Font Awesome 6.4.0: Icon library loaded via CDN for UI icons and visual elements
Chart.js: JavaScript charting library for EMI breakdown visualization and animated pie charts
Google Fonts: Web fonts for enhanced typography (implied by font-family stack)
Browser APIs
DOM API: Standard web APIs for element manipulation and event handling
CSS Features: Modern CSS features including Grid, Flexbox, and backdrop-filter
Development Dependencies
None: No build process, package managers, or development tools required
Direct Deployment: Static files can be served directly from any web server
