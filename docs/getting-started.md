# Getting Started

## Quick Start

This guide will help you get started with the Mechanistic Interpretability Showcase.

### Viewing the Showcase

The easiest way to view the showcase is to open `index.html` in your web browser.

#### Method 1: Direct File Opening

Simply double-click the `index.html` file in your file explorer, and it will open in your default browser.

#### Method 2: Local Web Server (Recommended)

Using a local web server provides a better development experience:

**Using Python:**
```bash
# Navigate to the project directory
cd MechanisticInterpretabilityShowcase

# Start a simple HTTP server
python -m http.server 8000

# Open http://localhost:8000 in your browser
```

**Using Node.js:**
```bash
# Install http-server globally (one-time setup)
npm install -g http-server

# Start the server
http-server

# Open http://localhost:8080 in your browser
```

**Using VS Code:**
1. Install the "Live Server" extension
2. Right-click `index.html`
3. Select "Open with Live Server"

### Project Structure

```
MechanisticInterpretabilityShowcase/
├── index.html          # Main HTML page
├── styles.css          # Styling and layout
├── script.js           # Interactive functionality
├── docs/               # Documentation
│   ├── README.md       # Documentation home
│   ├── getting-started.md  # This file
│   └── examples.md     # Example use cases
├── .gitignore          # Git ignore file
├── README.md           # Project README
└── LICENSE             # License information
```

### Customizing the Showcase

#### 1. Update Content

Edit `index.html` to modify:
- Hero section text
- Research topics
- Demo descriptions
- About section

#### 2. Change Styling

Edit `styles.css` to customize:
- Colors (defined in CSS variables)
- Fonts
- Layout
- Animations

#### 3. Add Interactivity

Edit `script.js` to add:
- Custom animations
- Interactive features
- Data visualizations
- User interactions

### Next Steps

1. Explore the [Examples](examples.md) to see what you can build
2. Check out the main [README](../README.md) for contribution guidelines
3. Visit the showcase page to see the interface

## Need Help?

If you encounter any issues or have questions:
- Check the documentation in the `docs/` folder
- Open an issue on [GitHub](https://github.com/PrecisionNeuroLab/MechanisticInterpretabilityShowcase/issues)
- Review the examples for common patterns
