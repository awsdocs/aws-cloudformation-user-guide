# `Fn::ForEach`<a name="intrinsic-function-reference-foreach"></a>

The `Fn::ForEach` intrinsic function takes a collection and a fragment, and applies the items in the collection to the identifier in the provided fragment\. `Fn::ForEach` can contain other intrinsic functions, including `Fn::ForEach` itself, and be used within the [Conditions](conditions-section-structure.md), [Outputs](outputs-section-structure.md), [Resources](resources-section-structure.md) \(including the resource properties\) sections\. It cannot be used in the [Format version](format-version-structure.md), [Description](template-description-structure.md), [Metadata](metadata-section-structure.md), [Transform](transform-section-structure.md), [Parameters](parameters-section-structure.md), [Mappings](mappings-section-structure.md), [Rules](rules-section-structure.md), or `Hooks` sections\. For examples, see [Examples](intrinsic-function-reference-foreach-examples.md)\.

**Important**  
You must use the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) to use the `Fn::ForEach` intrinsic function\.

**Important**  
Using the `Fn::ForEach` intrinsic function does not change the quotas, which apply to the resultant template\. Quotas include the maximum size of a template and the maximum number of resources in a template\. For more information, see [AWS CloudFormation quotas](cloudformation-limits.md)\.

## Declaration<a name="intrinsic-function-reference-foreach-declaration"></a>

### JSON<a name="intrinsic-function-reference-foreach-declaration.json"></a>

```
"Fn::ForEach::UniqueLoopName": [
  "Identifier",
  ["Value1","Value2"] // Collection
  {"OutputKey": {OutputValue}}
]
```

### YAML<a name="intrinsic-function-reference-foreach-declaration.yaml"></a>

```
'Fn::ForEach::UniqueLoopName':
    - Identifier
    - - Value1 # Collection
      - Value2
    - 'OutputKey':
        OutputValue
```

## Parameters<a name="intrinsic-function-reference-foreach-parameters"></a>

*`UniqueLoopName`*  
A name for this loop\. The name must be unique within the template and cannot conflict with any logical ID values in the [Resources](resources-section-structure.md) section of the template\. This name is not in the transformed output\.

*`Identifier`*  
The identifier you want to replace in the `OutputKey` and `OutputValue ` parameters that represent the template fragment that is replicated\. All instances of *$\{Identifier\}* in the `OutputKey` and `OutputValue ` parameters are replaced with the values from the `Collection` parameter\.

*`Collection`*  
The collection of values to iterate over\. This can be an array in this parameter, or it can be a ``Ref`` to a `CommaDelimitedList`\.

*`OutputKey`*  
The key in the transformed template\. *$\{Identifier\}* must be included within the `OutputKey` parameter\. For example, if `Fn::ForEach` is used in the [Resources](resources-section-structure.md) section of the template, this is the logical Id of each resource\.

*`OutputValue`*  
The value that is replicated in the transformed template for each item in the `Collection` parameter\. For example, if `Fn::ForEach` is used in the [Resources](resources-section-structure.md) section of the template, this is the template fragment that is repeated to configure each resource\.

## Return value<a name="intrinsic-function-reference-foreach-return-value"></a>

An expanded object that contains the object fragment repeated once for each item in the collection, where the identifier in the fragment is replaced with the item from the collection\. 

## Supported functions<a name="intrinsic-function-reference-foreach-nested-functions"></a>

You can use the following functions within `Fn::ForEach`\.
+ Condition functions:
  + ``Fn::And``
  + ``Fn::Equals``
  + ``Fn::If``
  + ``Fn::Not``
  + ``Fn::Or``
+ ``Fn::Base64``
+ ``Fn::FindInMap``
+ ``Fn::GetAtt``
+ ``Fn::GetAZs``
+ ``Fn::ImportValue``
+ ``Fn::Join``
+ ``Fn::Length``
+ ``Fn::Transform``
+ ``Fn::Select``
+ ``Fn::Sub``
+ ``Fn::ToJsonString``
+ ``Ref``