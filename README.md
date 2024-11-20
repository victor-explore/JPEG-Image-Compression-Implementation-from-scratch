# JPEG Image Compression Implementation

This repository contains a Python implementation of JPEG-like image compression algorithm. The implementation demonstrates the core concepts of JPEG compression including block-based DCT transformation, quantization, and entropy coding.

## Features

- Image blocking (8x8)
- Discrete Cosine Transform (DCT)
- Quantization using standard JPEG quantization matrix
- Custom entropy coding
- Image reconstruction
- Comparison with PIL's JPEG compression

## Requirements

```python
numpy
matplotlib
pillow
google.colab (if running in Google Colab)
```

## Installation

```bash
git clone https://github.com/yourusername/jpeg-compression.git
cd jpeg-compression
pip install -r requirements.txt
```

## Usage

```python
# Load and process an image
image = load_image('path_to_your_image.jpg')

# Compress the image
compressed_data = compress_image(image)

# Reconstruct the image
reconstructed_image = reconstruct_image(compressed_data)
```

## Implementation Details

### 1. Image Blocking
- Divides input image into 8x8 blocks
- Handles padding for images with dimensions not divisible by 8

### 2. DCT Transform
- Implements 2D DCT for each 8x8 block
- Transforms spatial domain data to frequency domain

### 3. Quantization
- Uses standard JPEG quantization matrix
- Reduces precision of DCT coefficients

### 4. Entropy Coding
- Custom implementation of coefficient encoding
- Uses predefined encoding table for common values

### 5. Reconstruction
- Implements inverse DCT (IDCT)
- Handles dequantization
- Reconstructs full image from blocks

## Performance Metrics

The implementation includes calculation of:
- Mean Squared Error (MSE)
- Compression ratio
- Comparison with PIL's JPEG implementation

## Example Output

```python
Original Image Size: 256x256
Compression Ratio: X:1
MSE: Y
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

- Based on the JPEG compression standard
- Uses standard JPEG quantization matrix
- Inspired by digital image processing principles
