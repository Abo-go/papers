# Camera Calibration

## 二次曲线

在仿射平面上，齐次仿射坐标$(x_1, x_2, x_3)$满足方程：
$$a_{11}x_1^2 + a_{22}x_2^2 + a_{33}x_3^2 + 2a_{12}x_1x_2 + 2a_{13}x_1x_3 + 2a_{23}x_2x_3 = 0\qquad(1)$$ 
的点的集合叫做仿射平面上的二次曲线。$a_{ij}$为实数至少有一个不为0。
方程(1)可简写成：
$$\sum^3_{i,j=1}a_{ij}x_ix_j = 0,\qquad a_{ij}=a_{ji}$$
用矩阵表示为：
$$(x_1,x_2,x_3)\left( \begin{matrix}a_{11}&a_{12}&a_{13}\\a_{21}&a_{22}&a_{23}\\a_{31}&a_{32}&a_{33}\end{matrix}\right)\left( \begin{matrix}x_1\\x_2\\x_3\end{matrix}\right)\qquad x^TAx = 0$$
当$|A|\neq 0$时，叫做非退化的二次曲线；当$|A|=0$时，叫做退化的二次曲线。

## 对偶原理

二次曲线：$J = x^TCx = 0$,过$x$处的切线参数向量为：$l = \partial J/\partial x=2Cx$则$x=\frac{1}{2}C^{-1}l$,代入上式得：
$$l^T\Omega l = 0\qquad \Omega = C^{-1}$$
称为对偶坐标曲线。

## 摄像机自标定

射影重建提升到欧式重建