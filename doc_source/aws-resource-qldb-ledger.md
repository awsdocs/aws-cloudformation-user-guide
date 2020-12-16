# AWS::QLDB::Ledger<a name="aws-resource-qldb-ledger"></a>

The `AWS::QLDB::Ledger` resource creates a new Amazon Quantum Ledger Database \(Amazon QLDB\) ledger in your AWS account\. Amazon QLDB is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log owned by a central trusted authority\. You can use QLDB to track all application data changes, and maintain a complete and verifiable history of changes over time\.

For more information, see [CreateLedger](https://docs.aws.amazon.com/qldb/latest/developerguide/API_CreateLedger.html) in the *Amazon QLDB API Reference*\.

## Syntax<a name="aws-resource-qldb-ledger-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-qldb-ledger-syntax.json"></a>

```
{
  "Type" : "AWS::QLDB::Ledger",
  "Properties" : {
      "[DeletionProtection](#cfn-qldb-ledger-deletionprotection)" : Boolean,
      "[Name](#cfn-qldb-ledger-name)" : String,
      "[PermissionsMode](#cfn-qldb-ledger-permissionsmode)" : String,
      "[Tags](#cfn-qldb-ledger-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-qldb-ledger-syntax.yaml"></a>

```
Type: AWS::QLDB::Ledger
Properties: 
  [DeletionProtection](#cfn-qldb-ledger-deletionprotection): Boolean
  [Name](#cfn-qldb-ledger-name): String
  [PermissionsMode](#cfn-qldb-ledger-permissionsmode): String
  [Tags](#cfn-qldb-ledger-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-qldb-ledger-properties"></a>

`DeletionProtection`  <a name="cfn-qldb-ledger-deletionprotection"></a>
The flag that prevents a ledger from being deleted by any user\. If not provided on ledger creation, this feature is enabled \(`true`\) by default\.  
If deletion protection is enabled, you must first disable it before you can delete the ledger using the QLDB API or the AWS Command Line Interface \(AWS CLI\)\. You can disable it by calling the `UpdateLedger` operation to set the flag to `false`\. The QLDB console disables deletion protection for you when you use it to delete a ledger\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-qldb-ledger-name"></a>
The name of the ledger that you want to create\. The name must be unique among all of your ledgers in the current AWS Region\.  
Naming constraints for ledger names are defined in [Quotas in Amazon QLDB](https://docs.aws.amazon.com/qldb/latest/developerguide/limits.html#limits.naming) in the *Amazon QLDB Developer Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Pattern*: `(?!^.*--)(?!^[0-9]+$)(?!^-)(?!.*-$)^[A-Za-z0-9-]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsMode`  <a name="cfn-qldb-ledger-permissionsmode"></a>
The permissions mode to assign to the ledger that you want to create\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ALLOW_ALL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-qldb-ledger-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-qldb-ledger-return-values"></a>

### Ref<a name="aws-resource-qldb-ledger-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myQLDBLedger" }` 

For the resource with the logical ID `myQLDBLedger`, `Ref` returns the Amazon QLDB ledger name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-qldb-ledger--examples"></a>



### Amazon QLDB Ledger<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger"></a>

The following example describes an Amazon QLDB ledger with a `PermissionsMode` of `ALLOW_ALL`\. The only permissions mode currently supported for a QLDB ledger is `ALLOW_ALL`\.

#### JSON<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger--json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myQLDBLedger": {
      "Type": "AWS::QLDB::Ledger",
      "Properties": {
        "DeletionProtection": true,
        "Name": "exampleLedger",
        "PermissionsMode": "ALLOW_ALL",
        "Tags": [
          {
            "Key": "Domain",
            "Value": "Test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-qldb-ledger--examples--Amazon_QLDB_Ledger--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  myQLDBLedger: 
    Type: "AWS::QLDB::Ledger"
    Properties:
      DeletionProtection: true
      Name: "exampleLedger"
      PermissionsMode: "ALLOW_ALL"
      Tags:
        - Key: Domain
          Value: Test
```

## See also<a name="aws-resource-qldb-ledger--seealso"></a>
+  [CreateLedger](https://docs.aws.amazon.com/qldb/latest/developerguide/API_CreateLedger.html) in the *Amazon QLDB API Reference*

