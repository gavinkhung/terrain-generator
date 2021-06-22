# terrain-generator

Terrain Generation using the Perlin Noise algorithm, NumPy, and Matplotlib

## Perlin Noise

Perlin Noise provides smooth random noise.

## Perlin Noise's 3 steps

- Grid Definition
- Dot product calculation between the random gradient and distance vectors
- Interpolation of dot product values

### Grid Definition

There is a grid that represents the pixel of the images and another grid on top of the first grid. The corners of the squares on the second grid represent the position of random gradient and distance vectors. Increasing the input will increase the number of rectangles in the grid, increasing the detail of the noise.

### Calculating of the dot product

The dot product is calculated using the random gradient vector and the distance vector. A random gradient vector is a vector pointing in a random direction on every corner of the squares on the second grid. The gradient vectors should be equally distributed in each direction. A distance vector is a vector pointing from the current rectangle of the first grid to the corner of the squares in the second grid.

### Interpolation of dot products

After the calculations are done, there are multiple dot products. After interpolation, you will get the value of the square. A fade function is used to remove artifacts.

## Program Output

![Matplotlib 3d Projection](./perlin-noise-1.png 'Perlin Noise 3d')
![Matplotlib Black and White Image](./perlin-noise-2.png 'Perlin Noise Img')
