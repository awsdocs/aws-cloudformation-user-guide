# cfn\-hup<a name="cfn-hup"></a>

## Description<a name="cfn-hup-Description"></a>

The cfn\-hup helper is a daemon that detects changes in resource metadata and runs user\-specified actions when a change is detected\. This allows you to make configuration updates on your running Amazon EC2 instances through the UpdateStack API action\.

## Syntax<a name="cfn-hup-Syntax"></a>

```
cfn-hup --config|-c config.dir \
        --no-daemon \
        --verbose|-v
```

## Options<a name="cfn-hup-options"></a>


| Name | Description | Required | 
| --- | --- | --- | 
|   `--config\|-c config.dir`   |  Specifies the path that the cfn\-hup script looks for the `cfn-hup.conf` and the `hooks.d` directories\. On Windows, the default path is `system_drive\cfn`\. On Linux, the default path is `/etc/cfn`\.  |  No  | 
|   `--no-daemon`   |  Specify this option to run the cfn\-hup script once and exit\.  |  No  | 
|   `-v, --verbose `   |  Specify this option to use verbose mode\.  |  No  | 

## cfn\-hup\.conf configuration file<a name="cfn-hup-config-file"></a>

The cfn\-hup\.conf file stores the name of the stack and the AWS credentials that the cfn\-hup daemon targets\.

The cfn\-hup\.conf file uses the following format:

```
[main]
stack=<stack-name-or-id>
```


| Name | Description | Required | 
| --- | --- | --- | 
|   `stack`   |  A stack name or ID\. *Type*: String  |  Yes  | 
|   `credential-file`   |  An owner\-only credential file, in the same format used for the command line tools\. *Type*: String *Condition*: The `role` parameter supersedes this parameter\.  |  No  | 
|   `role`   |  The name of an IAM role that is associated with the instance\. *Type*: String  |  No  | 
|   `region`   |  The name of the AWS region containing the stack\. *Example*: `us-east-2`  |  No  | 
|   `umask`   |  The umask used by the cfn\-hup daemon\. This value can be specified with or without a leading 0\. In both cases, it is interpreted as an octal number \(very similar to the Linux `umask` command\)\. This parameter has no effect on Windows\. *Type*: Octal integer between `0` and `0777` *Default*: `022`, version 1\.4\-22 and higher\. The default value of `022` masks group and world write permissions, so files created by the cfn\-hup daemon are not group or world writable by default\. The default value for versions 1\.4\-21 and earlier is `0`, which masks nothing\.  |  No  | 
|   `interval`   |  The interval used to check for changes to the resource metadata in minutes *Type*: Number *Default*: `15`  |  No  | 
|   `verbose`   |  Specifies whether to use verbose logging\. *Type*: Boolean *Default*: `false`  |  No  | 

## hooks\.conf configuration file<a name="cfn-hup-hook-file"></a>

The user actions that the cfn\-hup daemon calls periodically are defined in the hooks\.conf configuration file\. The hooks\.conf file uses the following *format*:

```
[hookname]
triggers=post.add or post.update or post.remove
path=Resources.<logicalResourceId> (.Metadata or .PhysicalResourceId)(.<optionalMetadatapath>)
action=<arbitrary shell command>
runas=<runas user>
```

When the action is run, it is run in a copy of the current environment \(that cfn\-hup is in\), with CFN\_OLD\_METADATA set to the previous value of path, and CFN\_NEW\_METADATA set to the current value\.

The hooks configuration file is loaded at cfn\-hup daemon startup only, so new hooks will require the daemon to be restarted\. A cache of previous metadata values is stored at /var/lib/cfn\-hup/data/metadata\_db—you can delete this cache to force cfn\-hup to run all post\.add actions again\.


| Name | Description | Required | 
| --- | --- | --- | 
|   `hookname`   |  A unique name for this hook *Type*: String  |  Yes  | 
|   `triggers`   |  A comma\-delimited list of conditions to detect\. *Valid values*: `post.add`, `post.update`, or `post.remove` *Example*: `post.add, post.update`  |  Yes  | 
|   `path`   |  The path to the metadata object\. Supports an arbitrarily deep path within the Metadata block\.  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html)  |  Yes  | 
|   `action`   |  An arbitrary shell command that is run as given\.  |  Yes  | 
|   `runas`   |  A user to run the commands as\. Cfn\-hup uses the su command to switch to the user\.  |  Yes  | 

## hooks\.d directory<a name="cfn-hup-hooks-dir"></a>

To support composition of several applications deploying change notification hooks, cfn\-hup supports a directory named hooks\.d that is located in the hooks configuration directory\. You can place one or more additional hooks configuration files in the hooks\.d directory\. The additional hooks files must use the same layout as the hooks\.conf file\.

The cfn\-hup daemon parses and loads each file in this directory\. If any hooks in the hooks\.d directory have the same name as a hook in hooks\.conf, the hooks will be merged \(meaning hooks\.d will overwrite hooks\.conf for any values that both files specify\)\.

## Example<a name="cfn-hup-example"></a>

In the following template snippet, AWS CloudFormation triggers the `cfn-auto-reloader.conf` hooks file when you change the `AWS::CloudFormation::Init` resource that is associated with the `LaunchConfig` resource\.

### JSON<a name="cfn-hup-example.json"></a>

```
...
    "LaunchConfig": {
      "Type" : "AWS::AutoScaling::LaunchConfiguration",
      "Metadata" : {
        "QBVersion": {"Ref": "paramQBVersion"},
        "AWS::CloudFormation::Init" : {
...
              "/etc/cfn/hooks.d/cfn-auto-reloader.conf": {
                "content": { "Fn::Join": [ "", [
                  "[cfn-auto-reloader-hook]\n",
                  "triggers=post.update\n",
                  "path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init\n",
                  "action=/opt/aws/bin/cfn-init -v ",
                          "         --stack ", { "Ref" : "AWS::StackName" },
                          "         --resource LaunchConfig ",
                          "         --configsets wordpress_install ",
                          "         --region ", { "Ref" : "AWS::Region" }, "\n",
                  "runas=root\n"
                ]]},          
                "mode"  : "000400",
                "owner" : "root",
                "group" : "root"
              }
...
```

### YAML<a name="cfn-hup-example.yaml"></a>

```
...
  LaunchConfig:
    Type: "AWS::AutoScaling::LaunchConfiguration"
    Metadata:
      QBVersion: !Ref paramQBVersion
      AWS::CloudFormation::Init:
...
            /etc/cfn/hooks.d/cfn-auto-reloader.conf:
              content: !Sub |
                [cfn-auto-reloader-hook]
                triggers=post.update
                path=Resources.LaunchConfig.Metadata.AWS::CloudFormation::Init
                action=/opt/aws/bin/cfn-init -v --stack ${AWS::StackName} --resource LaunchConfig --configsets wordpress_install --region ${AWS::Region}
                runas=root
              mode: "000400"
              owner: "root"
              group: "root"
...
```

### Additional example<a name="w7739ab1c33c42c35c15b8"></a>

For a sample template, see [Deploying applications on Amazon EC2 with AWS CloudFormation](deploying.applications.md)\.