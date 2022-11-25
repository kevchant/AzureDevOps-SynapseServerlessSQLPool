# Azure Synapse Serverless SQL Pool Database Project

Example of a Migration-Based deployment that deploys to an Azure Synapse serverless SQL Pool using Azure DevOps. Based on a blog post I wrote called '[CI/CD for serverless SQL pools using Azure DevOps](https://bit.ly/3FWCHQl)'.

You can see this template in action in the [video for the November 2022 edition of the Azure Synapse Analytics and MVP series](https://www.youtube.com/watch?v=87gNrueVRFU). Click on the link to view.

A brief overview is below. However, there is also a [wiki for this repository](https://github.com/kevchant/AzureDevOps-SynapseServerlessSQLPool/wiki).

It contains an example YAML file that you can use as a YAML pipeline in Azure Pipelines. You can find it in the AzureDevOpsTemplates folder. In order to use it in Azure Pipelines you can either import or fork this repository into another GitHub repository, or into [Azure Repos](https://bit.ly/3s4uO77).

Afterwards, you can select the YAML file in Azure Pipelines and tailor the pipeline to suit your needs. You can find a guide on how to select the YAML file whilst setting up a YAML Pipeline this in a blog post I wrote called '[Connect a Database Project in Azure Repos to Azure Pipelines](https://bit.ly/3uF1Iv9)'.

You can find the recommended variables inside the YAML file. Avoid putting sensitive information directly into the YAML file (like your connection details). One thing I must stress here is that the password MUST be wrapped in single quotes in the secret for it to work.

You can use the logic in 'Classic Editor' instead by adding the tasks into the GUI and transferring the logic over. Alternatively, you can build an artifact for it using the 'Classic Editor' and use the 'Releases' feature for deployments. Personally, I prefer doing the deployment using a YAML pipeline.

Please note that the databases must already exist in the serverless SQL Pool for this to work. 

In addition, you might want to create a file in Azure Data Lake storage that contains the headings used for the SchemaVersions table (https://dbup.readthedocs.io/en/latest/more-info/journaling/). From there, you can try using it as the SchemaVersions table in the code to log updates.

This repository is provided "as is" based on the [MIT license](https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
