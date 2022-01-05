# Azure Synapse Serverless SQL Pool Database Project

Example of a Migration-Based deployment that deploys to an Azure Synapse serverless SQL Pool using Azure DevOps. Based on a blog post I wrote called 'CI/CD for serverless SQL pools using Azure DevOps' (https://bit.ly/3FWCHQl).

It uses a YAML pipeline, which is in the AzureDevOpsTemplates folder.

In order to use it in Azure Pipelines you can either import or fork this repository into another GitHub repository or into Azure Repos.

Afterwards, you can select the YAML file in Azure Pipelines and tailor the pipeline to suit your needs.

Please note that the databases have to exist in the serverless SQL Pools for this to work. In addition, you might want to create a file in Azure Data Lake storage that contains the heading used for the SchemaVersions table (https://dbup.readthedocs.io/en/latest/more-info/journaling/). From there, you can try using it as the SchemaVersions table in the code.

This repository is provided "as is" based on the MIT license (https://opensource.org/licenses/MIT). Basically, I am not responsible for your use of it.
