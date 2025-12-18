# Mechanistic Interpretability Showcase

A research showcase page demonstrating mechanistic interpretability tools developed by the Precision Neuro Lab. This project aims to make neural networks more transparent and understandable through visualization and analysis techniques.

## Features

- **Clean, Professional Interface**: Modern web design showcasing research and tools
- **Responsive Design**: Works seamlessly across desktop, tablet, and mobile devices
- **Interactive Navigation**: Smooth scrolling and intuitive user experience
- **Extensible Structure**: Easy to add demos, research papers, and interactive visualizations

## Getting Started

### Prerequisites

No build tools or dependencies required! This is a pure HTML/CSS/JavaScript project.

### Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/PrecisionNeuroLab/MechanisticInterpretabilityShowcase.git
   cd MechanisticInterpretabilityShowcase
   ```

2. Open `index.html` in your web browser:
   - **Option 1**: Double-click `index.html`
   - **Option 2**: Use a local server (recommended for development):
     ```bash
     # Using Python 3
     python -m http.server 8000
     
     # Using Node.js (if http-server is installed)
     npx http-server
     ```
   - **Option 3**: Use VS Code Live Server extension

3. Navigate to `http://localhost:8000` in your browser

## Project Structure

```
MechanisticInterpretabilityShowcase/
├── index.html          # Main HTML page
├── styles.css          # Styling and layout
├── script.js           # Interactive functionality
├── docs/               # Documentation and examples
├── README.md           # This file
└── LICENSE             # License information
```

## Customization

### Adding New Research Cards

Edit `index.html` and add new cards in the `research-section`:

```html
<div class="research-card">
    <h3>Your Research Title</h3>
    <p>Description of your research.</p>
</div>
```

### Adding Interactive Demos

Add demo cards in the `demos-section` of `index.html`:

```html
<div class="demo-card">
    <h3>Demo Title</h3>
    <p>Demo description.</p>
    <a href="demo-link.html" class="btn btn-primary">Try Demo</a>
</div>
```

### Styling

Modify colors and styles in `styles.css`. Key CSS variables are defined at the top:

```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #7c3aed;
    /* Add more custom variables */
}
```

## Contributing

We welcome contributions! Please feel free to submit issues or pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Add interactive visualizations using D3.js or Three.js
- [ ] Integrate Jupyter notebooks for live demos
- [ ] Add research paper listings with links
- [ ] Create video tutorials section
- [ ] Add team member profiles
- [ ] Implement search functionality

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or collaborations, please visit our [GitHub repository](https://github.com/PrecisionNeuroLab/MechanisticInterpretabilityShowcase).

## Acknowledgments

- Inspired by research in mechanistic interpretability
- Built for the Precision Neuro Lab community
