# azure batch endpoint setup
deploy steps for azure batch endpoint
1. az login
2. az account get-access-token --query accessToken -o tsv
3. API_VERSION="2022-05-01"
4. environment setting
   az account set --subscription <subscription ID>
   az configure --defaults workspace=<AzureML workspace name> group=<resource group>
   az ml environment create --file docker-image-plus-conda.yml
