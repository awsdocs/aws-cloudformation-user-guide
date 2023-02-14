# AWS::S3::MultiRegionAccessPointPolicy<a name="aws-resource-s3-multiregionaccesspointpolicy"></a>

Applies an Amazon S3 access policy to an Amazon S3 Multi\-Region Access Point\.

It is not possible to delete an access policy for a Multi\-Region Access Point from the CloudFormation template\. When you attempt to delete the policy, CloudFormation updates the policy using `DeletionPolicy:Retain` and `UpdateReplacePolicy:Retain`\. CloudFormation updates the policy to only allow access to the account that created the bucket\.

## Syntax<a name="aws-resource-s3-multiregionaccesspointpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-multiregionaccesspointpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::S3::MultiRegionAccessPointPolicy",
  "Properties" : {
      "[MrapName](#cfn-s3-multiregionaccesspointpolicy-mrapname)" : String,
      "[Policy](#cfn-s3-multiregionaccesspointpolicy-policy)" : Json
    }
}
```

### YAML<a name="aws-resource-s3-multiregionaccesspointpolicy-syntax.yaml"></a>

```
Type: AWS::S3::MultiRegionAccessPointPolicy
Properties: 
  [MrapName](#cfn-s3-multiregionaccesspointpolicy-mrapname): String
  [Policy](#cfn-s3-multiregionaccesspointpolicy-policy): Json
```

## Properties<a name="aws-resource-s3-multiregionaccesspointpolicy-properties"></a>

`MrapName`  <a name="cfn-s3-multiregionaccesspointpolicy-mrapname"></a>
The name of the Multi\-Region Access Point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-s3-multiregionaccesspointpolicy-policy"></a>
The access policy associated with the Multi\-Region Access Point\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3-multiregionaccesspointpolicy-return-values"></a>

### Ref<a name="aws-resource-s3-multiregionaccesspointpolicy-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the Multi\-Region Access Point\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-s3-multiregionaccesspointpolicy--examples"></a>



### Simple Multi\-Region Access Point Policy<a name="aws-resource-s3-multiregionaccesspointpolicy--examples--Simple_Multi-Region_Access_Point_Policy"></a>

The following example grants access permissions to CloudWatch\.

It is very important to note where you need to use the name versus the alias for the Multi\-Region Access Point\. In the following example, the name is `DOC-EXAMPLE-MULTI-REGION-ACCESS-POINT`, the alias of the Multi\-Region Access Point is `mfzwi23gnjvgw.mrap`, and the AWS account is `123456789012`\. For more information about how ARNs for Multi\-Region Access Points work, see [ Making requests using a Multi\-Region Access Point](https://docs.aws.amazon.com/AmazonS3/latest/userguide/MultiRegionAccessPointRequests.html) in the in the *Amazon S3 User Guide*\.

#### JSON<a name="aws-resource-s3-multiregionaccesspointpolicy--examples--Simple_Multi-Region_Access_Point_Policy--json"></a>

```
{
   "SampleMultiRegionAccessPointPolicy":{
      "Type":"AWS::S3::MultiRegionAccessPointPolicy",
      "DeletionPolicy":"Retain",
      "UpdateReplacePolicy":"Retain",
      "Properties":{
         "MrapName":{
            "Ref":"DOC-EXAMPLE-MULTI-REGION-ACCESS-POINT"
         },
         "Policy":{
            "Statement":[
               {
                  "Action":[
                     "s3:GetObject"
                  ],
                  "Effect":"Allow",
                  "Resource":{
                     "Fn::Sub":[
                        "arn:aws:s3::123456789012:accesspoint/mfzwi23gnjvgw.mrap/object/*",
                        {
                           "mrapalias":{
                              "Fn::GetAtt":[
                                 "mfzwi23gnjvgw.mrap",
                                 "Alias"
                              ]
                           }
                        }
                     ]
                  },
                  "Principal":{
                     "Service":"cloudwatch.amazonaws.com"
                  }
               }
            ]
         }
      }
   }
}
```

#### YAML<a name="aws-resource-s3-multiregionaccesspointpolicy--examples--Simple_Multi-Region_Access_Point_Policy--yaml"></a>

```
SampleMultiRegionAccessPointPolicy:
  Type: 'AWS::S3::MultiRegionAccessPointPolicy'
  DeletionPolicy: Retain
  UpdateReplacePolicy: Retain
  Properties:
    MrapName:
      Ref: DOC-EXAMPLE-MULTI-REGION-ACCESS-POINT
    Policy:
      Statement:
        - Action:
            - 's3:GetObject'
          Effect: Allow
          Resource:
            'Fn::Sub':
              - 'arn:aws:s3::123456789012:accesspoint/mfzwi23gnjvgw.mrap/object/*'
              - mrapalias:
                  'Fn::GetAtt':
                    - mfzwi23gnjvgw.mrap
                    - Alias
          Principal:
            Service: cloudwatch.amazonaws.com
```