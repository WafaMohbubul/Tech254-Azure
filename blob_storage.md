## Blob Storage 

#### Task 1: Connect to Azure CLI
1. Download Azure CLI - `curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash`

2. Login - `az login`
3. Copy and paste URl and code when prompted

#### Task 2: Create Blob (container)

```
az storage account create 
    --name tech254wafastorage 
    --resource-group tech254 
    --location uksouth 
    --sku Standard_ZRS`
```

#### Task 3: Create Container

```
az storage container create \
     --account-name tech254samihastorage \
     --name testcontainer \
     --auth-mode login
```

#### Task 4: Upload Blob 

1. Copy and paste this is GitBash terminal
```commandline
az storage blob upload \
     --account-name tech254samihastorage \
     --container-name testcontainer \
     --name newtest.txt \
     --file test.txt \
     --auth-mode login
```

#### Task 5: Add cat image
1. Find cat image
2. curl -o filename.jpg URL_of_the_image = `curl -o cat.jpg https://t4.ftcdn.net/jpg/00/97/58/97/360_F_97589769_t45CqXyzjz0KXwoBZT9PRaWGHRk5hQqQ.jpg`

#### Task 6: upload blob with cat image

```commandline
az storage blob upload \
     --account-name tech254wafastorage \
     --container-name testcontainer \
     --name cat.jpg \
     --file cat.jpg \
     --auth-mode login
```