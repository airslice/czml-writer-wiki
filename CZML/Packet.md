# Packet

此页面描述了 CZML 文档或流的可能内容。请阅读 [[CZML Structure]] 以了解如何组合 CZML 文档。

Packet 用于描述场景中单个对象的图形属性，例如单个飞机。

**可插值**: 否 （译注：此处指 packet 本身可插值性，与其内部属性值的可插值性无关）

**范例**:

```javascript
{
    "id": "Facility/AGI",
    "name": "AGI",
    "availability": "2012-03-15T10:00:00Z/2012-03-16T10:00:00Z",
    "description": "<p>Analytical Graphics, Inc. (AGI) develops commercial modeling and analysis software.</p>",
    "billboard": {
        "eyeOffset": {
            "cartesian": [ 0, 0, 0 ]
        },
        "horizontalOrigin": "CENTER",
        "image": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAAAJcEhZcwAADsMAAA7DAcdvqGQAAACvSURBVDhPrZDRDcMgDAU9GqN0lIzijw6SUbJJygUeNQgSqepJTyHG91LVVpwDdfxM3T9TSl1EXZvDwii471fivK73cBFFQNTT/d2KoGpfGOpSIkhUpgUMxq9DFEsWv4IXhlyCnhBFnZcFEEuYqbiUlNwWgMTdrZ3JbQFoEVG53rd8ztG9aPJMnBUQf/VFraBJeWnLS0RfjbKyLJA8FkT5seDYS1Qwyv8t0B/5C2ZmH2/eTGNNBgMmAAAAAElFTkSuQmCC",
        "pixelOffset": {
            "cartesian2": [ 0, 0 ]
        },
        "scale": 1.5,
        "show": true,
        "verticalOrigin": "CENTER"
    },
    "label": {
        "fillColor": {
            "rgba": [ 0, 255, 255, 255 ]
        },
        "font": "11pt Lucida Console",
        "horizontalOrigin": "LEFT",
        "outlineColor": {
            "rgba": [ 0, 0, 0, 255 ]
        },
        "outlineWidth": 2,
        "pixelOffset": {
            "cartesian2": [ 12, 0 ]
        },
        "show": true,
        "style": "FILL_AND_OUTLINE",
        "text": "AGI",
        "verticalOrigin": "CENTER"
    },
    "position": {
        "cartesian": [ 1216469.9357990976, -4736121.71856379, 4081386.8856866374 ]
    }
}
```

```javascript
{
    "id": "document",
    "name": "My Document",
    "version": "1.0",
    "clock": {
        "interval": "2012-03-15T10:00:00Z/2012-03-16T10:00:00Z",
        "currentTime": "2012-03-15T10:00:00Z",
        "multiplier": 60,
        "range": "LOOP_STOP",
        "step": "SYSTEM_CLOCK_MULTIPLIER"
    }
}
```

```javascript
{
    "id": "My Object",
    "delete": true
}
```

## 属性

**id** - string

此 packet 描述的对象的 ID。 ID 不需要是 GUID，但它们确实需要唯一标识 CZML 源中的单个对象以及加载到同一范围内的任何其他 CZML 源。 如果没有指定这个属性，客户端会自动生成一个唯一的。 但是，这会阻止以后的 packet 引用此对象以向其添加更多数据。


**delete** - boolean

客户端是否应删除此对象的所有现有数据，由 ID 标识。如果为真，则此 packet 中的所有其他属性都将被忽略。


**name** - string

对象的名称。 它不必是唯一的，并且旨在供用户使用。


**parent** - string

父对象的 ID（如果有）。


**description** - [[String]]

对象的 HTML 描述。


**clock** - [[Clock]]

整个数据集的时钟设置。仅对 document 对象有效。


**version** - string

正在编写的 CZML 版本。仅对 document 对象有效。


**availability** - [[TimeIntervalCollection]]

对象数据可用的一组时间区间。该属性可以是指定单个区间的单个字符串，也可以是表示区间的字符串数组。如果以后的 CZML packet 发生更改或被发现不正确，则可以更新此可用性。例如，SGP4 传播器可能最初报告所有时间的可用性，但随后传播器抛出异常并且可以调整可用性以在那时结束。如果此可选属性不存在，则假定该对象始终可用。可用性仅限于特定的 CZML 流，因此两个不同的流可以列出单个对象的不同可用性。在单个流中，为对象声明的最后一个可用性是有效的，并且忽略先前数据包中的任何可用性。如果某个对象在某个时间不可用，则客户端将不会绘制该对象。

默认值: `0000-00-00T00:00:00Z/9999-12-31T24:00:00Z`


**properties** - [[CustomProperties]]

此对象的一组自定义属性。


**position** - [[Position]]

物体在世界中的位置。该位置没有直接的视觉表示，但它用于定位广告牌、标签和其他附加到对象的图形项目。

**Examples**:

```javascript
{
    "id": "MyObject",
    "position": {
        "cartographicDegrees": [
            -75.0, 40.0, 0.0
        ]
    }
}
```

```javascript
{
    "id": "InternationalSpaceStation",
    "position": {
        "interpolationAlgorithm": "LAGRANGE",
        "interpolationDegree": 5,
        "referenceFrame": "INERTIAL",
        "epoch": "2012-05-02T12:00:00Z",
        "cartesian": [
            0.0, -6668447.2211117, 1201886.45913705, 146789.427467256,
            60.0, -6711432.84684144, 919677.673492462, -214047.552431458,
            90.0, -6721319.92231553, 776899.784034099, -394198.837519575,
            150.0, -6717826.447064, 488820.628328182, -752924.980158179,
            180.0, -6704450.41462847, 343851.784836767, -931084.800346031,
            240.0, -6654518.44949696, 52891.726433174, -1283967.69137678
        ]
    }
}
```


**orientation** - [[Orientation]]

对象在世界中的方向。方向没有直接的视觉表示，但它用于定向模型、圆锥、金字塔和其他附加到对象的图形项。


**viewFrom** - [[ViewFrom]]

查看此对象时建议的相机位置。该属性被指定为相对于对象位置的东 (x)、北 (y)、上 (z) 参考系中的笛卡尔位置。


**billboard** - [[Billboard]]

广告牌或视口对齐的图像，有时称为标记。广告牌通过 `position` 属性定位在场景中。


**box** - [[Box]]

一个盒子，它是一个封闭的长方体。 使用 `position` 和 `orientation` 属性对盒子进行定位和定向。


**corridor** - [[Corridor]]

走廊，它是由中心线和宽度定义的形状。


**cylinder** - [[Cylinder]]

由长度、顶部半径和底部半径定义的圆柱体、截锥体或圆锥体。 圆柱体使用 `position` 和 `orientation` 属性定位和定向。


**ellipse** - [[Ellipse]]

一个椭圆，它是地球表面上的一条闭合曲线。 椭圆使用 `position` 属性定位。


**ellipsoid** - [[Ellipsoid]]

椭圆体，它是一个封闭的二次曲面，是椭圆的三维模拟。 椭圆体使用 `position` 和 `orientation` 属性进行定位和定向。


**label** - [[Label]]

一串文本。标签通过 `position` 属性定位在场景中。


**model** - [[Model]]

一个 3D 模型。使用 `position` 和 `orientation` 属性对模型进行定位和定向。


**path** - [[Path]]

路径，它是由对象随时间的运动定义的折线。路径的可能顶点由 `position` 属性指定。


**point** - [[Point]]

一个点或视口对齐的圆。 该点通过 `position` 属性定位在场景中。


**polygon** - [[Polygon]]

一个多边形，它是地球表面上的一个封闭图形。


**polyline** - [[Polyline]]

一条折线，即场景中由多条线段组成的一条线。


**polylineVolume** - [[PolylineVolume]]

具有体积的多段线，定义为沿多段线拉伸的二维形状。


**rectangle** - [[Rectangle]]

符合地球曲率的制图矩形，可以沿表面或高度放置。


**tileset** - [[Tileset]]

3D Tiles 瓦片集。


**wall** - [[Wall]]

符合地球曲率的二维墙，可以沿地表或高处放置。


**agi_conicSensor** - [[ConicSensor]]

考虑到椭圆体（即地球）的遮挡的锥形传感器体积。 使用 `position` 和 `orientation` 属性定位和定向传感器。


**agi_customPatternSensor** - [[CustomPatternSensor]]

考虑到椭圆体（即地球）的遮挡的自定义传感器体积。 使用 `position` 和 `orientation` 属性定位和定向传感器。


**agi_rectangularSensor** - [[RectangularSensor]]

考虑到椭圆体（即地球）的遮挡的矩形金字塔传感器体积。 使用 `position` 和 `orientation` 属性定位和定向传感器。


**agi_fan** - [[Fan]]

定义一个扇形，它从一个点或顶点开始，并从顶点沿指定的方向列表延伸。 每对方向形成延伸到指定半径的扇面。 使用 `position` 和 `orientation` 属性来定位和定向风扇。


**agi_vector** - [[Vector]]

定义一个图形向量，该向量源自 `position` 属性并在提供的方向上延伸提供的长度。 使用 `position` 属性定位向量。


