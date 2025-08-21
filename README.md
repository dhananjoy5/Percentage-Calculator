<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Percentage Calculator - Calculate percentages instantly</title>
    <meta name="description" content="Free online percentage calculator with real-time calculations. Calculate what percentage of a number, percentage increases/decreases, and more.">
    <meta name="keywords" content="percentage calculator, percent calculator, math calculator, online calculator">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Percentage Calculator</h1>
        <p class="subtitle">Calculate percentages instantly in real-time</p>
    </header>

    <main class="calculator-container">
        <div class="calculator">
            <!-- Calculator Mode Selector -->
            <div class="mode-selector">
                <button class="mode-btn active" data-mode="percentage-of">What is % of ?</button>
                <button class="mode-btn" data-mode="is-what-percent">? is what % of ?</button>
                <button class="mode-btn" data-mode="increase-decrease">Increase/Decrease by %</button>
            </div>

            <!-- Calculation Forms -->
            <div class="calculation-forms">
                <!-- What is X% of Y? -->
                <div class="calc-form active" id="percentage-of-form">
                    <div class="input-group">
                        <label for="percentage-input">Percentage (%)</label>
                        <input type="number" id="percentage-input" placeholder="Enter percentage" step="any">
                    </div>
                    <div class="input-group">
                        <label for="base-number-input">of Number</label>
                        <input type="number" id="base-number-input" placeholder="Enter base number" step="any">
                    </div>
                    <div class="result-section">
                        <div class="result-label">Result:</div>
                        <div class="result-value" id="percentage-of-result">0</div>
                        <div class="calculation-display" id="percentage-of-calc"></div>
                    </div>
                </div>

                <!-- X is what percent of Y? -->
                <div class="calc-form" id="is-what-percent-form">
                    <div class="input-group">
                        <label for="part-number-input">Part Number</label>
                        <input type="number" id="part-number-input" placeholder="Enter part number" step="any">
                    </div>
                    <div class="input-group">
                        <label for="whole-number-input">of Whole Number</label>
                        <input type="number" id="whole-number-input" placeholder="Enter whole number" step="any">
                    </div>
                    <div class="result-section">
                        <div class="result-label">Result:</div>
                        <div class="result-value" id="is-what-percent-result">0%</div>
                        <div class="calculation-display" id="is-what-percent-calc"></div>
                    </div>
                </div>

                <!-- Increase/Decrease by X% -->
                <div class="calc-form" id="increase-decrease-form">
                    <div class="input-group">
                        <label for="original-number-input">Original Number</label>
                        <input type="number" id="original-number-input" placeholder="Enter original number" step="any">
                    </div>
                    <div class="input-group">
                        <label for="change-percentage-input">Change (%)</label>
                        <input type="number" id="change-percentage-input" placeholder="Enter percentage change" step="any">
                    </div>
                    <div class="operation-selector">
                        <button class="operation-btn active" data-operation="increase">Increase</button>
                        <button class="operation-btn" data-operation="decrease">Decrease</button>
                    </div>
                    <div class="result-section">
                        <div class="result-label">Result:</div>
                        <div class="result-value" id="increase-decrease-result">0</div>
                        <div class="calculation-display" id="increase-decrease-calc"></div>
                    </div>
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="action-buttons">
                <button class="btn-calculate" id="calculate-btn">Calculate</button>
                <button class="btn-clear" id="clear-btn">Clear All</button>
            </div>
        </div>
    </main>

    <footer>
        <p>&copy; 2025 Percentage Calculator. All rights reserved.</p>
    </footer>

    /* Reset and Base Styles */
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
    flex-direction: column;
    color: #333;
}

/* Header Styles */
header {
    text-align: center;
    padding: 2rem 1rem 1rem;
    color: white;
}

header h1 {
    font-size: 2.5rem;
    font-weight: 300;
    margin-bottom: 0.5rem;
    text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
}

.subtitle {
    font-size: 1.1rem;
    font-weight: 300;
    opacity: 0.9;
}

/* Main Container */
.calculator-container {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 1rem;
}

.calculator {
    background: white;
    border-radius: 16px;
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
    padding: 2rem;
    width: 100%;
    max-width: 500px;
    transition: transform 0.3s ease;
}

.calculator:hover {
    transform: translateY(-2px);
}

/* Mode Selector */
.mode-selector {
    display: flex;
    flex-direction: column;
    gap: 0.5rem;
    margin-bottom: 2rem;
}

.mode-btn {
    padding: 0.75rem 1rem;
    border: 2px solid #e1e5e9;
    background: white;
    color: #666;
    border-radius: 8px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-size: 0.9rem;
    font-weight: 500;
}

.mode-btn:hover {
    border-color: #667eea;
    color: #667eea;
}

.mode-btn.active {
    background: #667eea;
    border-color: #667eea;
    color: white;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);
}

/* Calculation Forms */
.calculation-forms {
    position: relative;
    margin-bottom: 2rem;
}

.calc-form {
    display: none;
    animation: fadeIn 0.3s ease;
}

.calc-form.active {
    display: block;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(10px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Input Groups */
.input-group {
    margin-bottom: 1.5rem;
}

.input-group label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 600;
    color: #333;
    font-size: 0.9rem;
}

.input-group input {
    width: 100%;
    padding: 0.75rem;
    border: 2px solid #e1e5e9;
    border-radius: 8px;
    font-size: 1rem;
    transition: all 0.3s ease;
    background: #fafafa;
}

.input-group input:focus {
    outline: none;
    border-color: #667eea;
    background: white;
    box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
}

.input-group input:hover {
    border-color: #bbb;
}

/* Operation Selector */
.operation-selector {
    display: flex;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
}

.operation-btn {
    flex: 1;
    padding: 0.5rem;
    border: 2px solid #e1e5e9;
    background: white;
    color: #666;
    border-radius: 6px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-size: 0.85rem;
    font-weight: 500;
}

.operation-btn:hover {
    border-color: #667eea;
    color: #667eea;
}

.operation-btn.active {
    background: #667eea;
    border-color: #667eea;
    color: white;
}

/* Result Section */
.result-section {
    background: #f8f9fa;
    border-radius: 8px;
    padding: 1.5rem;
    text-align: center;
    border: 2px solid #e9ecef;
    transition: all 0.3s ease;
}

.result-section.highlight {
    border-color: #667eea;
    background: #f0f3ff;
    transform: scale(1.02);
}

.result-label {
    font-size: 0.9rem;
    font-weight: 600;
    color: #666;
    margin-bottom: 0.5rem;
}

.result-value {
    font-size: 2rem;
    font-weight: 700;
    color: #667eea;
    margin-bottom: 0.5rem;
    transition: all 0.3s ease;
}

.calculation-display {
    font-size: 0.85rem;
    color: #888;
    font-style: italic;
}

/* Action Buttons */
.action-buttons {
    display: flex;
    gap: 1rem;
}

.btn-calculate,
.btn-clear {
    flex: 1;
    padding: 0.75rem;
    border: none;
    border-radius: 8px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
}

.btn-calculate {
    background: #667eea;
    color: white;
}

.btn-calculate:hover {
    background: #5a6fd8;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(102, 126, 234, 0.3);
}

.btn-clear {
    background: #6c757d;
    color: white;
}

.btn-clear:hover {
    background: #5a6268;
    transform: translateY(-1px);
    box-shadow: 0 4px 12px rgba(108, 117, 125, 0.3);
}

/* Footer */
footer {
    text-align: center;
    padding: 1rem;
    color: white;
    font-size: 0.9rem;
    opacity: 0.8;
}

/* Responsive Design */
@media (max-width: 768px) {
    header h1 {
        font-size: 2rem;
    }
    
    .subtitle {
        font-size: 1rem;
    }
    
    .calculator {
        padding: 1.5rem;
        margin: 0.5rem;
    }
    
    .mode-selector {
        gap: 0.25rem;
    }
    
    .mode-btn {
        padding: 0.6rem 0.8rem;
        font-size: 0.8rem;
    }
    
    .result-value {
        font-size: 1.5rem;
    }
    
    .action-buttons {
        flex-direction: column;
    }
}

@media (max-width: 480px) {
    .calculator-container {
        padding: 0.5rem;
    }
    
    .calculator {
        padding: 1rem;
    }
    
    .mode-btn {
        padding: 0.5rem;
        font-size: 0.75rem;
    }
    
    .input-group input {
        padding: 0.6rem;
    }
    
    .result-section {
        padding: 1rem;
    }
    
    .result-value {
        font-size: 1.25rem;
    }
}

/* Animation for number changes */
@keyframes pulse {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.05);
    }
    100% {
        transform: scale(1);
    }
}

.result-value.updated {
    animation: pulse 0.3s ease;
}

/* Error states */
.input-group.error input {
    border-color: #dc3545;
    background: #fff5f5;
}

.error-message {
    color: #dc3545;
    font-size: 0.8rem;
    margin-top: 0.25rem;
}

    <script src="script.js"></script>
</body>
</html>

/**
 * Percentage Calculator - Main JavaScript functionality
 * Handles real-time calculations, UI interactions, and form switching
 */

class PercentageCalculator {
    constructor() {
        this.currentMode = 'percentage-of';
        this.currentOperation = 'increase';
        this.initializeEventListeners();
        this.setupRealTimeCalculation();
    }

    /**
     * Initialize all event listeners for the calculator
     */
    initializeEventListeners() {
        // Mode selector buttons
        const modeButtons = document.querySelectorAll('.mode-btn');
        modeButtons.forEach(btn => {
            btn.addEventListener('click', (e) => this.switchMode(e.target.dataset.mode));
        });

        // Operation selector buttons (for increase/decrease mode)
        const operationButtons = document.querySelectorAll('.operation-btn');
        operationButtons.forEach(btn => {
            btn.addEventListener('click', (e) => this.switchOperation(e.target.dataset.operation));
        });

        // Action buttons
        document.getElementById('calculate-btn').addEventListener('click', () => this.calculateManually());
        document.getElementById('clear-btn').addEventListener('click', () => this.clearAll());

        // Keyboard navigation
        document.addEventListener('keydown', (e) => {
            if (e.key === 'Enter') {
                this.calculateManually();
            } else if (e.key === 'Escape') {
                this.clearAll();
            }
        });
    }

    /**
     * Setup real-time calculation on input events
     */
    setupRealTimeCalculation() {
        // Get all input fields and add real-time calculation
        const inputs = document.querySelectorAll('input[type="number"]');
        inputs.forEach(input => {
            input.addEventListener('input', () => this.calculateRealTime());
            input.addEventListener('keyup', () => this.calculateRealTime());
            input.addEventListener('paste', () => {
                setTimeout(() => this.calculateRealTime(), 10);
            });
        });
    }

    /**
     * Switch between different calculation modes
     * @param {string} mode - The mode to switch to
     */
    switchMode(mode) {
        // Update active mode button
        document.querySelectorAll('.mode-btn').forEach(btn => btn.classList.remove('active'));
        document.querySelector(`[data-mode="${mode}"]`).classList.add('active');

        // Update active form
        document.querySelectorAll('.calc-form').forEach(form => form.classList.remove('active'));
        document.getElementById(`${mode}-form`).classList.add('active');

        this.currentMode = mode;
        this.calculateRealTime();
    }

    /**
     * Switch between increase/decrease operations
     * @param {string} operation - The operation to switch to
     */
    switchOperation(operation) {
        document.querySelectorAll('.operation-btn').forEach(btn => btn.classList.remove('active'));
        document.querySelector(`[data-operation="${operation}"]`).classList.add('active');
        
        this.currentOperation = operation;
        this.calculateRealTime();
    }

    /**
     * Perform real-time calculations based on current mode
     */
    calculateRealTime() {
        try {
            switch (this.currentMode) {
                case 'percentage-of':
                    this.calculatePercentageOf();
                    break;
                case 'is-what-percent':
                    this.calculateIsWhatPercent();
                    break;
                case 'increase-decrease':
                    this.calculateIncreaseDecrease();
                    break;
            }
        } catch (error) {
            console.error('Calculation error:', error);
        }
    }

    /**
     * Calculate "What is X% of Y?"
     */
    calculatePercentageOf() {
        const percentage = parseFloat(document.getElementById('percentage-input').value) || 0;
        const baseNumber = parseFloat(document.getElementById('base-number-input').value) || 0;
        
        const result = (percentage / 100) * baseNumber;
        
        // Update result display
        const resultElement = document.getElementById('percentage-of-result');
        const calcElement = document.getElementById('percentage-of-calc');
        
        resultElement.textContent = this.formatNumber(result);
        calcElement.textContent = `${percentage}% of ${this.formatNumber(baseNumber)} = ${this.formatNumber(result)}`;
        
        this.animateResult(resultElement);
        this.highlightResultSection('percentage-of');
    }

    /**
     * Calculate "X is what percent of Y?"
     */
    calculateIsWhatPercent() {
        const partNumber = parseFloat(document.getElementById('part-number-input').value) || 0;
        const wholeNumber = parseFloat(document.getElementById('whole-number-input').value) || 0;
        
        let result = 0;
        if (wholeNumber !== 0) {
            result = (partNumber / wholeNumber) * 100;
        }
        
        // Update result display
        const resultElement = document.getElementById('is-what-percent-result');
        const calcElement = document.getElementById('is-what-percent-calc');
        
        resultElement.textContent = `${this.formatNumber(result, 2)}%`;
        calcElement.textContent = `${this.formatNumber(partNumber)} is ${this.formatNumber(result, 2)}% of ${this.formatNumber(wholeNumber)}`;
        
        this.animateResult(resultElement);
        this.highlightResultSection('is-what-percent');
    }

    /**
     * Calculate increase/decrease by percentage
     */
    calculateIncreaseDecrease() {
        const originalNumber = parseFloat(document.getElementById('original-number-input').value) || 0;
        const changePercentage = parseFloat(document.getElementById('change-percentage-input').value) || 0;
        
        const changeAmount = (changePercentage / 100) * originalNumber;
        let result;
        
        if (this.currentOperation === 'increase') {
            result = originalNumber + changeAmount;
        } else {
            result = originalNumber - changeAmount;
        }
        
        // Update result display
        const resultElement = document.getElementById('increase-decrease-result');
        const calcElement = document.getElementById('increase-decrease-calc');
        
        resultElement.textContent = this.formatNumber(result);
        
        const operationText = this.currentOperation === 'increase' ? 'increased' : 'decreased';
        calcElement.textContent = `${this.formatNumber(originalNumber)} ${operationText} by ${changePercentage}% = ${this.formatNumber(result)}`;
        
        this.animateResult(resultElement);
        this.highlightResultSection('increase-decrease');
    }

    /**
     * Manual calculation trigger (for the Calculate button)
     */
    calculateManually() {
        this.calculateRealTime();
        
        // Add visual feedback for manual calculation
        const calculateBtn = document.getElementById('calculate-btn');
        calculateBtn.style.transform = 'scale(0.95)';
        setTimeout(() => {
            calculateBtn.style.transform = 'scale(1)';
        }, 150);
    }

    /**
     * Clear all input fields and reset results
     */
    clearAll() {
        // Clear all input fields
        const inputs = document.querySelectorAll('input[type="number"]');
        inputs.forEach(input => {
            input.value = '';
            input.classList.remove('error');
        });

        // Reset all results
        document.getElementById('percentage-of-result').textContent = '0';
        document.getElementById('percentage-of-calc').textContent = '';
        document.getElementById('is-what-percent-result').textContent = '0%';
        document.getElementById('is-what-percent-calc').textContent = '';
        document.getElementById('increase-decrease-result').textContent = '0';
        document.getElementById('increase-decrease-calc').textContent = '';

        // Remove highlighting from result sections
        document.querySelectorAll('.result-section').forEach(section => {
            section.classList.remove('highlight');
        });

        // Add visual feedback for clear action
        const clearBtn = document.getElementById('clear-btn');
        clearBtn.style.transform = 'scale(0.95)';
        setTimeout(() => {
            clearBtn.style.transform = 'scale(1)';
        }, 150);

        // Focus on the first input of current mode
        this.focusFirstInput();
    }

    /**
     * Focus on the first input field of the current mode
     */
    focusFirstInput() {
        const activeForm = document.querySelector('.calc-form.active');
        const firstInput = activeForm.querySelector('input[type="number"]');
        if (firstInput) {
            firstInput.focus();
        }
    }

    /**
     * Format numbers for display with proper decimal places
     * @param {number} num - Number to format
     * @param {number} decimals - Number of decimal places (default: auto)
     * @returns {string} Formatted number string
     */
    formatNumber(num, decimals = null) {
        if (isNaN(num) || !isFinite(num)) {
            return '0';
        }

        // If decimals not specified, use auto formatting
        if (decimals === null) {
            // Remove trailing zeros and limit to 6 decimal places max
            return parseFloat(num.toFixed(6)).toString();
        }

        return num.toFixed(decimals);
    }

    /**
     * Animate result value change
     * @param {HTMLElement} element - Element to animate
     */
    animateResult(element) {
        element.classList.remove('updated');
        setTimeout(() => {
            element.classList.add('updated');
        }, 10);
    }

    /**
     * Highlight the result section for the current calculation
     * @param {string} mode - Current calculation mode
     */
    highlightResultSection(mode) {
        // Remove highlight from all sections
        document.querySelectorAll('.result-section').forEach(section => {
            section.classList.remove('highlight');
        });

        // Add highlight to current section
        const currentSection = document.querySelector(`#${mode}-form .result-section`);
        if (currentSection) {
            currentSection.classList.add('highlight');
        }
    }

    /**
     * Validate input and show error states
     * @param {HTMLInputElement} input - Input element to validate
     * @returns {boolean} True if valid, false otherwise
     */
    validateInput(input) {
        const value = parseFloat(input.value);
        const inputGroup = input.parentElement;
        
        // Remove existing error states
        inputGroup.classList.remove('error');
        const existingError = inputGroup.querySelector('.error-message');
        if (existingError) {
            existingError.remove();
        }

        // Check for invalid values
        if (input.value !== '' && (isNaN(value) || !isFinite(value))) {
            inputGroup.classList.add('error');
            const errorMsg = document.createElement('div');
            errorMsg.className = 'error-message';
            errorMsg.textContent = 'Please enter a valid number';
            inputGroup.appendChild(errorMsg);
            return false;
        }

        return true;
    }
}

// Initialize the calculator when the page loads
document.addEventListener('DOMContentLoaded', () => {
    const calculator = new PercentageCalculator();
    
    // Set up input validation
    const inputs = document.querySelectorAll('input[type="number"]');
    inputs.forEach(input => {
        input.addEventListener('blur', () => calculator.validateInput(input));
    });

    // Focus on first input
    calculator.focusFirstInput();
});

// Add keyboard shortcuts info to console
console.log('Percentage Calculator loaded successfully!');
console.log('Keyboard shortcuts:');
console.log('- Enter: Calculate');
console.log('- Escape: Clear all');
