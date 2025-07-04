---
title: name
slug: Web/XML/XPath/Reference/Functions/name
page-type: xpath-function
sidebar: xmlsidebar
---

The `name` function returns a string representing the QName of the first node in a given node-set.

## Syntax

```plain
name( [node-set] )
```

### Parameters

- `node-set` (optional)
  - : The QName of the first node in this node-set will be returned. If this argument is omitted, the current context node will be used.

### Return value

A string representing the QName of a node.

## Description

- The [QName](https://www.w3.org/TR/xml-names/#NT-QName) is the node's qualified name, including its namespace prefix and its local name.

## Specifications

[XPath 1.0 4.1](https://www.w3.org/TR/xpath-10/#function-local-name)

## Gecko support

Supported.
