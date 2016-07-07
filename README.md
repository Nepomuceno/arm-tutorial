# ARM-tutorial
Tutorial on how to build advanced templates with Azure resource manager.

#Pre-Requisites
You will need to have the Azure Command Line Tools instaled on you PC. To do this, you can use Powershell *or* the Azure CLI

To install Azure CLI, run the following;

```
npm install azure-cli -g
```

or to install the Powershell Tools, you can use;

```
Install-Module Azure
``` 

#Running the examples

To execute any of these templates, execute for xplat

```shell
azure group deployment create -f <template-file> -e <parameter-file> <resource-group-name> <deployment-name>
```

or for Powershell

```
New-AzureRmResourceGroupDeployment -ResourceGroupName <resource-group-name> -TemplateFile <template-file> -TemplateParameterFile <parameter-file>
```

#Content
You can find the following templates in the _examples_ folder of this repo.

##101-base.json
This basic template is simply the basic areas of each one of the resources, and how to utilize the basic functionality.

On the parameters there is just the basic usage of a parameter file.

##102-parameter-customization.json

This template shows how to have restrictions on parameters and to make it more sensible to you use case.

The parameter file has invalid values on purpose to show how to validate the parameters of a template.

##103-invoking-other-templates.json

On this I show how to use nested templates and how can you deploy using them. 

##201-using-object-parameters.json

This shows the basic usage of an object parameter, and how you can customize it to fit your needs and do not require multiple parameters to be passed.

##202-enable-templates.json

This template shows how to combine using different templates to being able to enable parts of your template only, on this example with the parameter `Enable` you can create or not the redis template.

##301-TShirt-size-template.json

Using the TShirt approach, you basically bucket what kind of sizes people can use for your template puffing values, like `small` `medium` `large` enabling others to use your template easily.

## Next steps

- The best source for examples for templates [Quick start templates](https://github.com/Azure/azure-quickstart-templates)
- To learn about creating Resource Manager templates, see [Authoring templates](https://azure.microsoft.com/en-us/documentation/articles/resource-group-authoring-templates/)
- To understand the functions you can use in an Resource Manager template, see [Template functions](https://azure.microsoft.com/en-us/documentation/articles/resource-group-template-functions/)
- For guidance on designing your templates, see [Best practices for designing Azure Resource Manager templates](https://azure.microsoft.com/en-us/documentation/articles/best-practices-resource-manager-design-templates/)
