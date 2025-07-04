---
title: "ServiceWorkerRegistration: getNotifications() method"
short-title: getNotifications()
slug: Web/API/ServiceWorkerRegistration/getNotifications
page-type: web-api-instance-method
browser-compat: api.ServiceWorkerRegistration.getNotifications
---

{{APIRef("Web Notifications")}}{{SecureContext_Header}} {{AvailableInWorkers}}

The **`getNotifications()`** method of
the {{domxref("ServiceWorkerRegistration")}} interface returns a list of the
notifications in the order that they were created from the current origin via the
current service worker registration. Origins can have many active but
differently-scoped service worker registrations. Notifications created by one service
worker on the same origin will not be available to other active service workers on
that same origin.

## Syntax

```js-nolint
getNotifications()
getNotifications(options)
```

### Parameters

- `options` {{optional_inline}}
  - : An object containing options to filter the notifications returned. The available
    options are:
    - `tag` {{optional_inline}}
      - : A string representing a notification tag. If
        specified, only notifications that have this tag will be returned.

### Return value

A {{jsxref("Promise")}} that resolves to a list of {{domxref("Notification")}} objects.

## Examples

```js
navigator.serviceWorker.register("sw.js");

const options = { tag: "user_alerts" };

navigator.serviceWorker.ready.then((registration) => {
  registration.getNotifications(options).then((notifications) => {
    // do something with your notifications
  });
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
