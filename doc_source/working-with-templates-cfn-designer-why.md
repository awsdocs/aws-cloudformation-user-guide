# Why use AWS CloudFormation Designer?<a name="working-with-templates-cfn-designer-why"></a>

AWS CloudFormation Designer \(Designer\) provides the following benefits: it allows you to see graphic representations of the resources in your template, it simplifies template authoring, and it simplifies template editing\.

## Visualize template resources<a name="w7739ab1c27c17c11b5"></a>

Parsing JSON\- or YAML\-formatted text files to see the resources that are in your template and their relationships can be difficult\. In Designer, you can see a graphic representation of the resources that are included in a template and how they relate to each other\.

Designer defines the information about your resources, such as their size and relative position, in template metadata\. When you open a template, Designer automatically adds this metadata so that the current layout is preserved when you save your template\. When you reopen a template in Designer, it displays the diagram exactly as it appeared when you last saved the template\.

All layout information is defined in the `AWS::CloudFormation::Designer` metadata key, which is used only by Designer and won't interfere with creating AWS CloudFormation stacks\. The following example of template metadata shows the layout information that Designer adds to a template as metadata: 

### JSON<a name="working-with-templates-cfn-designer-example-template-metadata.json"></a>

```
"Metadata": {
  "AWS::CloudFormation::Designer": {
    "6b56eaae-0bb6-4215-aad6-12345EXAMPLE": {
      "size": {
        "width": 60,
        "height": 60
      },
      "position": {
        "x": 340,
        "y": 430
      },
      "z": 2,
      "parent": "21ccc9b0-29e9-4a86-9cf2-12345EXAMPLE",
      "embeds": [],
      "ismemberof": [
        "c3eead73-6a76-4532-9268-12345EXAMPLE"
      ]
    },
...
```

### YAML<a name="working-with-templates-cfn-designer-example-template-metadata.yaml"></a>

```
Metadata:
  'AWS::CloudFormation::Designer':
    6b56eaae-0bb6-4215-aad6-12345EXAMPLE:
      size:
        width: 60
        height: 60
      position:
        x: 340
        'y': 430
      z: 2
      parent: 21ccc9b0-29e9-4a86-9cf2-12345EXAMPLE
      embeds: []
      ismemberof:
        - c3eead73-6a76-4532-9268-12345EXAMPLE
...
```

## Simplify template authoring<a name="w7739ab1c27c17c11b7"></a>

When you author template resources in a text editor, you must manually edit JSON or YAML, which can be tedious and error\-prone\. By using Designer, you spend less time manually coding your templates and more time designing your AWS infrastructure\. In Designer, you drag and drop new resources to add them to your template, and you drag connections between resources to establish relationships\. Designer automatically modifies the JSON or YAML\.

When you create templates, Designer enforces some basic relationships between resources to help you create valid templates\. For example, you cannot add an EC2 instance directly inside a VPC; you must add the instance inside a subnet in the VPC\.

You can also validate a template directly in Designer\. It provides the same level of validation as the `[ValidateTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/)` API call, which checks that the JSON or YAML syntax is valid, that all referenced parameters are declared, and that there are no circular dependencies\.

## Simplify editing with the integrated JSON and YAML editor<a name="w7739ab1c27c17c11b9"></a>

With the integrated editor, you can make all of your template modifications in the AWS CloudFormation console\. You don't need to use a separate text editor to modify and save your templates\. The integrated editor also provides an auto\-complete feature that lists all property names for a resource, so you don't need to look them up or memorize them\. In addition, you can use the integrated editor to convert JSON templates to YAML and vice versa\.