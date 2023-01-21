#Unity笔记



##点击拖动



###sprite可用

sprite无法像UGUI使用接口 OnDrag, OnBeginDrag, OnEndDrag,所以需要使用鼠标点击事件。

鼠标点击事件需要在物体上***挂载组件Collider***才能起效

```c#
//鼠标点下时调用
private void OnMouseDown() {} 

//当鼠标按下左键拖动物体时调用
private void OnMouseDrag() {}

//当鼠标进入物体时调用
private void OnMouseEnter() {}

//当鼠标离开物体时调用
private void OnMouseExit() {}

//当鼠标停留在物体表面时调用
private void OnMouseOver() {}

//鼠标点击抬起时调用
private void OnMouseUp() {}

//像点击按钮一样点击游戏对象，需要点击后鼠标任然还在游戏物体身上才会调用
private void OnMouseUpAsButton() {}
```

###UGUI可用

首先需要导入

```c#
using UnityEngine.EventSystems;
```

然后类需要继承接口

```c#
public class Player : MonoBehaviour,IDragHandler,IBeginDragHandler,IEndDragHandler,IDragAndDropHandler
```

然后就可以在接口方法内写具体的实现

`//开始拖拽`

`public void OnBeginDrag(PointerEventData eventData){}`

`//拖拽中`

`public void OnBeginDrag(PointerEventData eventData)`

`{`

`}`

`//结束拖拽`

`public void OnBeginDrag(PointerEventData eventData){}`