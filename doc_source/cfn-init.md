# cfn\-init<a name="cfn-init"></a>

## Description<a name="cfn-init-Description"></a>

The cfn\-init helper script reads template metadata from the AWS::CloudFormation::Init key and acts accordingly to:
+ Fetch and parse metadata from AWS CloudFormation
+ Install packages
+ Write files to disk
+ Enable/disable and start/stop services

**Note**  
If you use cfn\-init to update an existing file, it creates a backup copy of the original file in the same directory with a \.bak extension\. For example, if you update `/path/to/file_name`, the action produces two files: `/path/to/file_name.bak` contains the original file's contents and `/path/to/file_name` contains the updated contents\.

For information about the template metadata, see [AWS::CloudFormation::Init](aws-resource-init.md)\.

**Note**  
cfn\-init does not require credentials, so you do not need to use the `--access-key`, `--secret-key`, `--role`, or `--credential-file` options\. However, if no credentials are specified, AWS CloudFormation checks for stack membership and limits the scope of the call to the stack that the instance belongs to\.

## Syntax<a name="cfn-init-Syntax"></a>

```
cfn-init --stack|-s stack.name.or.id \
         --resource|-r logical.resource.id \
         --region region
         --access-key access.key \
         --secret-key secret.key \
         --role rolename\
         --credential-file|-f credential.file \
         --configsets|-c config.sets \
         --url|-u service.url \
         --http-proxy HTTP.proxy \
         --https-proxy HTTPS.proxy \
         --verbose|-v
```

## Options<a name="cfn-init-options"></a>


| Name | Description | Required | 
| --- | --- | --- | 
|   `-s, --stack`   |  Name of the Stack\. *Type*: String *Default*: None *Example*: `-s { "Ref" : "AWS::StackName" },`  |  Yes  | 
|   `-r, --resource `   |  The logical resource ID of the resource that contains the metadata\. *Type*: String *Example*: `-r WebServerHost`  |  Yes  | 
|   `--region`   |  The AWS CloudFormation regional endpoint to use\. *Type*: String *Default*: `us-east-1` *Example*: `--region ", { "Ref" : "AWS::Region" },`  |  No  | 
|   `--access-key`   |  AWS access key for an account with permission to call DescribeStackResource on AWS CloudFormation\. The credential file parameter supersedes this parameter\. *Type*: String  |  No  | 
|   `--secret-key`   |  AWS secret access key that corresponds to the specified AWS access key\. *Type*: String  |  No  | 
|   `--role`   |  The name of an IAM role that is associated with the instance\. *Type*: String Condition: The credential file parameter supersedes this parameter\.  |  No  | 
|   `-f, --credential-file`   |  A file that contains both a secret access key and an access key\. The credential file parameter supersedes the \-\-role, \-\-access\-key, and \-\-secret\-key parameters\. *Type*: String  |  No  | 
|   `-c, --configsets`   |  A comma\-separated list of configsets to run \(in order\)\. *Type*: String *Default*: `default`  |  No  | 
|   `-u, --url`   |  The AWS CloudFormation endpoint to use\. *Type*: String  |  No  | 
|  `--http-proxy`  |  An HTTP proxy \(non\-SSL\)\. Use the following format: `http://user:password@host:port` *Type*: String  |  No  | 
|  `--https-proxy`  |  An HTTPS proxy\. Use the following format: `https://user:password@host:port` *Type*: String  |  No  | 
|  `-v`  |  Verbose output\. This is useful for debugging cases where cfn\-init is failing to initialize\.   To debug initialization events, you should turn DisableRollback on\. You can do this by using the AWS CloudFormation console, selecting *Show Advanced Options*, and then setting "Rollback on failure" to "No"\. You can then SSH into the console and read the logs at /var/log/cfn\-init\.log\.   |  No  | 

## Example<a name="cfn-init-Examples"></a>

### Amazon Linux example<a name="w7739ab1c33c42c29b9b2"></a>

The following snippet shows the `UserData` property of an EC2 instance, which runs the `InstallAndRun` configset that is associated with the `WebServerInstance` resource\.

For a complete example template, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.

#### JSON<a name="cfn-init-example.json"></a>

```
"UserData" : { "Fn::Base64" :
  { "Fn::Join" : ["", [
     "#!/bin/bash -xe\n",
     "# Install the files and packages from the metadata\n",
     "/opt/aws/bin/cfn-init -v ",
     "         --stack ", { "Ref" : "AWS::StackName" },
     "         --resource WebServerInstance ",
     "         --configsets InstallAndRun ",
     "         --region ", { "Ref" : "AWS::Region" }, "\n"
  ]]}
}
```

#### YAML<a name="cfn-init-example.yaml"></a>

```
UserData: !Base64 
  'Fn::Join':
    - ''
    - - |
        #!/bin/bash -xe
      - |
        # Install the files and packages from the metadata
      - '/opt/aws/bin/cfn-init -v '
      - '         --stack '
      - !Ref 'AWS::StackName'
      - '         --resource WebServerInstance '
      - '         --configsets InstallAndRun '
      - '         --region '
      - !Ref 'AWS::Region'
      - |+
```