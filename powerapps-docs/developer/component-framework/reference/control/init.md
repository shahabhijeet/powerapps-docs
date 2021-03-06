---
title: "init | MicrosoftDocs"
manager: kvivek
ms.date: 04/23/2019
ms.service: "powerapps"
ms.topic: "reference"
applies_to: ""
ms.assetid: 4485b7d4-c68f-4298-8676-1820eb33c1ad
ms.author: "nabuthuk"
author: Nkrb
---
# init

[!INCLUDE[./includes/init-description.md](./includes/init-description.md)]

## Syntax

`init(context,notifyOutputChanged,state,container)`

## Parameters

| Parameter Name|Type|Required|Description|
| ------------- |----|--------|-----------|
|context|[Context](../context.md)|yes|The *Input Properties* containing the parameters, component metadata and interface functions.|
|notifyOutputChanged|`function`|no|The method to notify the framework that it has new outputs|
|state|`Dictionary`|no|The component state that is saved from *setControlState* in the last session|
|container|[HTMLDivElement](https://developer.mozilla.org/docs/Web/API/HTMLDivElement)|no|The div element to render|

## Example

```JavaScript
MyNameSpace.JSHelloWorldControl.prototype.init = function (context, notifyOutputChanged, state, container) {
	this._labelElement = document.createElement("label");
	this._labelElement.setAttribute("class", "JS_HelloWorldColor");
	container.appendChild(this._labelElement);
};
```

### Related topics

[Control](../control.md)<br/>
[PowerApps component framework API Reference](../../reference/index.md)<br/>
[PowerApps component framework Overview](../../overview.md)
