---
title: Declaration Nodes
slug: 0.0.1/reference/schemas/declarations
---

## `AttributeDeclarationNode` *(extends `DeclarationNode`)*

*kind discriminant: `"AttributeDeclaration"`*

| Field | Type |
|---|---|
| `attributes` | `Attribute[]` |

***

## `TemplateNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Template"`*

| Field | Type |
|---|---|
| `parameters` | `TemplateParameter[]` |
| `requiresClause` | `Node?` |

***

## `NamespaceNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Namespace"`*

| Field | Type |
|---|---|
| `segments` | `NamespaceSegment[]` |
| `isAnonymous` | `boolean` |
| `isInline` | `boolean` |
| `children` | `Node[]` |

***

## `UsingNamespaceNode` *(extends `DeclarationNode`)*

*kind discriminant: `"UsingNamespace"`*

| Field | Type |
|---|---|
| `identifier` | `IdentifierNode?` |

***

## `StaticAssertNode` *(extends `DeclarationNode`)*

*kind discriminant: `"StaticAssert"`*

| Field | Type |
|---|---|
| `condition` | `Node?` |
| `message` | `string` |

***

## `NamespaceAliasNode` *(extends `DeclarationNode`)*

*kind discriminant: `"NamespaceAlias"`*

| Field | Type |
|---|---|
| `aliasName` | `string` |
| `targetNamespace` | `IdentifierNode?` |

***

## `TypedefNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Typedef"`*

| Field | Type |
|---|---|
| `aliasName` | `string` |
| `typeDecl` | `DeclarationNode?` |
| `targetType` | `TypeSignature?` |

***

## `TypeAliasNode` *(extends `DeclarationNode`)*

*kind discriminant: `"TypeAlias"`*

| Field | Type |
|---|---|
| `aliasName` | `string` |
| `targetType` | `TypeSignature` |
| `templateDecl` | `Node?` |

***

## `UsingDeclarationNode` *(extends `DeclarationNode`)*

*kind discriminant: `"UsingDeclaration"`*

| Field | Type |
|---|---|
| `aliasName` | `string` |
| `targetType` | `TypeSignature` |

***

## `EnumNode` *(extends `DeclarationNode`)*

*kind discriminant: `"EnumeratorSpecifier"`*

| Field | Type |
|---|---|
| `identifier` | `IdentifierNode?` |
| `underlyingType` | `TypeSignature` |
| `isScoped` | `boolean` |
| `isForwardDeclaration` | `boolean` |
| `enumerators` | `Node[]` |

***

## `EnumSpecifierNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Enumerator"`*

| Field | Type |
|---|---|
| `name` | `string` |
| `value` | `Node?` |

***

## `VariableNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Variable"`*

| Field | Type |
|---|---|
| `isStatic` | `boolean` |
| `isConstexpr` | `boolean` |
| `isThreadLocal` | `boolean` |
| `isInline` | `boolean` |
| `isExtern` | `boolean` |
| `isConstinit` | `boolean` |
| `attributes` | `Attribute[]` |
| `alignasExprs` | `string[]` |
| `typeSignature` | `TypeSignature` |
| `identifier` | `IdentifierNode?` |
| `defaultValue` | `Node?` |

***

## `VariableGroupNode` *(extends `DeclarationNode`)*

*kind discriminant: `"VariableGroup"`*

| Field | Type |
|---|---|
| `variables` | `VariableNode[]` |

***

## `StructuredBindingNode` *(extends `DeclarationNode`)*

*kind discriminant: `"StructuredBinding"`*

| Field | Type |
|---|---|
| `names` | `string[]` |
| `typeSignature` | `TypeSignature` |
| `initializer` | `Node?` |
| `isStatic` | `boolean` |
| `isConstexpr` | `boolean` |
| `isConstinit` | `boolean` |
| `isThreadLocal` | `boolean` |
| `isInline` | `boolean` |

***

## `ConceptNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Concept"`*

| Field | Type |
|---|---|
| `identifier` | `IdentifierNode?` |
| `constraintExpr` | `Node?` |
| `templateDecl` | `Node?` |

***

## `FunctionNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Function"`*

| Field | Type |
|---|---|
| `isStatic` | `boolean` |
| `isConst` | `boolean` |
| `isVolatile` | `boolean` |
| `isVirtual` | `boolean` |
| `isPureVirtual` | `boolean` |
| `isOverride` | `boolean` |
| `isNoexcept` | `boolean` |
| `noexceptCondition` | `Node?` |
| `isFinal` | `boolean` |
| `isInline` | `boolean` |
| `isConstexpr` | `boolean` |
| `isConsteval` | `boolean` |
| `isExplicit` | `boolean` |
| `explicitCondition` | `Node?` |
| `isDefaulted` | `boolean` |
| `isDeleted` | `boolean` |
| `isTrailingReturn` | `boolean` |
| `refQualifier` | `RefQualifier` |
| `requiresClause` | `Node?` |
| `body` | `BlockNode?` |
| `attributes` | `Attribute[]` |
| `returnSignature` | `TypeSignature` |
| `identifier` | `IdentifierNode?` |
| `parameters` | `FunctionParameter[]` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |

***

## `ConstructorNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Constructor"`*

| Field | Type |
|---|---|
| `isExplicit` | `boolean` |
| `explicitCondition` | `Node?` |
| `isNoexcept` | `boolean` |
| `noexceptCondition` | `Node?` |
| `isDefaulted` | `boolean` |
| `isDeleted` | `boolean` |
| `isConstexpr` | `boolean` |
| `isInline` | `boolean` |
| `isCopyConstructor` | `boolean` |
| `isMoveConstructor` | `boolean` |
| `requiresClause` | `Node?` |
| `body` | `BlockNode?` |
| `attributes` | `Attribute[]` |
| `identifier` | `IdentifierNode?` |
| `parameters` | `FunctionParameter[]` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |

***

## `DestructorNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Destructor"`*

| Field | Type |
|---|---|
| `isVirtual` | `boolean` |
| `isPureVirtual` | `boolean` |
| `isDefaulted` | `boolean` |
| `isDeleted` | `boolean` |
| `isNoexcept` | `boolean` |
| `noexceptCondition` | `Node?` |
| `isInline` | `boolean` |
| `isConstexpr` | `boolean` |
| `requiresClause` | `Node?` |
| `body` | `BlockNode?` |
| `attributes` | `Attribute[]` |
| `identifier` | `IdentifierNode?` |

***

## `OperatorNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Operator"`*

| Field | Type |
|---|---|
| `isStatic` | `boolean` |
| `isConst` | `boolean` |
| `isVolatile` | `boolean` |
| `isVirtual` | `boolean` |
| `isPureVirtual` | `boolean` |
| `isOverride` | `boolean` |
| `isNoexcept` | `boolean` |
| `noexceptCondition` | `Node?` |
| `isFinal` | `boolean` |
| `isInline` | `boolean` |
| `isConstexpr` | `boolean` |
| `isExplicit` | `boolean` |
| `explicitCondition` | `Node?` |
| `isDefaulted` | `boolean` |
| `isDeleted` | `boolean` |
| `isTrailingReturn` | `boolean` |
| `refQualifier` | `RefQualifier` |
| `requiresClause` | `Node?` |
| `body` | `BlockNode?` |
| `attributes` | `Attribute[]` |
| `operatorSymbol` | `string` |
| `returnSignature` | `TypeSignature` |
| `castTargetType` | `TypeSignature` |
| `parameters` | `FunctionParameter[]` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |

***

## `UnionNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Union"`*

| Field | Type |
|---|---|
| `isAnonymous` | `boolean` |
| `isForwardDeclaration` | `boolean` |
| `attributes` | `Attribute[]` |
| `alignasExprs` | `string[]` |
| `identifier` | `IdentifierNode?` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |
| `memberVariables` | `Node[]` |
| `memberFunctions` | `Node[]` |
| `staticMemberVariables` | `Node[]` |
| `staticMemberFunctions` | `Node[]` |
| `constructors` | `Node[]` |
| `destructors` | `Node[]` |
| `operators` | `Node[]` |
| `nestedTypes` | `Node[]` |

***

## `FriendNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Friend"`*

| Field | Type |
|---|---|
| `kind` | `string` |
| `identifier` | `IdentifierNode?` |

***

## `StructNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Struct"`*

| Field | Type |
|---|---|
| `isFinal` | `boolean` |
| `isForwardDeclaration` | `boolean` |
| `attributes` | `Attribute[]` |
| `alignasExprs` | `string[]` |
| `identifier` | `IdentifierNode?` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |
| `baseClasses` | `[?, IdentifierNode][]` |
| `derivedClasses` | `string[]` |
| `memberVariables` | `Node[]` |
| `memberFunctions` | `Node[]` |
| `staticMemberVariables` | `Node[]` |
| `staticMemberFunctions` | `Node[]` |
| `constructors` | `Node[]` |
| `destructors` | `Node[]` |
| `operators` | `Node[]` |
| `friends` | `Node[]` |
| `nestedTypes` | `Node[]` |
| `statements` | `Node[]` |

***

## `ClassNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Class"`*

| Field | Type |
|---|---|
| `isFinal` | `boolean` |
| `isForwardDeclaration` | `boolean` |
| `attributes` | `Attribute[]` |
| `alignasExprs` | `string[]` |
| `identifier` | `IdentifierNode?` |
| `templateDecl` | `Node?` |
| `templateArgs` | `TemplateArgument[]` |
| `baseClasses` | `[?, IdentifierNode][]` |
| `derivedClasses` | `string[]` |
| `memberVariables` | `[?, Node][]` |
| `memberFunctions` | `[?, Node][]` |
| `staticMemberVariables` | `[?, Node][]` |
| `staticMemberFunctions` | `[?, Node][]` |
| `constructors` | `[?, Node][]` |
| `destructors` | `[?, Node][]` |
| `operators` | `[?, Node][]` |
| `friends` | `[?, Node][]` |
| `nestedTypes` | `[?, Node][]` |
| `statements` | `Node[]` |

***

## `ModuleNode` *(extends `DeclarationNode`)*

*kind discriminant: `"Module"`*

| Field | Type |
|---|---|
| `moduleName` | `string` |
| `partition` | `string` |
| `isExported` | `boolean` |
| `isGlobalFragment` | `boolean` |
| `isPrivateFragment` | `boolean` |
| `children` | `Node[]` |

***

## `ModuleImportNode` *(extends `DeclarationNode`)*

*kind discriminant: `"ModuleImport"`*

| Field | Type |
|---|---|
| `moduleName` | `string` |
| `partition` | `string` |
| `header` | `string` |
| `isSystem` | `boolean` |
| `isExported` | `boolean` |

***

## `ExternCNode` *(extends `DeclarationNode`)*

*kind discriminant: `"ExternC"`*

| Field | Type |
|---|---|
| `language` | `string` |
| `isBlock` | `boolean` |
| `children` | `Node[]` |

***

## `ExportDeclarationNode` *(extends `DeclarationNode`)*

*kind discriminant: `"ExportDeclaration"`*

| Field | Type |
|---|---|
| `children` | `Node[]` |

***
