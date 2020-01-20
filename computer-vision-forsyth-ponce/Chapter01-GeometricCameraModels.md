# Geometric Camera Models

## Image Formation

### Pinhole Perspective

A pinhole camera forces light through a small hole at the front onto a translucent plate at the back. The image will appear flipped upside down. Due to perspective things further away appear smaller than things closer to the pinhole. Also, parallel lines seem to converge on a horizon line, e.g. train tracks going into the distance.
When we look at an object through a pinhole the resulting object on the image plane can be written like so

$$x = d\frac{X}{Z}$$

$$y = d\frac{Y}{Z}$$

where *x* and *y* denote the point on the image plane and *X* and *Y* the point on the real object in space. *d* is the distance between the pinhole and the image plane and *Z* the distance from the actual point in space to the pinhole. Simply put, there is a direct relationship of these points in respect to their distances from the pinhole. Moving the object closer to the pinhole changes its *x* and *y* coordinates on the image plane, stretching the final image.

### Weak Perspective

An even coarser approximation of the geometry is *weak perspective*. The pinhole can be thought of being between two image planes. If both of these planes have equal distance from the pinhole their coordinates are equal on their respective image plane, which is called *orthographic projection*.

$$x = X$$

$$y = Y$$

In other cases the parallel planes with different distances from the pinhole have the following relationship

$$x = -mX$$
$$y = -mY$$

$$ where m = -\frac{d}{Z}

### Camera with Lenses

