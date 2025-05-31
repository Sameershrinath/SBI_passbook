# LOGO Encoding and Decoding Project

This project implements a unique way of encoding numerical data into visual patterns using logos. It provides two main implementations:

1. Basic Circle-based Encoding (24-bit)
2. SBI Logo-based Encoding (24-bit)

## Features

### 1. Basic Circle-based Encoding
- Encodes a 24-bit number (0 to 16,777,215) into a pattern of colored circles
- Uses two distinct colors to represent binary 0 and 1
- Default colors: Blue (0, 0, 255) for 0 and Dark Blue (0, 0, 139) for 1
- Organizes circles in an 8×3 grid pattern
- Image size: 500×500 pixels
- Each circle represents one bit of the 24-bit number

### 2. SBI Logo-based Encoding
- Encodes a 24-bit number using miniature SBI logo patterns
- Each logo represents one bit of the binary number
- Uses color variations of the SBI logo to represent 0 and 1
- Default colors:
  - Blue (0, 102, 204) for 0
  - Red (204, 0, 0) for 1
- Features a more sophisticated visual pattern using the SBI logo design
- Supports transparency and advanced image composition

## Usage

### Basic Circle Encoding
```python
# Encode a number into circles
encoded_image = create_color_logo_from_number(11354783)
encoded_image.show()
encoded_image.save("encoded_logo.jpg", format="JPEG")

# Decode the image back to number
binary_result, decoded_number = decode_color_logo(encoded_image)
print(f"Binary: {binary_result}")
print(f"Decoded number: {decoded_number}")
```

### SBI Logo Encoding
```python
# Encode a number using SBI logos
encoded_image2 = create_color_logo_from_number(11568962)
encoded_image2.show()
encoded_image2.save("encoded_logo2.jpg", format="JPEG")

# Decode the SBI logo pattern
binary_result, decoded_number = decode_color_logo(encoded_image2)
print(f"Binary: {binary_result}")
print(f"Decoded number: {decoded_number}")
```

## Technical Details

### Image Specifications
- Output image size: 500×500 pixels
- Circle/Logo size: 40×40 pixels
- Grid layout: 8×3 pattern
- Padding: 30 pixels from edges
- Format support: RGB and RGBA (for transparency)

### Error Handling
- Input validation for numbers (0 to 2²⁴-1)
- Image format validation
- Size and dimension checks
- Color detection and averaging for reliable decoding
- Robust error messages for troubleshooting

## Dependencies
- PIL (Python Imaging Library)
- NumPy (for advanced image processing)
- Python 3.x

## Installation
```bash
pip install Pillow numpy
```

## Applications
1. **Data Visualization**: Convert numerical data into visually appealing patterns
2. **Steganography**: Hide numerical information in logo patterns
3. **Brand Integration**: Incorporate company logos into data visualization
4. **Educational Tool**: Demonstrate binary number systems visually
5. **Design Patterns**: Create unique designs based on numerical input

## Limitations
- Maximum value: 16,777,215 (24-bit)
- Requires consistent image quality for reliable decoding
- Color sensitivity in different lighting conditions
- JPEG compression may affect decoding accuracy

## Future Enhancements
1. Support for larger numbers (32-bit, 64-bit)
2. Additional logo patterns and designs
3. Color scheme customization
4. Error correction codes
5. Support for multiple encoding schemes

## License
This project is open source and available under the MIT License.

## Contributing
Contributions, issues, and feature requests are welcome. Feel free to check issues page if you want to contribute.