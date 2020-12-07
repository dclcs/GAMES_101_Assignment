# Introduction to Computer Graphics

### Lec4 : Transformation Cont.

##### 3D transformations

- Think about how to take a photo
  - Find a good place and arange people(**model** transformation)
  - Find a good "angle" to put the camera(**view** transformation)

- Viewing transformation(观测矩阵)
  - View / Camera transformation（视图矩阵）
    - Define the camera first
      - Position : $\vec e$
      - Look-at / gaze direction : $\hat g$
      - Up direction : $\hat t$(assuming prep. to look-at)
    - key observation
      - If the camera and all obejcts move togethor, the "photo" will be the same
    - How about that we always transform the camera to 
      - The origin, up at $Y$, and look at $-Z$
      - And transform the objects along wih the camera
      - $M_{view}$, it's located at the origin, up at $Y$, look at $-Z$
        - Translate $e$ to origin
        - Rotates $\hat g$ to $-Z$
        - Rotate $\hat t$ to $Y$
        - Rotates $(g x t)$ to $X$
        - Difficult to write!!!

<img src="https://tva1.sinaimg.cn/large/0081Kckwgy1glela8i8umj30jq0eggmi.jpg" alt="截屏2020-12-07 上午12.11.45" style="zoom:50%;" /><img src="https://tva1.sinaimg.cn/large/0081Kckwgy1glelgp9k7kj30lo0f6dgq.jpg" alt="截屏2020-12-07 上午12.20.00" style="zoom:50%;" />


- s
	- sda
	- Projection transformation
 - Orthographic projection
    - Perspective projection
- fovY(filed of view)  and aspect ratio

    - $tan{\frac{\text{fovY} }{2}} = \frac{t}{|n|}$ 
    - $\text{aspect} = \frac{r}{t}$

