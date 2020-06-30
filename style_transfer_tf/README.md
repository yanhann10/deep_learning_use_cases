# Neural style transfer (NST)

### Key concepts

C - content image
S - style image
G - generated image

Loss function include:

1. Content cost:

- squared L2 norm between activation in a layer
- tip: Choose middle activation layer instead of shallow or deep ones.

2. Style cost:

- Activation of a filter is unrolled such that width and height is reshaped into 1D row
- Gram matrix is computed by multiplying this unrolled filter matrix with its transpose. Its dimension is (num_filters, num_filters)
- Describes correlation between activation across channels(filters).
- The style of a layer is defined as squared L2 norm of Gram matrix differences between S and G
- Style cost is calculated as the weighted sum of style across layers
