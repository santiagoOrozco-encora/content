---
title: "GPUExternalTexture: label property"
short-title: label
slug: Web/API/GPUExternalTexture/label
page-type: web-api-instance-property
browser-compat: api.GPUExternalTexture.label
---

{{APIRef("WebGPU API")}}{{SecureContext_Header}}{{AvailableInWorkers}}

The **`label`** property of the
{{domxref("GPUExternalTexture")}} interface provides a label that can be used to identify the object, for example in {{domxref("GPUError")}} messages or console warnings.

This can be set by providing a `label` property in the descriptor object passed into the originating {{domxref("GPUDevice.importExternalTexture()")}} call, or you can get and set it directly on the `GPUExternalTexture` object.

## Value

A string. If this has not been previously set as described above, it will be an empty string.

## Examples

Setting and getting a label via `GPUExternalTexture.label`:

```js
// …

const externalTexture = device.importExternalTexture({
  source: video,
});

externalTexture.label = "my_ext_texture";

console.log(externalTexture.label); // "my_ext_texture"
```

Setting a label via the originating {{domxref("GPUDevice.importExternalTexture()")}} call, and then getting it via `GPUExternalTexture.label`:

```js
// …

const externalTexture = device.importExternalTexture({
  source: video,
  label: "my_ext_texture",
});

console.log(externalTexture.label); //  "my_ext_texture"
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- The [WebGPU API](/en-US/docs/Web/API/WebGPU_API)
