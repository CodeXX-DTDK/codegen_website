---
title: Statement Nodes
slug: 0.0.1/reference/schemas/statements
---

## `BlockNode` *(extends `StatementNode`)*

*kind discriminant: `"Block"`*

| Field | Type |
|---|---|
| `statements` | `Node[]` |

***

## `IfNode` *(extends `StatementNode`)*

*kind discriminant: `"IfStatement"`*

| Field | Type |
|---|---|
| `isConstexpr` | `boolean` |
| `initStatement` | `Node?` |
| `condition` | `Node?` |
| `thenBody` | `BlockNode?` |
| `elseBody` | `Node?` |

***

## `SwitchNode` *(extends `StatementNode`)*

*kind discriminant: `"SwitchStatement"`*

| Field | Type |
|---|---|
| `initStatement` | `Node?` |
| `condition` | `Node?` |
| `cases` | `Node[]` |

***

## `CaseLabelNode` *(extends `StatementNode`)*

*kind discriminant: `"CaseLabel"`*

| Field | Type |
|---|---|
| `value` | `Node?` |
| `statements` | `Node[]` |

***

## `BreakNode` *(extends `StatementNode`)*

*kind discriminant: `"BreakStatement"`*

*No own serialized fields.*

***

## `ContinueNode` *(extends `StatementNode`)*

*kind discriminant: `"ContinueStatement"`*

*No own serialized fields.*

***

## `ReturnNode` *(extends `StatementNode`)*

*kind discriminant: `"ReturnStatement"`*

| Field | Type |
|---|---|
| `value` | `Node?` |

***

## `GotoNode` *(extends `StatementNode`)*

*kind discriminant: `"GotoStatement"`*

| Field | Type |
|---|---|
| `label` | `string` |

***

## `LabeledStatementNode` *(extends `StatementNode`)*

*kind discriminant: `"LabeledStatement"`*

| Field | Type |
|---|---|
| `label` | `string` |
| `body` | `Node?` |

***

## `DefaultLabelNode` *(extends `StatementNode`)*

*kind discriminant: `"DefaultLabel"`*

| Field | Type |
|---|---|
| `statements` | `Node[]` |

***

## `WhileNode` *(extends `StatementNode`)*

*kind discriminant: `"WhileStatement"`*

| Field | Type |
|---|---|
| `initStatement` | `Node?` |
| `condition` | `Node?` |
| `body` | `BlockNode?` |

***

## `DoWhileNode` *(extends `StatementNode`)*

*kind discriminant: `"DoWhileStatement"`*

| Field | Type |
|---|---|
| `condition` | `Node?` |
| `body` | `BlockNode?` |

***

## `ForNode` *(extends `StatementNode`)*

*kind discriminant: `"ForStatement"`*

| Field | Type |
|---|---|
| `init` | `Node?` |
| `condition` | `Node?` |
| `update` | `Node?` |
| `body` | `BlockNode?` |

***

## `ForRangeNode` *(extends `StatementNode`)*

*kind discriminant: `"ForRangeStatement"`*

| Field | Type |
|---|---|
| `initStatement` | `Node?` |
| `loopVar` | `Node?` |
| `range` | `Node?` |
| `body` | `BlockNode?` |

***

## `CatchClauseNode` *(extends `StatementNode`)*

*kind discriminant: `"CatchClause"`*

| Field | Type |
|---|---|
| `isCatchAll` | `boolean` |
| `parameter` | `Node?` |
| `body` | `BlockNode?` |

***

## `TryNode` *(extends `StatementNode`)*

*kind discriminant: `"TryStatement"`*

| Field | Type |
|---|---|
| `body` | `BlockNode?` |
| `catchClauses` | `CatchClauseNode[]` |

***
