# AWS::GuardDuty::IPSet<a name="aws-resource-guardduty-ipset"></a>

The `AWS::GuardDuty::IPSet` resource creates an Amazon GuardDuty IP set\. An IP set is a list of trusted IP addresses that have been whitelisted for secure communication with your AWS environment\. 


+ [Syntax](#aws-resource-guardduty-ipset-syntax)
+ [Properties](#aws-resource-guardduty-ipset-properties)
+ [Return Values](#aws-resource-guardduty-ipset-returnvalues)
+ [Examples](#aws-resource-guardduty-ipset-examples)

## Syntax<a name="aws-resource-guardduty-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-guardduty-ipset-syntax.json"></a>

```
{
  "Type" : "AWS::GuardDuty::IPSet",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-activate)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-detectorid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-format)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-location)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-name)" : String
  }
}
```

### YAML<a name="aws-resource-guardduty-ipset-syntax.yaml"></a>

```
Type: "AWS::GuardDuty::IPSet"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-activate): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-detectorid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-format): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-location): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-guardduty-ipset-name): String
```

## Properties<a name="aws-resource-guardduty-ipset-properties"></a>

`Activate`  
A Boolean value that indicates whether GuardDuty is to start using the uploaded IP set\.  
 *Required*: Yes  
 *Type*: Boolean  
 *Update requires*: No interruption 

`DetectorId`  
The detector ID that specifies the GuardDuty service for which an IP set is to be created\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`Format`  
The format of the file that contains the IP set\. Valid values are TXT, STIX, and OTX\_CSV\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`Location`  
The URI of the file that contains the IP set\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`Name`  
The friendly name to identify the IP set\. This name is displayed in all findings that are triggered by activity that involves IP addresses included in this IP set\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: No interruption 

## Return Values<a name="aws-resource-guardduty-ipset-returnvalues"></a>

### Ref<a name="aws-resource-guardduty-ipset-ref"></a>

When you pass the logical ID of an `AWS::GuardDuty::IPSet` resource to the intrinsic `Ref` function, the function returns the unique ID of the created IP set\. 

For more information about using the `Ref` function, see Ref\. 

## Examples<a name="aws-resource-guardduty-ipset-examples"></a>

### Declaring a GuardDuty IPSet Resource<a name="aws-resource-guardduty-ipset-example1"></a>

The following example shows how to declare an AWS::GuardDuty::IPSet resource to create a GuardDuty IP set\.

#### JSON<a name="aws-resource-guardduty-ipset-example1.json"></a>

```
"myipset”: {
  "Type": "AWS::GuardDuty::IPSet",
  "Properties": {
    "Activate": true,
    "DetectorId": "12abc34d567e8f4912ab3d45e67891f2",
    "Format": "TXT",
    "Location": "https://s3-us-west-2.amazonaws.com/mybucket/myipset.txt",
    "Name": "MyIPSet"
  }
}
```

#### YAML<a name="aws-resource-guardduty-ipset-example1.yaml"></a>

```
myipset:
  Type: "AWS::GuardDuty::IPSet"
  Properties:
    Activate: true
    DetectorId: "12abc34d567e8f4912ab3d45e67891f2"
    Format: "TXT"
    Location: "https://s3-us-west-2.amazonaws.com/mybucket/myipset.txt"
    Name: "MyIPSet"
```