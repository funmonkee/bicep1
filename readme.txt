
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