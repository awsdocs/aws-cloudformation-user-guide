# AWS::Route53::CidrCollection<a name="aws-resource-route53-cidrcollection"></a>

Creates a CIDR collection in the current AWS account\.

## Syntax<a name="aws-resource-route53-cidrcollection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-cidrcollection-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::CidrCollection",
  "Properties" : {
      "[Locations](#cfn-route53-cidrcollection-locations)" : [ Location, ... ],
      "[Name](#cfn-route53-cidrcollection-name)" : String
    }
}
```

### YAML<a name="aws-resource-route53-cidrcollection-syntax.yaml"></a>

```
Type: AWS::Route53::CidrCollection
Properties: 
  [Locations](#cfn-route53-cidrcollection-locations): 
    - Location
  [Name](#cfn-route53-cidrcollection-name): String
```

## Properties<a name="aws-resource-route53-cidrcollection-properties"></a>

`Locations`  <a name="cfn-route53-cidrcollection-locations"></a>
A complex type that contains information about the list of CIDR locations\.  
*Required*: No  
*Type*: List of [Location](aws-properties-route53-cidrcollection-location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-route53-cidrcollection-name"></a>
The name of a CIDR collection\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[0-9A-Za-z_\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53-cidrcollection-return-values"></a>

### Ref<a name="aws-resource-route53-cidrcollection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `CidrCollection` ID\.

### Fn::GetAtt<a name="aws-resource-route53-cidrcollection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53-cidrcollection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
"The Amazon resource name \(ARN\) to uniquely identify the AWS resource\.

`Id`  <a name="Id-fn::getatt"></a>
The UUID of the CIDR collection\.

## Examples<a name="aws-resource-route53-cidrcollection--examples"></a>



### Create a CIDR collection<a name="aws-resource-route53-cidrcollection--examples--Create_a_CIDR_collection"></a>

The following example creates CIDR collection with two locations that each contain two CIDR blocks\.

#### JSON<a name="aws-resource-route53-cidrcollection--examples--Create_a_CIDR_collection--json"></a>

```
{
  "MyCidrCollection":{
    "Type":"AWS::Route53::CidrCollection",
    "Properties":{
      "Name":"my-first-cidr-collection",
      "Locations":[
      {
        "LocationName":"location-1",
        "CidrList":[
          "1.1.0.0/24",
          "2.1.0.0/16"
        ]
      },
      {  
        "LocationName":"location-2",
        "CidrList":[
          "2002::1234:0:0:0:0:0/48",
          "1002::/32"
        ]
      }
    ]
   }
  }
}
```

#### YAML<a name="aws-resource-route53-cidrcollection--examples--Create_a_CIDR_collection--yaml"></a>

```
MyCidrCollection:
  Type: AWS::Route53::CidrCollection
  Properties:
    Name: "my-first-cidr-collection"
    Locations:
      - LocationName: "location-1"
        CidrList:
          - "1.1.0.0/24"
          - "2.1.0.0/16"
      - LocationName: "location-2"
        CidrList:
          - "2002::1234:0:0:0:0:0/48"
          - "1002::/32"
```

## See also<a name="aws-resource-route53-cidrcollection--seealso"></a>
+ [CreateCidrCollection](https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateCidrCollection.html) in the *Amazon Route 53 API Reference*

