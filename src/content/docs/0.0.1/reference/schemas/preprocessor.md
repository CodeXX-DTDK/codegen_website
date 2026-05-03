---
title: Preprocessor Nodes
slug: 0.0.1/reference/schemas/preprocessor
---

## `IncludeNode` *(extends `PreprocessorNode`)*

*kind discriminant: `"IncludeDirective"`*

| Field | Type |
|---|---|
| `path` | `string` |
| `isSystem` | `boolean` |

***

## `ObjectLikeMacroNode` *(extends `PreprocessorNode`)*

*kind discriminant: `"ObjectLikeMacro"`*

| Field | Type |
|---|---|
| `name` | `string` |
| `body` | `string` |

***

## `FunctionLikeMacroNode` *(extends `PreprocessorNode`)*

*kind discriminant: `"FunctionLikeMacro"`*

| Field | Type |
|---|---|
| `name` | `string` |
| `body` | `string` |
| `parameters` | `MacroParameter[]` |

***

## `PragmaNode` *(extends `PreprocessorNode`)*

*kind discriminant: `"Pragma"`*

| Field | Type |
|---|---|
| `pragmaKind` | `Unknown` |
| `rawArg` | `string` |
| `packAction` | `string` |
| `packAlignment` | `number` |
| `packLabel` | `string` |
| `warningAction` | `string` |
| `warningCodes` | `number[]` |
| `messageText` | `string` |
| `regionName` | `string` |
| `stdcSetting` | `string` |
| `stdcValue` | `string` |
| `commentType` | `string` |
| `commentValue` | `string` |

***
