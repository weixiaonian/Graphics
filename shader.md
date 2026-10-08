# 前置数学：

## 向量

数轴上的都是实数

值得距离，相减的绝对值

偏移量，相对位置（加上距离）

向量可以视为角度和长度（仅表示相对方向和大小）
```gdscript
godot中的向量：
$Node2D.position = Vector2(100,200)
表示以屏幕左上角为原点，向右100，向下200
通过点引用访问分量
position.x
```
abs()绝对值函数|n|

sign(a) 获得符号函数(正1负-1)

(标量\*单位轴，标量\*单位轴)

```math
\vec A + \vec B = (A_x+B_x,A_y+B_y)
```

向量取反就是x和y加负号，两个向量相减获得差值
要找到A指向B的向量，使用B-A

```math
B到A的向量：\vec A - \vec B = \vec A + (- \vec B) = (A_x - B_x,A_y - B_y)
```

```gdscript
var AP = A.direction_to(P)
AP是A朝向P的向量
```
```gdscript
向量乘以/除以标量，相当于向量的各分量乘/除标量
```


```math
向量长度(模长)||\vec V||=\sqrt {v_x^2+v_y^2}
```
```math
向量归一化\hat v = (V.x / \|V\|,V.y / \|V\|)
```
```gdscript
godot中向量a归一化
a=a.normalized()
```

```math
标量a*向量v=(a*v.x,a*v.y)
```
```math
点积（两个向量关系）：\vec V \cdot \vec U=V.x \times U.x + V.y \times U.y=
\|\vec V\|\|\vec U\|\cos \theta
```

```gdscript
godot中点积：c = a.dot(b)
```

```math
标量投影：\hat a \cdot \vec b 得到的是b作垂直辅助线到\vec a的投影，\\沿着a的有符号长度
```
```math
\cos \theta = \hat a \cdot \hat b
```
```math
向量投影：\hat a (\hat a \cdot \vec b)
```
叉积
```math
叉积的结果是垂直于两个向量的向量\\
\|\vec a \times \vec b\| = \|\vec a\|\|b\|\sin \theta
```
```gdscript
var c = a.cross(b)
```
通过表面两个点的叉积来获取表面的法线
通过两个对象的面向叉积获取围绕哪个轴旋转

让点与面的法线点乘，可以知道点位于面的哪一侧，点积是点与该平面的距离


空间平面，原点顺着平面的法线方向的距离D和法线N组成平面
# 一些着色器概念

次表面散射

光穿过物体表面，进入材质内部进行随机散射，部分波长的光被吸收，反射出来的光颜色会改变

顶点着色器

对所有顶点进行遍历执行

片段着色器

对每个片段遍历，确定像素颜色
