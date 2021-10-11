<h1 align="center">Laya自定义View</h1>
Laya version 2.x

# 1.编写自定义view
```
export namespace UIbase {
    //自定义view
    export class ItemBase extends Laya.View{
        //.....
    }
}
```
# 2.IDE设置自定义View导入
快捷键：F9

```
import { UIbase } from "../framework/common/base/ItemBase";
import ItemBase = UIbase.ItemBase;
```
![](./img/16339428794585.png)
![](./img/16339429889129.png)

# 3.使用自定义View
![](./img/16339434719553.png)

```
export default class HeroListItem extends ui.view.HeroListItemUI {
    //....
}
```