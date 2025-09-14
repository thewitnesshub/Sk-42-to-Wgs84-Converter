# SK-42 → WGS84 Coordinate Converter

A web application for converting coordinates from the SK-42 (Soviet Union coordinate system) to WGS84 (World Geodetic System 1984) format.

## Overview

This tool converts coordinates from the SK-42 Gauss-Krüger projection (commonly used in former Soviet Union countries) to the globally standard WGS84 coordinate system.

## Features

- **Coordinate Conversion**: Converts SK-42 to WGS84 coordinates
- **Copy to Clipboard**: Copy converted coordinates
- **Google Maps Integration**: View results in Google Maps
- **Multiple Input Formats**: Accepts various coordinate formats
- **No Dependencies**: Pure HTML, CSS, and JavaScript

## Usage

1. Open `index.html` in a web browser
2. Enter your SK-42 coordinates in the input field
3. Click "Convert" or press Enter
4. View the converted WGS84 coordinates
5. Copy coordinates or open in Google Maps

### Input Format

The converter accepts various input formats:
- `X = 5171098 Y = 6481253`
- `5171098, 6481253`
- `5171098 6481253`
- `X: 5171098, Y: 6481253`

## Technical Details

### Coordinate Systems

- **Input**: SK-42 (Soviet Coordinate System 1942) using Gauss-Krüger projection
- **Output**: WGS84 (World Geodetic System 1984) in decimal degrees

### Conversion Process

1. **Zone Detection**: Automatically detects the UTM zone from the Y coordinate
2. **Inverse Gauss-Krüger**: Converts from projected to geodetic coordinates on Krassovsky ellipsoid
3. **Datum Transformation**: Applies Helmert transformation parameters (ΔX=23.92m, ΔY=-141.27m, ΔZ=-80.9m)
4. **WGS84 Output**: Final coordinates in WGS84 decimal degrees

### Browser Support

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Project Structure

```
Sk-42-to-Wgs84-Converter/
├── index.html          # Main application file
└── README.md          # Project documentation
```

## Algorithm Accuracy

This converter uses a simplified 3-parameter Helmert transformation which provides accuracy suitable for most civilian applications. For higher precision requirements in professional surveying, consider using specialized GIS software with 7-parameter transformations.

## Contributing

Contributions are welcome! Please feel free to submit issues, feature requests, or pull requests.

### Development Setup

1. Clone the repository
2. Open `index.html` in your browser
3. Make changes and test locally
4. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- Coordinate transformation algorithms based on standard geodetic practices
- SK-42 to WGS84 transformation parameters from official geodetic sources

## Support

If you encounter any issues or have questions, please open an issue on GitHub.
