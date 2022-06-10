
https://ochzhen.com/blog/create-resource-group-azure-bicep
https://ochzhen.com/blog/five-ways-to-deploy-azure-bicep


git
…or create a new repository on the command line
echo "# bicep1" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/funmonkee/bicep1.git
git push -u origin main

…or push an existing repository from the command line
git remote add origin https://github.com/funmonkee/bicep1.git
git branch -M main
git push -u origin main


git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin <https://github.com/funmonkee/bicep1.git>
git push -u origin main

commands

az account list
az account list --refresh --query "[?contains(name,'Ent')].id" --output table
az account list --refresh --query "[?contains(name,'Ent')]" --output table

create testrg in portal

az configure --defaults group=testrg
az deployment group create --template-file main.bicep

az deployment group list --output table

az deployment group create --template-file main.bicep

az deployment group create \
  --template-file main.bicep \
  --parameters environmentType=nonprod

ex2
...

ex3
az deployment group create \
  --template-file main.bicep \
  --parameters environmentType=nonprod


ex4
  az deployment group create \
  --template-file main.bicep \
  --parameters main.parameters.dev.json

  complex007
  C0mplexPassw0rd

  keyVault007ts

keyVaultName='keyVault007ts' # A unique name for the key vault.
login='complex007' # The login that you used in the previous step.
password='C0mplexPassw0rd' # The password that you used in the previous step.

az keyvault create --name $keyVaultName --location westus --enabled-for-template-deployment true
az keyvault secret set --vault-name $keyVaultName --name "sqlServerAdministratorLogin" --value $login
az keyvault secret set --vault-name $keyVaultName --name "sqlServerAdministratorPassword" --value $password

# keyvault id
az keyvault show --name $keyVaultName --query id --output tsv
> /subscriptions/82074a21-3b88-451b-88bf-4d86c81c6064/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/keyVault007ts

ex5

