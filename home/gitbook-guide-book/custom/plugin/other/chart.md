---
description: gitbook 使用 `C3.js` 或者 `Highcharts` 绘制图形 插件, gitbook-plugin-chart 使用教程
---
# Chart

Gitbook 插件：使用 `C3.js` 或者 `Highcharts` 绘制图形。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-chart

[https://github.com/csbun/gitbook-plugin-chart](https://github.com/csbun/gitbook-plugin-chart)
 
- C3.js：`https://github.com/c3js/c3`

- highcharts：`https://github.com/highcharts/highcharts`

```json
{
    "plugins": [ "chart" ],
    "pluginsConfig": {
        "chart": {
            "type": "c3"
        }
    }
}
```
type 可以是 `c3` 或者 `highcharts`, 默认是 `c3`.

#### 举几个例子

##### JSON 格式的数据

```json
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
```

效果如下所示：

{% chart %}
{
    "data": {
        "type": "bar",
        "columns": [
            ["data1", 30, 200, 100, 400, 150, 250],
            ["data2", 50, 20, 10, 40, 15, 25]
        ],
        "axes": {
            "data2": "y2"
        }
    },
    "axis": {
        "y2": {
            "show": true
        }
    }
}
{% endchart %}

##### YAML 格式的数据

```yaml
data:
    columns:
        - [data1, 30, 200, 100, 400, 150, 250]
        - [data2, 50, 20, 10, 40, 15, 25]
    axes:
        data2: y2
axis:
    y2:
        show: true
```

效果如下所示：

{% chart format="yaml" %}
data:
    columns:
        - [data1, 30, 200, 100, 400, 150, 250]
        - [data2, 50, 20, 10, 40, 15, 25]
    axes:
        data2: y2
axis:
    y2:
        show: true
{% endchart %}



> [!WARNING|style:callout|iconVisibility:hidden|label:注意]
> 如果页面内容显示不完整，请F5刷新当前页面