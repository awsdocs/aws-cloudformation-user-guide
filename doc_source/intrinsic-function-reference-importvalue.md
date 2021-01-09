# `Fn::ImportValue`<a name="intrinsic-function-reference-importvalue"></a>

The intrinsic function `Fn::ImportValue` returns the value of [an output exported](outputs-section-structure.md) by another stack\. You typically use this function to [create cross\-stack references](walkthrough-crossstackref.md)\. In the following example template snippets, Stack A exports VPC security group values and Stack B imports them\.

**Note**  
The following restrictions apply to cross\-stack references:  
For each AWS account, `Export` names must be unique within a region\.
You can't create cross\-stack references across regions\. You can use the intrinsic function `Fn::ImportValue` to import only values that have been exported within the same region\.
For outputs, the value of the `Name` property of an `Export` can't use `Ref` or `GetAtt` functions that depend on a resource\.  
Similarly, the `ImportValue` function can't include `Ref` or `GetAtt` functions that depend on a resource\.
You can't delete a stack if another stack references one of its outputs\.
You can't modify or remove an output value that is referenced by another stack\.

Stack A Export

```
"Outputs" : {
  "PublicSubnet" : {
    "Description" : "The subnet ID to use for public web servers",
    "Value" :  { "Ref" : "PublicSubnet" },
    "Export" : { "Name" : {"Fn::Sub": "${AWS::StackName}-SubnetID" }}
  },
  "WebServerSecurityGroup" : {
    "Description" : "The security group ID to use for public web servers",
    "Value" :  { "Fn::GetAtt" : ["WebServerSecurityGroup", "GroupId"] },
    "Export" : { "Name" : {"Fn::Sub": "${AWS::StackName}-SecurityGroupID" }}
  }
}
```

Stack B Import

```
"Resources" : {
  "WebServerInstance" : {
    "Type" : "AWS::EC2::Instance",
    "Properties" : {
      "InstanceType" : "t2.micro",
      "ImageId" : "ami-a1b23456",
      "NetworkInterfaces" : [{
        "GroupSet" : [{"Fn::ImportValue" : {"Fn::Sub" : "${NetworkStackNameParameter}-SecurityGroupID"}}],
        "AssociatePublicIpAddress" : "true",
        "DeviceIndex" : "0",
        "DeleteOnTermination" : "true",
        "SubnetId" : {"Fn::ImportValue" : {"Fn::Sub" : "${NetworkStackNameParameter}-SubnetID"}}
      }]
    }
  }
}
```

## Declaration<a name="w7739ab1c33c28c41c15"></a>

### JSON<a name="intrinsic-function-reference-importvalue-syntax.json"></a>

```
{ "Fn::ImportValue" : sharedValueToImport }
```

### YAML<a name="intrinsic-function-reference-importvalue-syntax.yaml"></a>

You can use the full function name:

```
Fn::ImportValue: sharedValueToImport
```

Alternatively, you can use the short form:

```
!ImportValue sharedValueToImport
```

**Important**  
You can't use the short form of `!ImportValue` when it contains a `!Sub`\. The following example is valid for AWS CloudFormation, but *not* valid for YAML:   

```
!ImportValue
  !Sub "${NetworkStack}-SubnetID"
```
Instead, you must use the full function name, for example:  

```
Fn::ImportValue:
  !Sub "${NetworkStack}-SubnetID"
```

## Parameters<a name="w7739ab1c33c28c41c17"></a>

sharedValueToImport  
The stack output value that you want to import\.

## Return value<a name="w7739ab1c33c28c41c19"></a>

The stack output value\.

## Example<a name="w7739ab1c33c28c41c21"></a>

### JSON<a name="intrinsic-function-reference-importvalue-example.json"></a>

```
{ "Fn::ImportValue" : {"Fn::Sub": "${NetworkStackNameParameter}-SubnetID" } }
```

### YAML<a name="intrinsic-function-reference-importvalue-example.yaml"></a>

```
Fn::ImportValue:
  !Sub "${NetworkStackName}-SecurityGroupID"
```

## Supported functions<a name="w7739ab1c33c28c41c23"></a>

You can use the following functions in the `Fn::ImportValue` function\. The value of these functions can't depend on a resource\.
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::If`
+ `Fn::Join`
+ `Fn::Select`
+ `Fn::Split`
+ `Fn::Sub`
+ `Ref`