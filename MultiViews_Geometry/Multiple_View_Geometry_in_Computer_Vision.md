# Multiple View Geometry in Computer Vision

## 9. Epipolar Geometry and the Fundamental Matrix

Fundamental Matrix:

- $3 \times 3$ matrix of rank 2.
- A point in 3-space $X$ is imaged as $x$ in the first view,and $x'$ in the second,then the image points satisfy the relation $x'^TFx = 0$.
- it canbe computed from corespondences of imaged scene points alone, without requiring knowledge of the cameras' internal parameters or relative pose.

### 9.1 Epipolar geometry

![fig9.2](9.2.Epipolar_geometry.png)Fig. 9.2. Epipolar geometry

- epipole
- epipolar plane
- epipolar line

Geometric derivation of fundamental matrix:

- transfer via the plane $\pi$.在第一个视图中的所有点点集$x_i$和对应的第二个视图的点集$x'_i$都可以投影到一个共面三维点集$X_i$，因此他们是投影对等的关系，可以找到一个2D单应性矩阵$H_\pi$将每个$x_i$映射到$x'_i$。
- constructing the epipolar line. 给定图像点$x'$,过图像点$x'$和极点$e'$的极线$l'$可以被表示为$l' = e' \times x' = [e']_\times x'$.由于$x'$可以被表示为$x' = H_\pi x$，因此我们有：$l' = [e']_\times H_\pi x = Fx$.我们定义$F = [e']_\times H_\pi$为基础矩阵。

结论9.1：$[e']_\times$的秩为2而$H_\pi$的秩为3,因此F的秩为2。
