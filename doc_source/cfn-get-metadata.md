# cfn\-get\-metadata<a name="cfn-get-metadata"></a>

## Description<a name="cfn-get-metadata-Description"></a>

You can use the cfn\-get\-metadata helper script to fetch a metadata block from AWS CloudFormation and print it to standard out\. You can also print a sub\-tree of the metadata block if you specify a key\. However, only top\-level keys are supported\.

**Note**  
cfn\-get\-metadata does not require credentials, so you do not need to use the `--access-key`, `--secret-key`, `--role`, or `--credential-file` options\. However, if no credentials are specified, AWS CloudFormation checks for stack membership and limits the scope of the call to the stack that the instance belongs to\.

## Syntax<a name="cfn-get-metadata-Syntax"></a>

```
cfn-get-metadata --access-key access.key \
                 --secret-key secret.key \
                 --credential-file|f credential.file \
                 --key|k key \
                 --stack|-s stack.name.or.id \
                 --resource|-r logical.resource.id \
                 --role IAM.role.name \
                 --url|-u service.url \
                 --region region
```

## Options<a name="cfn-get-metadata-options"></a>


| Name | Description | Required | 
| --- | --- | --- | 
|   `-k, --key`   |  For a key\-value pair, returns the name of the key for the value that you specified\. *Type*: String *Example*: For `{ "Key1": "SampleKey1", "Key2": "SampleKey2" }`, `cfn-get-metadata -k Key2` returns `SampleKey2`\.  |  No  | 
|   `-s, --stack`   |  Name of the Stack\. *Type*: String *Default*: None *Example*: `-s { "Ref" : "AWS::StackName" },`  |  Yes  | 
|   `-r, --resource`   |  The logical resource ID of the resource that contains the metadata\. *Type*: String *Example*: `-r WebServerHost`  |  Yes  | 
|  `--role` \(resource signaling only\)  |  The name of an IAM role that is associated with the instance\. *Type*: String Condition: The credential file parameter supersedes this parameter\.  |  No  | 
|   `--region`   |  The region to derive the AWS CloudFormation URL from\. *Type*: String *Default*: None *Example*: `--region ", { "Ref" : "AWS::Region" },`  |  No  | 
|   `--access-key`   |  AWS Access Key for an account with permission to call DescribeStackResource on AWS CloudFormation\. *Type*: String Condition: The credential file parameter supersedes this parameter\.  |  Conditional  | 
|   `--secret-key`   |  AWS Secret Key that corresponds to the specified AWS Access Key\. *Type*: String Condition: The credential file parameter supersedes this parameter\.  |  Conditional  | 
|   `-f, --credential-file`   |  A file that contains both a secret key and an access key\. *Type*: String Condition: The credential file parameter supersedes the \-\-access\-key and \-\-secret\-key parameters\.  |  Conditional  | 