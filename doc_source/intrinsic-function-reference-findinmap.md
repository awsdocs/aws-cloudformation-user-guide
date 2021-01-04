# `Fn::FindInMap`<a name="intrinsic-function-reference-findinmap"></a>

The intrinsic function `Fn::FindInMap` returns the value corresponding to keys in a two\-level map that is declared in the `Mappings` section\.

## Declaration<a name="w7739ab1c33c28c26b5"></a>

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

## Parameters<a name="w7739ab1c33c28c26b7"></a>

MapName  
The logical name of a mapping declared in the Mappings section that contains the keys and values\.

TopLevelKey  
The top\-level key name\. Its value is a list of key\-value pairs\.

SecondLevelKey  
The second\-level key name, which is set to one of the keys from the list assigned to `TopLevelKey`\.

## Return value:<a name="w7739ab1c33c28c26b9"></a>

The value that is assigned to `SecondLevelKey`\. 

## Example<a name="w7739ab1c33c28c26c11"></a>

The following example shows how to use `Fn::FindInMap` for a template with a `Mappings` section that contains a single map, `RegionMap`, that associates AMIs with AWS regions\. 
+ The map has 5 top\-level keys that correspond to various AWS regions\.
+ Each top\-level key is assigned a list with two second level keys, `"HVM64"` and `"HVMG2"`, that correspond to the AMI's architecture\.
+ Each of the second\-level keys is assigned an appropriate AMI name\.

The example template contains an `AWS::EC2::Instance` resource whose `ImageId` property is set by the `FindInMap` function\. 

`MapName` is set to the map of interest, `"RegionMap"` in this example\. `TopLevelKey` is set to the region where the stack is created, which is determined by using the `"AWS::Region"` pseudo parameter\. `SecondLevelKey` is set to the desired architecture, `"HVM64"` for this example\.

`FindInMap` returns the AMI assigned to `FindInMap`\. For a HVM64 instance in us\-east\-1, `FindInMap` would return `"ami-0ff8a91507f77f867"`\.

### JSON<a name="intrinsic-function-reference-findinmap-example.json"></a>

```
 1. {
 2.   ...
 3.   "Mappings" : {
 4.     "RegionMap" : {
 5.       "us-east-1" : { 
 6.         "HVM64" : "ami-0ff8a91507f77f867", "HVMG2" : "ami-0a584ac55a7631c0c" 
 7.       },
 8.       "us-west-1" : { 
 9.         "HVM64" : "ami-0bdb828fd58c52235", "HVMG2" : "ami-066ee5fd4a9ef77f1" 
10.       },
11.       "eu-west-1" : { 
12.         "HVM64" : "ami-047bb4163c506cd98", "HVMG2" : "ami-0a7c483d527806435" 
13.       },
14.       "ap-southeast-1" : { 
15.         "HVM64" : "ami-08569b978cc4dfa10", "HVMG2" : "ami-0be9df32ae9f92309" 
16.       },
17.       "ap-northeast-1" : { 
18.         "HVM64" : "ami-06cd52961ce9f0d85", "HVMG2" : "ami-053cdd503598e4a9d" 
19.       }
20.     }
21.   },
22. 
23.   "Resources" : {
24.     "myEC2Instance" : {
25.       "Type" : "AWS::EC2::Instance",
26.       "Properties" : {
27.         "ImageId" : { 
28.           "Fn::FindInMap" : [ 
29.             "RegionMap", 
30.             { 
31.               "Ref" : "AWS::Region" 
32.             }, 
33.             "HVM64"
34.           ]
35.         },
36.         "InstanceType" : "m1.small"
37.       }   
38.     }
39.   }
40. }
```

### YAML<a name="intrinsic-function-reference-findinmap-example.yaml"></a>

```
Mappings: 
  RegionMap: 
    us-east-1: 
      HVM64: "ami-0ff8a91507f77f867"
      HVMG2: "ami-0a584ac55a7631c0c"
    us-west-1: 
      HVM64: "ami-0bdb828fd58c52235"
      HVMG2: "ami-066ee5fd4a9ef77f1"
    eu-west-1: 
      HVM64: "ami-047bb4163c506cd98"
      HVMG2: "ami-31c2f645"
    ap-southeast-1: 
      HVM64: "ami-08569b978cc4dfa10"
      HVMG2: "ami-0be9df32ae9f92309"
    ap-northeast-1: 
      HVM64: "ami-06cd52961ce9f0d85"
      HVMG2: "ami-053cdd503598e4a9d"
Resources: 
  myEC2Instance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: !FindInMap
        - RegionMap
        - !Ref 'AWS::Region'
        - HVM64
      InstanceType: m1.small
```

## Supported functions<a name="w7739ab1c33c28c26c13"></a>

You can use the following functions in a `Fn::FindInMap` function:
+ `Fn::FindInMap`
+ `Ref`