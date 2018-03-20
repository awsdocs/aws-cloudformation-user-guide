# Mappings<a name="mappings-section-structure"></a>

The optional `Mappings` section matches a key to a corresponding set of named values\. For example, if you want to set values based on a region, you can create a mapping that uses the region name as a key and contains the values you want to specify for each specific region\. You use the `Fn::FindInMap` intrinsic function to retrieve values in a map\.

You cannot include parameters, pseudo parameters, or intrinsic functions in the `Mappings` section\.

## Syntax<a name="w3ab2c17c15c19b7"></a>

The `Mappings` section consists of the key name `Mappings`\. The keys in mappings must be literal strings\. The values can be `String` or `List` types\.  The following example shows a `Mappings` section containing a single mapping named `Mapping01` \(the logical name\)\.

Within a mapping, each map is a key followed by another mapping\. The key identifies a map of name\-value pairs and must be unique within the mapping\. The name can contain only alphanumeric characters \(A\-Za\-z0\-9\)\.

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

## Examples<a name="w3ab2c17c15c19b9"></a>

### Basic Mapping<a name="w3ab2c17c15c19b9b2"></a>

The following example shows a `Mappings` section with a map `RegionMap`, which contains five keys that map to name\-value pairs containing single string values\. The keys are region names\. Each name\-value pair is the AMI ID for the 32\-bit AMI in the region represented by the key\.

The name\-value pairs have a name \(32 in the example\) and a value\. By naming the values, you can map more than one set of values to a key\. 

#### JSON<a name="mappings-section-structure-example1.json"></a>

```
"Mappings" : {
  "RegionMap" : {
    "us-east-1"      : { "32" : "ami-6411e20d"},
    "us-west-1"      : { "32" : "ami-c9c7978c"},
    "eu-west-1"      : { "32" : "ami-37c2f643"},
    "ap-southeast-1" : { "32" : "ami-66f28c34"},
    "ap-northeast-1" : { "32" : "ami-9c03a89d"}
  }
}
```

#### YAML<a name="mappings-section-structure-example1.yaml"></a>

```
Mappings: 
  RegionMap: 
    us-east-1: 
      "32": "ami-6411e20d"
    us-west-1: 
      "32": "ami-c9c7978c"
    eu-west-1: 
      "32": "ami-37c2f643"
    ap-southeast-1: 
      "32": "ami-66f28c34"
    ap-northeast-1: 
      "32": "ami-9c03a89d"
```

### Mapping with Multiple Values<a name="w3ab2c17c15c19b9b4"></a>

The following example has region keys that are mapped to two sets of values: one named 32 and the other 64\.

#### JSON<a name="mappings-section-structure-example2.json"></a>

```
"RegionMap" : {
  "us-east-1"      : { "32" : "ami-6411e20d", "64" : "ami-7a11e213" },
  "us-west-1"      : { "32" : "ami-c9c7978c", "64" : "ami-cfc7978a" },
  "eu-west-1"      : { "32" : "ami-37c2f643", "64" : "ami-31c2f645" },
  "ap-southeast-1" : { "32" : "ami-66f28c34", "64" : "ami-60f28c32" },
  "ap-northeast-1" : { "32" : "ami-9c03a89d", "64" : "ami-a003a8a1" }
}
```

#### YAML<a name="mappings-section-structure-example2.yaml"></a>

```
RegionMap: 
  us-east-1: 
    "32": "ami-6411e20d"
    "64": "ami-7a11e213"
  us-west-1: 
    "32": "ami-c9c7978c"
    "64": "ami-cfc7978a"
  eu-west-1: 
    "32": "ami-37c2f643"
    "64": "ami-31c2f645"
  ap-southeast-1: 
    "32": "ami-66f28c34"
    "64": "ami-60f28c32"
  ap-northeast-1: 
    "32": "ami-9c03a89d"
    "64": "ami-a003a8a1"
```

### Return a Value from a Mapping<a name="w3ab2c17c15c19b9b6"></a>

You can use the `[Fn::FindInMap](intrinsic-function-reference-findinmap.md)` function to return a named value based on a specified key\. The following example template contains an Amazon EC2 resource whose `ImageId` property is assigned by the `FindInMap` function\. The `FindInMap` function specifies key as the region where the stack is created \(using the [AWS::Region pseudo parameter](pseudo-parameter-reference.md)\) and `32` as the name of the value to map to\.

#### JSON<a name="mappings-section-structure-example3.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",

  "Mappings" : {
    "RegionMap" : {
      "us-east-1" : { "32" : "ami-6411e20d", "64" : "ami-7a11e213" },
      "us-west-1" : { "32" : "ami-c9c7978c", "64" : "ami-cfc7978a" },
      "eu-west-1" : { "32" : "ami-37c2f643", "64" : "ami-31c2f645" },
      "ap-southeast-1" : { "32" : "ami-66f28c34", "64" : "ami-60f28c32" },
      "ap-northeast-1" : { "32" : "ami-9c03a89d", "64" : "ami-a003a8a1" }
    }
  },

  "Resources" : {
    "myEC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "32"]},
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
      "32": "ami-6411e20d"
      "64": "ami-7a11e213"
    us-west-1: 
      "32": "ami-c9c7978c"
      "64": "ami-cfc7978a"
    eu-west-1: 
      "32": "ami-37c2f643"
      "64": "ami-31c2f645"
    ap-southeast-1: 
      "32": "ami-66f28c34"
      "64": "ami-60f28c32"
    ap-northeast-1: 
      "32": "ami-9c03a89d"
      "64": "ami-a003a8a1"
Resources: 
  myEC2Instance: 
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: !FindInMap [RegionMap, !Ref "AWS::Region", 32]
      InstanceType: m1.small
```

### Input Parameter and FindInMap<a name="w3ab2c17c15c19b9b8"></a>

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