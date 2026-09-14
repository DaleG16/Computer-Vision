# Experiment 1 – Haar Wavelet Decomposition

## Aim

To apply Haar wavelet decomposition to a handwritten digit image and extract important features from the image.

## Objective

The objective of this experiment is to decompose a handwritten digit image into different frequency components using the Haar wavelet transform.

The decomposition produces four sub-bands:

- **LL** – Approximation
- **LH** – Vertical details
- **HL** – Horizontal details
- **HH** – Diagonal details

## Libraries Used

- Python
- OpenCV
- NumPy
- Matplotlib

## Theory

The Haar wavelet transform is used to analyze an image at different frequency levels. It uses two basic operations:

### Low-Pass Filtering

Low-pass filtering calculates the average of adjacent pixels.

```
Low-pass → Average → Smooth / low-frequency information
```

### High-Pass Filtering

High-pass filtering calculates the difference between adjacent pixels.

```
High-pass → Difference → Edge / high-frequency information
```

These operations are applied in both horizontal and vertical directions to obtain four sub-bands.

### Haar Wavelet Components

| Component | Filtering | Information |
|-----------|-----------|-------------|
| LL | Low-pass + Low-pass | Approximation |
| LH | Low-pass + High-pass | Vertical details |
| HL | High-pass + Low-pass | Horizontal details |
| HH | High-pass + High-pass | Diagonal details |


## Input

A handwritten digit image is used as the input.

Example: `4.png`

## Output

The program displays:

```
Original Image | LL | LH | HL | HH
```

The LL component represents the approximation of the original image, while LH, HL, and HH represent different directional and high-frequency details.

## Result

The handwritten digit image was successfully decomposed using the Haar wavelet transform into four sub-bands: LL, LH, HL, and HH.

The decomposition demonstrates how the overall structure of the image is preserved in the LL component while edge and fine-detail information is captured by the high-frequency components.
