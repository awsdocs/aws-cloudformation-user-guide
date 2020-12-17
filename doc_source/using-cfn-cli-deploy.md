# Quickly deploying templates with transforms<a name="using-cfn-cli-deploy"></a>

AWS CloudFormation requires you to use a change set to create a template that includes transforms\. Instead of independently creating and then executing a change set, use the `aws cloudformation deploy` command\. When you run this command, it creates a change set, executes the change set, and then terminates\. This command reduces the numbers of required steps when you create or update a stack that includes transforms\.

The following command creates a new stack by using the `my-template.json` template\.

```
aws cloudformation deploy --template /path_to_template/my-template.json --stack-name my-new-stack --parameter-overrides Key1=Value1 Key2=Value2
```

For more information, see the `aws cloudformation deploy` command in the [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/index.html)