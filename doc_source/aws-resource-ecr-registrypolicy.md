# AWS::ECR::RegistryPolicy<a name="aws-resource-ecr-registrypolicy"></a>

The `AWS::ECR::RegistryPolicy` resource creates or updates the permissions policy for a private registry\.

A private registry policy is used to specify permissions for another AWS account and is used when configuring cross\-account replication\. For more information, see [Registry permissions](https://docs.aws.amazon.com/AmazonECR/latest/userguide/registry-permissions.html) in the *Amazon Elastic Container Registry User Guide*\.

## Syntax<a name="aws-resource-ecr-registrypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-registrypolicy-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::RegistryPolicy",
  "Properties" : {
      "[PolicyText](#cfn-ecr-registrypolicy-policytext)" : Json
    }
}
```

### YAML<a name="aws-resource-ecr-registrypolicy-syntax.yaml"></a>

```
Type: AWS::ECR::RegistryPolicy
Properties: 
  [PolicyText](#cfn-ecr-registrypolicy-policytext): Json
```

## Properties<a name="aws-resource-ecr-registrypolicy-properties"></a>

`PolicyText`  <a name="cfn-ecr-registrypolicy-policytext"></a>
The JSON policy text for your registry\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecr-registrypolicy-return-values"></a>

### Fn::GetAtt<a name="aws-resource-ecr-registrypolicy-return-values-fn--getatt"></a>

#### <a name="aws-resource-ecr-registrypolicy-return-values-fn--getatt-fn--getatt"></a>

`RegistryId`  <a name="RegistryId-fn::getatt"></a>
The account ID of the private registry the policy is associated with\.

## Examples<a name="aws-resource-ecr-registrypolicy--examples"></a>



### Specify a registry policy for a private registry<a name="aws-resource-ecr-registrypolicy--examples--Specify_a_registry_policy_for_a_private_registry"></a>

The following example specifies a private registry policy in `us-west-2` that grants permission for account `210987654321` to create repositories and replicate their contents to your private registry\.

#### JSON<a name="aws-resource-ecr-registrypolicy--examples--Specify_a_registry_policy_for_a_private_registry--json"></a>

```
"TestRegistryPolicy": {
   "Type": "AWS::ECR::RegistryPolicy",
   "Properties": {
      "PolicyText": {
         "Version":"2012-10-17",
         "Statement":[
            {
               "Sid":"ReplicationAccessCrossAccount",
               "Effect":"Allow",
               "Principal":{
                  "AWS":"arn:aws:iam::210987654321:root"
               },
               "Action":[
                  "ecr:CreateRepository",
                  "ecr:ReplicateImage"
               ],
               "Resource": "arn:aws:ecr:us-west-2:123456789012:repository/*"
             }
          ]
       }
    }
}
```

#### YAML<a name="aws-resource-ecr-registrypolicy--examples--Specify_a_registry_policy_for_a_private_registry--yaml"></a>

```
Resources:
  TestRegistryPolicy:
    Type: 'AWS::ECR::RegistryPolicy'
    Properties:
      PolicyText:
        Version: 2012-10-17
        Statement:
          - Sid: UpdatedRegistryPolicy
            Effect: Allow
            Principal:
              AWS: 'arn:aws:iam::210987654321:root'
            Action:
              - 'ecr:CreateRepository'
              - 'ecr:ReplicateImage'
            Resource: 'arn:aws:ecr:us-west-2:123456789012:repository/*'
```