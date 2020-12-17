# AWS CloudFormation Designer interface overview<a name="working-with-templates-cfn-designer-overview"></a>

[Designer](https://console.aws.amazon.com/cloudformation/designer) has four panes\. The **canvas** pane shows a diagram of your template resources so that you can see them and their relationships at a glance\. To add resources to your template, you drag them from the **Resources types** pane onto the **canvas** pane\. Use the **Integrated JSON and YAML editor** pane to specify template details, such as resource properties or template parameters\. After you've modified the template, you can save it to a local file or to an Amazon S3 bucket\. When you convert a valid template from JSON to YAML or vice\-versa, the **Messages** pane displays a success or failure message\. When you open or validate an invalid template, the **Messages** pane displays validation errors\.

**Note**  
Designer cannot show or modify running resources in your stacks; use it only for creating, modifying, and saving templates\.

The following figure illustrates the Designer panes and its main components\.

** Designer panes and components**

![\[A screenshot of the Designer with its panes and components numbered.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-overview.png)

1\. Toolbar  
The toolbar provides quick access to commands for common actions, such as opening and saving templates, undoing or redoing changes, creating a stack, and validating your template\. You can also download the diagram as an image, get help, or refresh the diagram in the canvas pane\.

2\. Resource types pane  
The **Resource types** pane lists all of the template resources that you can add to your template, categorized by their AWS service name\. You add resources by dragging them from the **Resource types** pane to the canvas\. Most of the supported resources are listed in the [AWS resource and property types reference](aws-template-resource-type-ref.md)\. The **Resource types** pane doesn't list connecting resources, such as the `AWS::EC2::SubnetRouteTableAssociation` resource\. You create these resources when you connect the relevant resources, such as when you connect a route table to a subnet\. For more information, see [Canvas pane](working-with-templates-cfn-designer-canvas-details.md)\.  
Designer can display only AWS CloudFormation\-supported resource types\. It cannot display other entities, such as Availability Zones \(AZs\) or the resources of a nested stack\.

3\. Canvas pane  
The **canvas** pane displays your template resources as a diagram\. You use it to add or remove resources, create relationships between resources, and arrange their layout\. The changes that you make in the **canvas** automatically modify the template's JSON or YAML\. For more information, see [Canvas pane](working-with-templates-cfn-designer-canvas-details.md)\.

4\. Fit to window button  
A button that resizes the **canvas** pane to fit your template's diagram\.

5\. Full screen and Split screen buttons  
Buttons to select different views of Designer\. You can select a full\-screen view of the canvas, a full\-screen view of the **Integrated JSON and YAML editor**, or a split\-screen view of the canvas and editor\.

6\. Integrated JSON and YAML editor pane  
In the integrated editor, you specify the details of your template, such as resource properties or template parameters\. When you select an item in the **canvas**, Designer highlights the related JSON or YAML in the editor\. After editing the JSON or YAML, you must refresh the **canvas** \(choose ![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-refresh.png)\) to update the diagram\. You can convert a valid template between JSON and YAML by selecting the appropriate radio button in **Choose template language**\. Designer can only convert valid YAML or valid JSON templates\. If the conversion succeeds, the **Messages** pane displays a message like: *Successfully converted the template to YAML*\. AWS CloudFormation Designer does not preserve formatting when converting a template\.  
We recommend that you do not add `#` YAML comments to your templates in Designer\. If your YAML template has `#` comments, Designer doesn't preserve those comments when editing the YAML or converting to JSON\. If you edit or modify your template in Designer \(for example, if you drag a resource on the canvas\), your comments are lost\.
Once you choose a template language, any new resources you drag onto the canvas will be created in the language you have selected\. To change back to another language, make sure your template is valid and then select **YAML** or **JSON** where it says **Choose template language**\.  
For more information, see [Integrated JSON and YAML editor](working-with-templates-cfn-designer-json-editor.md)\.

7\. Messages pane  
When you convert a template from JSON to YAML or vice\-versa, the **Messages** pane displays a success or failure message\. When you open, validate, or attempt to create a stack with an invalid template, the **Messages** pane displays validation errors\.