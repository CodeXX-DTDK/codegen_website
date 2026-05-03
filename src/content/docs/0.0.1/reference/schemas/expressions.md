---
title: Expression Nodes
slug: 0.0.1/reference/schemas/expressions
---

## `LiteralNode` *(extends `ExpressionNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `udlSuffix` | `string` |

***

## `NumberLiteralNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `base` | `NumberBase` |
| `category` | `NumberCategory` |
| `value` | `string` |
| `suffix` | `string` |

***

## `StringLiteralNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `encoding` | `StringEncoding` |
| `isRaw` | `boolean` |
| `isMultiLine` | `boolean` |
| `value` | `string` |

***

## `ConcatenatedStringNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `parts` | `LiteralNode[]` |

***

## `CharLiteralNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `encoding` | `StringEncoding` |
| `value` | `string` |

***

## `BoolLiteralNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

| Field | Type |
|---|---|
| `value` | `boolean` |

***

## `NullptrLiteralNode` *(extends `LiteralNode`)*

*kind discriminant: `"Literal"`*

*No own serialized fields.*

***

## `PointerExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"PointerExpression"`*

| Field | Type |
|---|---|
| `op` | `PointerExprOp` |
| `operand` | `Node?` |

***

## `FieldExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"FieldExpression"`*

| Field | Type |
|---|---|
| `object` | `Node?` |
| `op` | `FieldAccessOp` |
| `member` | `string` |

***

## `SubscriptExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"SubscriptExpression"`*

| Field | Type |
|---|---|
| `object` | `Node?` |
| `index` | `Node?` |

***

## `ParenthesizedExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"ParenthesizedExpression"`*

| Field | Type |
|---|---|
| `inner` | `Node?` |

***

## `UnaryExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"UnaryExpression"`*

| Field | Type |
|---|---|
| `op` | `string` |
| `operand` | `Node?` |

***

## `BinaryExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"BinaryExpression"`*

| Field | Type |
|---|---|
| `lhs` | `Node?` |
| `op` | `string` |
| `rhs` | `Node?` |

***

## `UpdateExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"UpdateExpression"`*

| Field | Type |
|---|---|
| `op` | `string` |
| `isPrefix` | `boolean` |
| `operand` | `Node?` |

***

## `NewExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"NewExpression"`*

| Field | Type |
|---|---|
| `typeSignature` | `TypeSignature` |
| `isArray` | `boolean` |
| `arraySize` | `Node?` |
| `placementArgs` | `Node[]` |
| `constructorArgs` | `Node[]` |

***

## `DeleteExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"DeleteExpression"`*

| Field | Type |
|---|---|
| `isArray` | `boolean` |
| `operand` | `Node?` |

***

## `CastExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"CastExpression"`*

| Field | Type |
|---|---|
| `castKind` | `CastKind` |
| `targetType` | `TypeSignature` |
| `operand` | `Node?` |

***

## `IntrospectionExpressionNode` *(extends `ExpressionNode`)*

| Field | Type |
|---|---|
| `isTypeForm` | `boolean` |
| `typeOperand` | `TypeSignature` |
| `exprOperand` | `Node?` |

***

## `SizeofExpressionNode` *(extends `IntrospectionExpressionNode`)*

*kind discriminant: `"SizeofExpression"`*

*No own serialized fields.*

***

## `AlignofExpressionNode` *(extends `IntrospectionExpressionNode`)*

*kind discriminant: `"AlignofExpression"`*

*No own serialized fields.*

***

## `TypeidExpressionNode` *(extends `IntrospectionExpressionNode`)*

*kind discriminant: `"TypeidExpression"`*

*No own serialized fields.*

***

## `DecltypeExpressionNode` *(extends `IntrospectionExpressionNode`)*

*kind discriminant: `"DecltypeExpression"`*

*No own serialized fields.*

***

## `CallExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"CallExpression"`*

| Field | Type |
|---|---|
| `callKind` | `CallKind` |
| `callee` | `Node?` |
| `calleeIdentifier` | `IdentifierNode?` |
| `args` | `FunctionArgument[]` |

***

## `AssignmentExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"AssignmentExpression"`*

| Field | Type |
|---|---|
| `lhs` | `Node?` |
| `op` | `string` |
| `rhs` | `Node?` |

***

## `ConditionalExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"ConditionalExpression"`*

| Field | Type |
|---|---|
| `condition` | `Node?` |
| `thenExpr` | `Node?` |
| `elseExpr` | `Node?` |

***

## `LambdaExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"LambdaExpression"`*

| Field | Type |
|---|---|
| `captureDefault` | `number` |
| `captures` | `LambdaCaptureItem[]` |
| `templateParameters` | `TemplateParameter[]` |
| `parameters` | `FunctionParameter[]` |
| `trailingReturn` | `TypeSignature` |
| `isMutable` | `boolean` |
| `isNoexcept` | `boolean` |
| `noexceptCondition` | `Node?` |
| `body` | `BlockNode?` |

***

## `InitializerListNode` *(extends `ExpressionNode`)*

*kind discriminant: `"InitializerList"`*

| Field | Type |
|---|---|
| `elements` | `Node[]` |

***

## `FoldExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"FoldExpression"`*

| Field | Type |
|---|---|
| `op` | `string` |
| `leftOperand` | `Node?` |
| `rightOperand` | `Node?` |

***

## `ThrowExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"ThrowExpression"`*

| Field | Type |
|---|---|
| `operand` | `Node?` |

***

## `NoexceptExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"NoexceptExpression"`*

| Field | Type |
|---|---|
| `operand` | `Node?` |

***

## `ThisExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"ThisExpression"`*

*No own serialized fields.*

***

## `CoYieldExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"CoYieldExpression"`*

| Field | Type |
|---|---|
| `operand` | `Node?` |

***

## `CoAwaitExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"CoAwaitExpression"`*

| Field | Type |
|---|---|
| `operand` | `Node?` |

***

## `CommaExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"CommaExpression"`*

| Field | Type |
|---|---|
| `lhs` | `Node?` |
| `rhs` | `Node?` |

***

## `RequirementNode` *(extends `Node`)*

*No own serialized fields.*

***

## `SimpleRequirementNode` *(extends `RequirementNode`)*

*kind discriminant: `"SimpleRequirement"`*

| Field | Type |
|---|---|
| `expression` | `Node?` |

***

## `TypeRequirementNode` *(extends `RequirementNode`)*

*kind discriminant: `"TypeRequirement"`*

| Field | Type |
|---|---|
| `typeName` | `TypeSignature` |

***

## `CompoundRequirementNode` *(extends `RequirementNode`)*

*kind discriminant: `"CompoundRequirement"`*

| Field | Type |
|---|---|
| `expression` | `Node?` |
| `isNoexcept` | `boolean` |
| `returnTypeConstraint` | `TypeSignature` |

***

## `RequiresExpressionNode` *(extends `ExpressionNode`)*

*kind discriminant: `"RequiresExpression"`*

| Field | Type |
|---|---|
| `parameters` | `FunctionParameter[]` |
| `requirements` | `RequirementNode[]` |

***
