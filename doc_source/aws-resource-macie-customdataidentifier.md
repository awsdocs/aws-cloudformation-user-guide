# AWS::Macie::CustomDataIdentifier<a name="aws-resource-macie-customdataidentifier"></a>

The `AWS::Macie::CustomDataIdentifier` resource specifies a custom data identifier\. A *custom data identifier* is a set of custom criteria for Amazon Macie to use when it inspects data sources for sensitive data\. The criteria consist of a regular expression \(*regex*\) that defines a text pattern to match and, optionally, character sequences and a proximity rule that refine the results\. The character sequences can be:
+ *Keywords*, which are words or phrases that must be in proximity of text that matches the regex, or
+ *Ignore words*, which are words or phrases to exclude from the results\.

By using custom data identifiers, you can supplement the managed data identifiers that Macie provides and detect sensitive data that reflects your particular scenarios, intellectual property, or proprietary data\. For more information, see [Building custom data identifiers](https://docs.aws.amazon.com/macie/latest/user/custom-data-identifiers.html) in the *Amazon Macie User Guide*\.

An `AWS::Macie::Session` resource must exist for an AWS account before you can create an `AWS::Macie::CustomDataIdentifier` resource for the account\. Use a [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to ensure that an `AWS::Macie::Session` resource is created before other Macie resources are created for an account\. For example, `"DependsOn": "Session"`\.

## Syntax<a name="aws-resource-macie-customdataidentifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-macie-customdataidentifier-syntax.json"></a>

```
{
  "Type" : "AWS::Macie::CustomDataIdentifier",
  "Properties" : {
      "[Description](#cfn-macie-customdataidentifier-description)" : String,
      "[IgnoreWords](#cfn-macie-customdataidentifier-ignorewords)" : [ String, ... ],
      "[Keywords](#cfn-macie-customdataidentifier-keywords)" : [ String, ... ],
      "[MaximumMatchDistance](#cfn-macie-customdataidentifier-maximummatchdistance)" : Integer,
      "[Name](#cfn-macie-customdataidentifier-name)" : String,
      "[Regex](#cfn-macie-customdataidentifier-regex)" : String
    }
}
```

### YAML<a name="aws-resource-macie-customdataidentifier-syntax.yaml"></a>

```
Type: AWS::Macie::CustomDataIdentifier
Properties: 
  [Description](#cfn-macie-customdataidentifier-description): String
  [IgnoreWords](#cfn-macie-customdataidentifier-ignorewords): 
    - String
  [Keywords](#cfn-macie-customdataidentifier-keywords): 
    - String
  [MaximumMatchDistance](#cfn-macie-customdataidentifier-maximummatchdistance): Integer
  [Name](#cfn-macie-customdataidentifier-name): String
  [Regex](#cfn-macie-customdataidentifier-regex): String
```

## Properties<a name="aws-resource-macie-customdataidentifier-properties"></a>

`Description`  <a name="cfn-macie-customdataidentifier-description"></a>
A custom description of the custom data identifier\. The description can contain 1\-512 characters\.  
Avoid including sensitive data in the description\. Users of the account might be able to see the description, depending on the actions that they're allowed to perform in Amazon Macie\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IgnoreWords`  <a name="cfn-macie-customdataidentifier-ignorewords"></a>
An array of character sequences \(*ignore words*\) to exclude from the results\. If text matches the regular expression \(`Regex`\) but it contains a string in this array, Amazon Macie ignores the text and doesn't include it in the results\.  
The array can contain 1\-10 ignore words\. Each ignore word can contain 4\-90 UTF\-8 characters\. Ignore words are case sensitive\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Keywords`  <a name="cfn-macie-customdataidentifier-keywords"></a>
An array of character sequences \(*keywords*\), one of which must precede and be in proximity \(`MaximumMatchDistance`\) of the regular expression \(`Regex`\) to match\.  
The array can contain 1\-50 keywords\. Each keyword can contain 3\-90 UTF\-8 characters\. Keywords aren't case sensitive\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaximumMatchDistance`  <a name="cfn-macie-customdataidentifier-maximummatchdistance"></a>
The maximum number of characters that can exist between the end of at least one complete character sequence specified by the `Keywords` array and the end of text that matches the regular expression \(`Regex`\)\. If a complete keyword precedes all the text that matches the regular expression and the keyword is within the specified distance, Amazon Macie includes the result\.  
The distance can be 1\-300 characters\. The default value is 50\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-macie-customdataidentifier-name"></a>
A custom name for the custom data identifier\. The name can contain 1\-128 characters\.  
Avoid including sensitive data in the name of a custom data identifier\. Users of the account might be able to see the name, depending on the actions that they're allowed to perform in Amazon Macie\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Regex`  <a name="cfn-macie-customdataidentifier-regex"></a>
The regular expression \(*regex*\) that defines the text pattern to match\. The expression can contain 1\-512 characters\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-macie-customdataidentifier-return-values"></a>

### Ref<a name="aws-resource-macie-customdataidentifier-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the `CustomDataIdentifier`\. For example, `{ "Ref": "CustomDataIdentifier" }`

### Fn::GetAtt<a name="aws-resource-macie-customdataidentifier-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-macie-customdataidentifier-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the custom data identifier\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the custom data identifier\.

## Examples<a name="aws-resource-macie-customdataidentifier--examples"></a>

The following example demonstrates how to declare an `AWS::Macie::CustomDataIdentifier` resource\.

### Creating a custom data identifier<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_custom_data_identifier"></a>

This example creates a custom data identifier that detects six\-digit character sequences that are in proximity of certain keywords, as specified by the `Keywords` array\. If a match is a sample value, as specified by the `IgnoreWords` array, Amazon Macie excludes that match from the results\.

#### JSON<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_custom_data_identifier--json"></a>

```
{
    "Type": "AWS::Macie::CustomDataIdentifier",
    "DependsOn": "Session",
    "Properties": {
        "Description": "My custom data identifier",
        "IgnoreWords": [
            "000000",
            "123456"
        ],
        "Keywords": [
            "employeeID",
            "employee ID"
        ],
        "MaximumMatchDistance": 20,
        "Name": "EmployeeIDCustomDataIdentifier",
        "Regex": "\\d{6}"
    }
}
```

#### YAML<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_custom_data_identifier--yaml"></a>

```
Type: 'AWS::Macie::CustomDataIdentifier'
DependsOn: Session
Properties:
  Description: My custom data identifier
  IgnoreWords:
    - '000000'
    - '123456'
  Keywords:
    - 'employeeID'
    - 'employee ID'
  MaximumMatchDistance: 20
  Name: EmployeeIDCustomDataIdentifier
  Regex: '\\d{6}'
```