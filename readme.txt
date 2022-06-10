
https://ochzhen.com/blog/create-resource-group-azure-bicep
https://ochzhen.com/blog/five-ways-to-deploy-azure-bicep


commands

az account list
az account list --refresh --query "[?contains(name,'Ent')].id" --output table
az account list --refresh --query "[?contains(name,'Ent')]" --output table

create testrg in portal

az configure --defaults group=testrg
az deployment group create --template-file main.bicep

az deployment group list --output table

az deployment group create --template-file main.bicep


