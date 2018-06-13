# `Fn::FindInMap`<a name="intrinsic-function-reference-findinmap"></a>

The intrinsic function `Fn::FindInMap` returns the value corresponding to keys in a two\-level map that is declared in the `Mappings` section\.

## Declaration<a name="w3ab2c21c28c26b5"></a>

### JSON<a name="intrinsic-function-reference-findinmap-syntax.json"></a>

```
{ "Fn::FindInMap" : [ "MapName", "TopLevelKey", "SecondLevelKey"] }
```

### YAML<a name="intrinsic-function-reference-findinmap-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::FindInMap: [ MapName, TopLevelKey, SecondLevelKey ]
```

Syntax for the short form:

```
!FindInMap [ MapName, TopLevelKey, SecondLevelKey ]
```

**Note**  
You can't nest two instances of two functions in short form\.

## Parameters<a name="w3ab2c21c28c26b7"></a>

MapName  
The logical name of a mapping declared in the Mappings section that contains the keys and values\.

TopLevelKey  
The top\-level key name\. Its value is a list of key\-value pairs\.

SecondLevelKey  
The second\-level key name, which is set to one of the keys from the list assigned to `TopLevelKey`\.

## Return Value:<a name="w3ab2c21c28c26b9"></a>

The value that is assigned to `SecondLevelKey`\. 

## Example<a name="w3ab2c21c28c26c11"></a>

The following example shows how to use `Fn::FindInMap` for a template with a `Mappings` section that contains a single map, `RegionMap`, that associates AMIs with AWS regions\. 
+ The map has 5 top\-level keys that correspond to various AWS regions\.
+ Each top\-level key is assigned a list with two second level keys, `"32"` and `"64"`, that correspond to the AMI's architecture\.
+ Each of the second\-level keys is assigned an appropriate AMI name\.

The example template contains an `AWS::EC2::Instance` resource whose `ImageId` property is set by the `FindInMap` function\. 

`MapName` is set to the map of interest, `"RegionMap"` in this example\. `TopLevelKey` is set to the region where the stack is created, which is determined by using the `"AWS::Region"` pseudo parameter\. `SecondLevelKey` is set to the desired architecture, `"32"` for this example\.

`FindInMap` returns the AMI assigned to `FindInMap`\. For a 32\-bit instance in us\-east\-1, `FindInMap` would return `"ami-6411e20d"`\.

### JSON<a name="intrinsic-function-reference-findinmap-example.json"></a>

```
 1. {
 2.   ...
 3.   "Mappings" : {
 4.     "RegionMap" : {
 5.       "us-east-1" : { "32" : "ami-6411e20d", "64" : "ami-7a11e213" },
 6.       "us-west-1" : { "32" : "ami-c9c7978c", "64" : "ami-cfc7978a" },
 7.       "eu-west-1" : { "32" : "ami-37c2f643", "64" : "ami-31c2f645" },
 8.       "ap-southeast-1" : { "32" : "ami-66f28c34", "64" : "ami-60f28c32" },
 9.       "ap-northeast-1" : { "32" : "ami-9c03a89d", "64" : "ami-a003a8a1" }
10.     }
11.   },
12. 
13.   "Resources" : {
14.      "myEC2Instance" : {
15.         "Type" : "AWS::EC2::Instance",
16.         "Properties" : {
17.            "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "32"]},
18.            "InstanceType" : "m1.small"
19.         }
20.      }
21.  }
22. }
```

### YAML<a name="intrinsic-function-reference-findinmap-example.yaml"></a>

```
Mappings: 
  RegionMap: 
    us-east-1: 
      32: "ami-6411e20d"
      64: "ami-7a11e213"
    us-west-1: 
      32: "ami-c9c7978c"
      64: "ami-cfc7978a"
    eu-west-1: 
      32: "ami-37c2f643"
      64: "ami-31c2f645"
    ap-southeast-1: 
      32: "ami-66f28c34"
      64: "ami-60f28c32"
    ap-northeast-1: 
      32: "ami-9c03a89d"
      64: "ami-a003a8a1"
Resources: 
  myEC2Instance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: !FindInMap [ RegionMap, !Ref "AWS::Region", 32 ]
      InstanceType: m1.small
```

## Supported Functions<a name="w3ab2c21c28c26c13"></a>

You can use the following functions in a `Fn::FindInMap` function:
+ `Fn::FindInMap`
+ `Ref`