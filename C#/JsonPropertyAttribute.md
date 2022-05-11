## 序列化时改名称
``` C#
using System.Text.Json.Serialization;
public class Map
{
    [JsonProperty("id")]
    public Guid ID { get; set; }
}
```
``` C#
using Newtonsoft.Json;
Map map = new Map();
var jsonStr = JsonConvert.SerializeObject(map);
// jsonStr 里面包含的 json 数据显示的名称是指定名称
```
> 一版用于大小写转化 也可以用于换名字