# AWS::Macie::CustomDataIdentifier<a name="aws-resource-macie-customdataidentifier"></a>

The `AWS::Macie::CustomDataIdentifier` resource is a set of criteria that you define to detect sensitive data in one or more data sources\. Each identifier specifies a regular expression \(regex\) that defines a text pattern to match in the data\. It can also specify character sequences, such as words and phrases, and a proximity rule that refine the analysis of a data source\. By using custom data identifiers, you can tailor your analysis to meet your organization's specific needs, and supplement the built\-in data identifiers that Amazon Macie provides\.

A `Session` must exist for the account before you can create a `CustomDataIdentifier`\. Use a [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to ensure that the `Session` is created before the other resources\. For example, `"DependsOn: Session"`\.

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
The description of the custom data identifier\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IgnoreWords`  <a name="cfn-macie-customdataidentifier-ignorewords"></a>
An array that lists specific character sequences \(ignore words\) to exclude from the results\. If the text matched by the regular expression is the same as any string in this array, Amazon Macie ignores it\. The array can contain as many as 10 ignore words\. Each ignore word can contain 4 \- 90 characters\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Keywords`  <a name="cfn-macie-customdataidentifier-keywords"></a>
An array that lists specific character sequences \(keywords\), one of which must be within proximity \(`MaximumMatchDistance`\) of the regular expression to match\. The array can contain as many as 50 keywords\. Each keyword can contain 4 \- 90 characters\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaximumMatchDistance`  <a name="cfn-macie-customdataidentifier-maximummatchdistance"></a>
The maximum number of characters that can exist between text that matches the regex pattern and the character sequences specified by the `Keywords` array\. Amazon Macie includes or excludes a result based on the proximity of a keyword to text that matches the regex pattern\. The distance can be 1 \- 300 characters\. The default value is 50\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-macie-customdataidentifier-name"></a>
A custom name for the custom data identifier\. The name can contain as many as 120 characters\.  
We strongly recommend that you avoid including any sensitive data in the name of a custom data identifier\. Other users of your account might be able to see the identifier's name, depending on the actions that they're allowed to perform in Amazon Macie\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Regex`  <a name="cfn-macie-customdataidentifier-regex"></a>
The regular expression \(regex\) that defines the pattern to match\. The expression can contain as many as 500 characters\.  
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

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The date and time, in UTC and extended ISO 8601 format, when the custom data identifier was created\.

`Deleted`  <a name="Deleted-fn::getatt"></a>
Specifies whether the custom data identifier was deleted\. If you delete a custom data identifier, Amazon Macie doesn't delete it permanently\. Instead, it soft deletes the identifier\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier for the custom data identifier\.

## Examples<a name="aws-resource-macie-customdataidentifier--examples"></a>

The following example demonstrates how to declare an `AWS::Macie::CustomDataIdentifier` resource\.

### Creating a Macie CustomDataIdentifier<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_Macie_CustomDataIdentifier"></a>

This example creates a custom data identifier that detects 6\-digit employee IDs that are located near the specified keywords\. If the match is a sample value, such as those provided in the ignore words, it is skipped\.

#### JSON<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_Macie_CustomDataIdentifier--json"></a>

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

#### YAML<a name="aws-resource-macie-customdataidentifier--examples--Creating_a_Macie_CustomDataIdentifier--yaml"></a>

```
Type: AWS::Macie::CustomDataIdentifier
DependsOn: "Session"
Properties:
    Description: "My custom data identifier"
    IgnoreWords: 
        - "000000" 
        - "123456"
    Keywords: 
        - "employeeID" 
        - "Employee ID"
    MaximumMatchDistance: 20
    Name: EmployeeIDCustomDataIdentifier
    Regex: \d{6}
```