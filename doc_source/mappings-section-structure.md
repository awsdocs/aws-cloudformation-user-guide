# Mappings<a name="mappings-section-structure"></a>

The optional `Mappings` section matches a key to a corresponding set of named values\. For example, if you want to set values based on a region, you can create a mapping that uses the region name as a key and contains the values you want to specify for each specific region\. You use the `Fn::FindInMap` intrinsic function to retrieve values in a map\.

You cannot include parameters, pseudo parameters, or intrinsic functions in the `Mappings` section\.

## Syntax<a name="mappings-section-structure-syntax"></a>

The `Mappings` section consists of the key name `Mappings`\. The keys in mappings must be literal strings\. The values can be `String` or `List` types\.  The following example shows a `Mappings` section containing a single mapping named `Mapping01` \(the logical name\)\.

Within a mapping, each map is a key followed by another mapping\. The key must be a map of name\-value pairs and unique within the mapping\. The name can contain only alphanumeric characters \(A\-Za\-z0\-9\)\.

### JSON<a name="mappings-section-structure-syntax.json"></a>

```
"Mappings" : {
  "Mapping01" : {
    "Key01" : {
      "Name" : "Value01"
    },
    "Key02" : {
      "Name" : "Value02"
    },
    "Key03" : {
      "Name" : "Value03"
    }
  }
}
```

### YAML<a name="mappings-section-structure-syntax.yaml"></a>

```
Mappings: 
  Mapping01: 
    Key01: 
      Name: Value01
    Key02: 
      Name: Value02
    Key03: 
      Name: Value03
```

## Examples<a name="mappings-section-structure-examples"></a>

### Basic mapping<a name="mappings-section-structure-examples-basic"></a>

The following example shows a `Mappings` section with a map `RegionMap`, which contains five keys that map to name\-value pairs containing single string values\. The keys are region names\. Each name\-value pair is the AMI ID for the HVM64 AMI in the region represented by the key\.

The name\-value pairs have a name \(HVM64 in the example\) and a value\. By naming the values, you can map more than one set of values to a key\. 

#### JSON<a name="mappings-section-structure-example1.json"></a>

```
"Mappings" : {
  "RegionMap" : {
    "us-east-1"      : { "HVM64" : "ami-0ff8a91507f77f867"},
    "us-west-1"      : { "HVM64" : "ami-0bdb828fd58c52235"},
    "eu-west-1"      : { "HVM64" : "ami-047bb4163c506cd98"},
    "ap-southeast-1" : { "HVM64" : "ami-08569b978cc4dfa10"},
    "ap-northeast-1" : { "HVM64" : "ami-06cd52961ce9f0d85"}
  }
}
```

#### YAML<a name="mappings-section-structure-example1.yaml"></a>

```
Mappings: 
  RegionMap: 
    us-east-1: 
      "HVM64": "ami-0ff8a91507f77f867"
    us-west-1: 
      "HVM64": "ami-0bdb828fd58c52235"
    eu-west-1: 
      "HVM64": "ami-047bb4163c506cd98"
    ap-southeast-1: 
      "HVM64": "ami-08569b978cc4dfa10"
    ap-northeast-1: 
      "HVM64": "ami-06cd52961ce9f0d85"
```

### Mapping with multiple values<a name="mappings-section-structure-examples-multiple"></a>

The following example has region keys that are mapped to two sets of values: one named HVM64 and the other HVMG2\.

#### JSON<a name="mappings-section-structure-example2.json"></a>

```
    "RegionMap" : {
      "us-east-1"        : {"HVM64" : "ami-0ff8a91507f77f867", "HVMG2" : "ami-0a584ac55a7631c0c"},
      "us-west-1"        : {"HVM64" : "ami-0bdb828fd58c52235", "HVMG2" : "ami-066ee5fd4a9ef77f1"},
      "eu-west-1"        : {"HVM64" : "ami-047bb4163c506cd98", "HVMG2" : "ami-0a7c483d527806435"},
      "ap-northeast-1"   : {"HVM64" : "ami-06cd52961ce9f0d85", "HVMG2" : "ami-053cdd503598e4a9d"},
      "ap-southeast-1"   : {"HVM64" : "ami-08569b978cc4dfa10", "HVMG2" : "ami-0be9df32ae9f92309"}
    }
```

#### YAML<a name="mappings-section-structure-example2.yaml"></a>

```
RegionMap: 
    us-east-1:
      HVM64: ami-0ff8a91507f77f867
      HVMG2: ami-0a584ac55a7631c0c
    us-west-1:
      HVM64: ami-0bdb828fd58c52235
      HVMG2: ami-066ee5fd4a9ef77f1
    eu-west-1:
      HVM64: ami-047bb4163c506cd98
      HVMG2: ami-0a7c483d527806435
    ap-northeast-1:
      HVM64: ami-06cd52961ce9f0d85
      HVMG2: ami-053cdd503598e4a9d
    ap-southeast-1:
      HVM64: ami-08569b978cc4dfa10
      HVMG2: ami-0be9df32ae9f92309
```

### Return a value from a mapping<a name="mappings-section-structure-examples-return-value"></a>

You can use the `Fn::FindInMap` function to return a named value based on a specified key\. The following example template contains an Amazon EC2 resource whose `ImageId` property is assigned by the `FindInMap` function\. The `FindInMap` function specifies key as the region where the stack is created \(using the [AWS::Region pseudo parameter](pseudo-parameter-reference.md)\) and `HVM64` as the name of the value to map to\.

#### JSON<a name="mappings-section-structure-example3.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Mappings" : {
    "RegionMap" : {
      "us-east-1"        : {"HVM64" : "ami-0ff8a91507f77f867", "HVMG2" : "ami-0a584ac55a7631c0c"},
      "us-west-1"        : {"HVM64" : "ami-0bdb828fd58c52235", "HVMG2" : "ami-066ee5fd4a9ef77f1"},
      "eu-west-1"        : {"HVM64" : "ami-047bb4163c506cd98", "HVMG2" : "ami-0a7c483d527806435"},
      "ap-northeast-1"   : {"HVM64" : "ami-06cd52961ce9f0d85", "HVMG2" : "ami-053cdd503598e4a9d"},
      "ap-southeast-1"   : {"HVM64" : "ami-08569b978cc4dfa10", "HVMG2" : "ami-0be9df32ae9f92309"}
    }
  },

  "Resources" : {
    "myEC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "HVM64"]},
        "InstanceType" : "m1.small"
      }
    }
  }
}
```

#### YAML<a name="mappings-section-structure-example3.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Mappings: 
  RegionMap: 
    us-east-1:
      HVM64: ami-0ff8a91507f77f867
      HVMG2: ami-0a584ac55a7631c0c
    us-west-1:
      HVM64: ami-0bdb828fd58c52235
      HVMG2: ami-066ee5fd4a9ef77f1
    eu-west-1:
      HVM64: ami-047bb4163c506cd98
      HVMG2: ami-0a7c483d527806435
    ap-northeast-1:
      HVM64: ami-06cd52961ce9f0d85
      HVMG2: ami-053cdd503598e4a9d
    ap-southeast-1:
      HVM64: ami-08569b978cc4dfa10
      HVMG2: ami-0be9df32ae9f92309
Resources: 
  myEC2Instance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: !FindInMap [RegionMap, !Ref "AWS::Region", HVM64]
      InstanceType: m1.small
```

### Input parameter and FindInMap<a name="mappings-section-structure-examples-findinmap"></a>

You can use an input parameter with the `Fn::FindInMap` function to refer to a specific value in a map\. For example, suppose you have a list of regions and environment types that map to a specific AMI ID\. You can select the AMI ID that your stack uses by using an input parameter \(`EnvironmentType`\)\. To determine the region, use the `AWS::Region` pseudo parameter, which gets the AWS region in which you create the stack\.

#### JSON<a name="mappings-section-structure-example4.json"></a>

```
{
  "Parameters" : {
    "EnvironmentType": {
      "Description": "The environment type",
      "Type": "String",
      "Default": "test",
      "AllowedValues": ["prod", "test"],
      "ConstraintDescription": "must be a prod or test"
    }
  },
	
  "Mappings" : {
    "RegionAndInstanceTypeToAMIID" : {
      "us-east-1": {
        "test": "ami-8ff710e2",
        "prod": "ami-f5f41398"
      },
      "us-west-2" : {
        "test" : "ami-eff1028f",
        "prod" : "ami-d0f506b0"
      },

      ...other regions and AMI IDs...

    }
  },

  "Resources" : {
  
   ...other resources...

    },
    
  "Outputs" : {
    "TestOutput" : {
      "Description" : "Return the name of the AMI ID that matches the region and environment type keys",
      "Value" : { "Fn::FindInMap" : [ "RegionAndInstanceTypeToAMIID", { "Ref" : "AWS::Region" }, { "Ref" : "EnvironmentType" } ]}
    }
  }
  
}
```

#### YAML<a name="mappings-section-structure-example4.yaml"></a>

```
  Parameters: 
    EnvironmentType: 
      Description: The environment type
      Type: String
      Default: test
      AllowedValues: 
        - prod
        - test
      ConstraintDescription: must be a prod or test
  Mappings: 
    RegionAndInstanceTypeToAMIID: 
      us-east-1: 
        test: "ami-8ff710e2"
        prod: "ami-f5f41398"
      us-west-2: 
        test: "ami-eff1028f"
        prod: "ami-d0f506b0"
        
      ...other regions and AMI IDs...
  
  Resources:
  
   ...other resources...

  Outputs: 
    TestOutput: 
      Description: Return the name of the AMI ID that matches the region and environment type keys
      Value: !FindInMap [RegionAndInstanceTypeToAMIID, !Ref "AWS::Region", !Ref EnvironmentType]
```