# 前置数学：

## 向量

数轴上的都是实数

值得距离，相减的绝对值

偏移量，相对位置（加上距离）

abs()绝对值函数|n|

sign(a) 获得符号函数(正1负-1)

(标量\*单位轴，标量\*单位轴)

```math
\vec A + \vec B = (A_x+B_x,A_y+B_y)
```

向量取反就是x和y加负号，两个向量相减获得差值

```math
B到A的向量：\vec A - \vec B = \vec A + (- \vec B) = (A_x - B_x,A_y - B_y)
```

```math
向量长度(模长)||\vec V||=\sqrt {v_x^2+v_y^2}
```
```math
向量归一化\hat v = (V.x / \|V\|,V.y / \|V\|)
```

```math
标量a*向量v=(a*v.x,a*v.y)
```
```math
点积（两个向量关系）：\vec V \cdot \vec U=V.x \times U.x + V.y \times U.y=
\|\vec V\|\|\vec U\|\cos \theta
```
```math
标量投影：\hat a \cdot \vec b 得到的是b作垂直辅助线到\vec a的投影，\\沿着a的有符号长度
```
```math
\cos \theta = \hat a \cdot \hat b
```
# 一些着色器概念

次表面散射

光穿过物体表面，进入材质内部进行随机散射，部分波长的光被吸收，反射出来的光颜色会改变

顶点着色器

对所有顶点进行遍历执行

片段着色器

对每个片段遍历，确定像素颜色
