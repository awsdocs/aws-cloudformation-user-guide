# AWS Rule Functions<a name="intrinsic-function-reference-rules"></a>

In the condition or assertions of a rule, you can use intrinsic functions, such as `Fn::Equals`, `Fn::Not`, and `Fn::RefAll`\. The condition property determines if AWS CloudFormation applies the assertions\. If the condition evaluates to `true`, AWS CloudFormation evaluates the assertions to verify whether a parameter value is valid when a provisioned product is created or updated\. If a parameter value is invalid, AWS CloudFormation does not create or update the stack\. If the condition evaluates to `false`, AWS CloudFormation doesn't check the parameter value and proceeds with the stack operation\.

**Topics**
+ [Fn::And](#fn-and)
+ [Fn::Contains](#fn-contains)
+ [Fn::EachMemberEquals](#fn-eachmemberequals)
+ [Fn::EachMemberIn](#fn-eachmemberin)
+ [Fn::Equals](#fn-equals)
+ [Fn::Not](#fn-not)
+ [Fn::Or](#fn-or)
+ [Fn::RefAll](#fn-refall)
+ [Fn::ValueOf](#fn-valueof)
+ [Fn::ValueOfAll](#fn-valueofall)
+ [Supported Functions](#supported-rule-functions)
+ [Supported Attributes](#rules-parameter-attributes)

## Fn::And<a name="fn-and"></a>

Returns `true` if all the specified conditions evaluate to `true`; returns `false` if any one of the conditions evaluates to `false`\. `Fn::And` acts as an AND operator\. The minimum number of conditions that you can include is two, and the maximum is ten\.

### Declaration<a name="fn-and-declaration"></a>

```
"Fn::And" : [{condition}, {...}]
```

### Parameters<a name="fn-and-parameters"></a>

*condition*  
A rule\-specific intrinsic function that evaluates to `true` or `false`\.

### Example<a name="fn-and-example"></a>

The following example evaluates to `true` if the referenced security group name is equal to `sg-mysggroup` and if the `InstanceType` parameter value is either `m1.large` or `m1.small`:

```
"Fn::And" : [
  {"Fn::Equals" : ["sg-mysggroup", {"Ref" : "ASecurityGroup"}]},
  {"Fn::Contains" : [["m1.large", "m1.small"], {"Ref" : "InstanceType"}]}
]
```

## Fn::Contains<a name="fn-contains"></a>

Returns `true` if a specified string matches at least one value in a list of strings\.

### Declaration<a name="fn-contains-declaration"></a>

```
"Fn::Contains" : [[list_of_strings], string]
```

### Parameters<a name="fn-contains-parameters"></a>

*list\_of\_strings*  
A list of strings, such as `"A", "B", "C"`\.

*string*  
A string, such as `"A"`, that you want to compare against a list of strings\.

### Example<a name="fn-contains-example"></a>

The following function evaluates to `true` if the `InstanceType` parameter value is contained in the list \(`m1.large` or `m1.small`\):

```
"Fn::Contains" : [
  ["m1.large", "m1.small"], {"Ref" : "InstanceType"}
]
```

## Fn::EachMemberEquals<a name="fn-eachmemberequals"></a>

Returns `true` if a specified string matches all values in a list\.

### Declaration<a name="fn-eachmemberequals-declaration"></a>

```
"Fn::EachMemberEquals" : [[list_of_strings], string]
```

### Parameters<a name="fn-eachmemberequals-parameters"></a>

*list\_of\_strings*  
A list of strings, such as `"A", "B", "C"`\.

*string*  
A string, such as `"A"`, that you want to compare against a list of strings\.

### Example<a name="fn-eachmemberequals-example"></a>

The following function returns `true` if the `Department` tag for all parameters of type `AWS::EC2::VPC::Id` have a value of `IT`:

```
"Fn::EachMemberEquals" : [
  {"Fn::ValueOfAll" : ["AWS::EC2::VPC::Id", "Tags.Department"]}, "IT"
]
```

## Fn::EachMemberIn<a name="fn-eachmemberin"></a>

Returns `true` if each member in a list of strings matches at least one value in a second list of strings\.

### Declaration<a name="fn-eachmemberin-declaration"></a>

```
"Fn::EachMemberIn" : [[strings_to_check], [strings_to_match]]
```

### Parameters<a name="fn-eachmemberin-parameters"></a>

*strings\_to\_check*  
A list of strings, such as `"A", "B", "C"`\. AWS CloudFormation checks whether each member in the `strings_to_check` parameter is in the `strings_to_match` parameter\.

*strings\_to\_match*  
A list of strings, such as `"A", "B", "C"`\. Each member in the `strings_to_match` parameter is compared against the members of the `strings_to_check` parameter\.

### Example<a name="fn-eachmemberin-example"></a>

The following function checks whether users specify a subnet that is in a valid virtual private cloud \(VPC\)\. The VPC must be in the account and the region in which users are working with the stack\. The function applies to all parameters of type `AWS::EC2::Subnet::Id`\.

```
"Fn::EachMemberIn" : [ 
  {"Fn::ValueOfAll" : ["AWS::EC2::Subnet::Id", "VpcId"]}, {"Fn::RefAll" : "AWS::EC2::VPC::Id"}
]
```

## Fn::Equals<a name="fn-equals"></a>

Compares two values to determine whether they are equal\. Returns `true` if the two values are equal and `false` if they aren't\.

### Declaration<a name="fn-equals-declaration"></a>

```
"Fn::Equals" : ["value_1", "value_2"]
```

### Parameters<a name="fn-equals-parameters"></a>

*`value`*  
A value of any type that you want to compare with another value\.

### Example<a name="fn-equals-example"></a>

The following example evaluates to `true` if the value for the `EnvironmentType` parameter is equal to `prod`:

```
"Fn::Equals" : [{"Ref" : "EnvironmentType"}, "prod"]
```

## Fn::Not<a name="fn-not"></a>

Returns `true` for a condition that evaluates to `false`, and returns `false` for a condition that evaluates to `true`\. `Fn::Not` acts as a NOT operator\.

### Declaration<a name="fn-not-declaration"></a>

```
"Fn::Not" : [{condition}]
```

### Parameters<a name="fn-not-parameters"></a>

*`condition`*  
A rule\-specific intrinsic function that evaluates to `true` or `false`\.

### Example<a name="fn-not-example"></a>

The following example evaluates to `true` if the value for the `EnvironmentType` parameter is not equal to `prod`:

```
"Fn::Not" : [{"Fn::Equals" : [{"Ref" : "EnvironmentType"}, "prod"]}]
```

## Fn::Or<a name="fn-or"></a>

Returns `true` if any one of the specified conditions evaluates to `true`; returns `false` if all of the conditions evaluate to `false`\. `Fn::Or` acts as an OR operator\. The minimum number of conditions that you can include is two, and the maximum is ten\.

### Declaration<a name="fn-or-declaration"></a>

```
"Fn::Or" : [{condition}, {...}]
```

### Parameters<a name="fn-or-parameters"></a>

*`condition`*  
A rule\-specific intrinsic function that evaluates to `true` or `false`\.

### Example<a name="fn-or-example"></a>

The following example evaluates to `true` if the referenced security group name is equal to `sg-mysggroup` or if the `InstanceType` parameter value is either `m1.large` or `m1.small`:

```
"Fn::Or" : [
  {"Fn::Equals" : ["sg-mysggroup", {"Ref" : "ASecurityGroup"}]},
  {"Fn::Contains" : [["m1.large", "m1.small"], {"Ref" : "InstanceType"}]}
]
```

## Fn::RefAll<a name="fn-refall"></a>

Returns all values for a specified parameter type\.

### Declaration<a name="fn-refall-declaration"></a>

```
"Fn::RefAll" : "parameter_type"
```

### Parameters<a name="fn-refall-parameters"></a>

*parameter\_type*  
An AWS\-specific parameter type, such as `AWS::EC2::SecurityGroup::Id` or `AWS::EC2::VPC::Id`\. For more information, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) in the *AWS CloudFormation User Guide*\.

### Example<a name="fn-refall-example"></a>

The following function returns a list of all VPC IDs for the region and AWS account in which the stack is being created or updated:

```
"Fn::RefAll" : "AWS::EC2::VPC::Id"
```

## Fn::ValueOf<a name="fn-valueof"></a>

Returns an attribute value or list of values for a specific parameter and attribute\.

### Declaration<a name="fn-valueof-declaration"></a>

```
"Fn::ValueOf" : [ "parameter_logical_id", "attribute" ]
```

### Parameters<a name="fn-valueof-parameters"></a>

*attribute*  
The name of an attribute from which you want to retrieve a value\. For more information about attributes, see [Supported Attributes](#rules-parameter-attributes)\.

*parameter\_logical\_id*  
The name of a parameter for which you want to retrieve attribute values\. The parameter must be declared in the `Parameters` section of the template\.

### Examples<a name="fn-valueof-examples"></a>

The following example returns the value of the `Department` tag for the VPC that is specified by the `ElbVpc` parameter:

```
"Fn::ValueOf" : ["ElbVpc", "Tags.Department"]
```

If you specify multiple values for a parameter, the Fn::ValueOf function can return a list\. For example, you can specify multiple subnets and get a list of Availability Zones where each member is the Avalibility Zone of a particular subnet:

```
"Fn::ValueOf" : ["ListOfElbSubnets", "AvailabilityZone"]
```

## Fn::ValueOfAll<a name="fn-valueofall"></a>

Returns a list of all attribute values for a given parameter type and attribute\.

### Declaration<a name="fn-valueofall-declaration"></a>

```
"Fn::ValueOfAll" : ["parameter_type", "attribute"]
```

### Parameters<a name="fn-valueofall-parameters"></a>

*attribute*  
The name of an attribute from which you want to retrieve a value\. For more information about attributes, see [Supported Attributes](#rules-parameter-attributes)\.

*parameter\_type*  
An AWS\-specific parameter type, such as AWS::EC2::SecurityGroup::Id or AWS::EC2::VPC::Id\. For more information, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html) in the *AWS CloudFormation User Guide*\.

### Example<a name="fn-valueofall-example"></a>

In the following example, the `Fn::ValueOfAll` function returns a list of values, where each member is the `Department` tag value for VPCs with that tag:

```
"Fn::ValueOfAll" : ["AWS::EC2::VPC::Id", "Tags.Department"]
```

## Supported Functions<a name="supported-rule-functions"></a>

You cannot use another function within the `Fn::ValueOf` and `Fn::ValueOfAll` functions\. However, you can use the following functions within all other rule\-specific intrinsic functions:
+ `Ref`
+ Other rule\-specific intrinsic functions

## Supported Attributes<a name="rules-parameter-attributes"></a>

The following list describes the attribute values that you can retrieve for specific resources and parameter types:

The `AWS::EC2::VPC::Id` parameter type or VPC IDs  
+ DefaultNetworkAcl
+ DefaultSecurityGroup
+ Tags\.*tag\_key*

The `AWS::EC2::Subnet::Id` parameter type or subnet IDs  
+ AvailabilityZone
+ Tags\.*tag\_key*
+ VpcId

The `AWS::EC2::SecurityGroup::Id` parameter type or security group IDs  
+ Tags\.*tag\_key*