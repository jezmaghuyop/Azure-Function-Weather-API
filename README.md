# Azure Function Weather API
This is a basic Azure Function written in C# that consumes a 3rd party API from https://www.weatherapi.com/ and integrates Azure KeyVault to hide the API Keys.

## Helpful Azure CLI Commands
This will set the default subscription to use when running commands.
-s = is shorthand for subscription
```
az account set -s (subscription name or subscription id)
```

This will list all the function app in your subscription
```
az functionapp list
```

it will automatically populate your local.settings.json with list of properties from Configuration > Application Settings in Azure Portal
```
func azure functionapp fetch-app-settings FUNCTION_NAME
```

this will encrypt the values in local.settings.json
```
func settings encrypt
```

this will decrypt the values
```
func settings decrypt
```
