# NeuralCanvas

AI-powered generative art studio with real-time style transfer.

## Overview

NeuralCanvas is an interactive canvas application that applies neural style transfer in real-time. It provides multiple AI models for different artistic styles, with adjustable parameters and layer blending capabilities.

## Features

- **Real-time Style Transfer**: Apply artistic styles as you draw
- **Multiple AI Models**: Various pre-trained networks for different aesthetics
- **Parameter Controls**: Fine-tune style intensity, color preservation, and detail
- **Layer Blending**: Combine multiple styles with opacity and blend modes
- **Export Options**: Save high-resolution outputs in multiple formats

## Technical Stack

- **Python** - Model training and inference backend
- **TensorFlow** - Neural network implementations
- **WebGL** - GPU-accelerated canvas rendering
- **React** - User interface components
- **FastAPI** - High-performance API server

## Style Transfer Pipeline

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Content   │────▶│   Encoder   │────▶│  Content    │
│   Image     │     │   Network   │     │  Features   │
└─────────────┘     └─────────────┘     └──────┬──────┘
                                               │
┌─────────────┐     ┌─────────────┐     ┌──────▼──────┐
│   Style     │────▶│   Encoder   │────▶│  AdaIN     │
│   Image     │     │   Network   │     │  Transform  │
└─────────────┘     └─────────────┘     └──────┬──────┘
                                               │
                                        ┌──────▼──────┐
                                        │   Decoder   │
                                        │   Network   │
                                        └──────┬──────┘
                                               │
                                        ┌──────▼──────┐
                                        │  Stylized   │
                                        │   Output    │
                                        └─────────────┘
```

## Available Styles

- Impressionist (Monet, Van Gogh)
- Abstract (Kandinsky, Pollock)
- Classical (Renaissance, Baroque)
- Modern (Cubism, Pop Art)
- Custom (Upload your own)

## Performance

- WebGL shader-based rendering for 60fps interaction
- Progressive quality for real-time preview
- Full resolution processing on export

## Demo

View the live demo at: https://danielminton.github.io/NeuralCanvas/

## Local Development

```bash
# Backend
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend
npm install
npm run dev
```

## Author

Daniel Minton