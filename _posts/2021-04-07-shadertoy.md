---
title: Shadertoy记录
tags: [Projects]
style: 
color: 
description: Ray Marching原理，还有一些Shader的学习记录。
comments: true
---



<br/>

### Ray Marching原理

在Shadertoy里只处理片元着色器，输入FragCoord，通过自己的操作输出该点的颜色值，因此处理3d物体必须用到Ray Marching。

如图所示：

![avatar](../assets/img/post2/sdtoy/2.png)

 

连接摄像机和像素点，向前延伸，和物体求交点，符合相交条件则进行处理，利用distance去计算该点上的颜色。



![avatar](../assets/img/post2/sdtoy/1.png)



光线步进的大概原理如下：

![avatar](../assets/img/post2/sdtoy/3.png)

```glsl
float RayMarching(vec3 ro, vec3 rd)
{
    float dO = 0.;

    for (int i = 0; i < MAX_STEPS; i++)
    {
    	vec3 p = ro + dO * rd;
    	float dS = GetDist(p);
    	dO += dS;
    	if (dS < SURF_DIST || dO > MAX_DIST) break;
    }

    return dO;
}
```



<br/>

<br/>


