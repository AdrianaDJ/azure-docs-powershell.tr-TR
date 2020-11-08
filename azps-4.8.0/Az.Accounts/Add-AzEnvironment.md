---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: ba5a398e21543bc4b19c09309884ceb11fed3197
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273769"
---
# <span data-ttu-id="e7ddf-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7ddf-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="e7ddf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ddf-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ddf-103">Bir Azure Resource Manager örneğine uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="e7ddf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7ddf-104">SYNTAX</span></span>

### <span data-ttu-id="e7ddf-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7ddf-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ddf-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="e7ddf-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ddf-107">Yapılamadı</span><span class="sxs-lookup"><span data-stu-id="e7ddf-107">Discovery</span></span>
```
Add-AzEnvironment -AutoDiscover [-Uri <Uri>] [-Scope {Process | CurrentUser}]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ddf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7ddf-108">DESCRIPTION</span></span>
<span data-ttu-id="e7ddf-109">Add-AzEnvironment cmdlet 'i Azure Resource Manager cmdlet 'lerinin yeni bir Azure Kaynak Yöneticisi örneğine bağlanmasını sağlamak için uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="e7ddf-110">Yerleşik ortamlar Azurecsesli ve AzureChinaCloud hedefi Azure Resource Manager 'ın var olan genel örneklerini hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="e7ddf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7ddf-111">EXAMPLES</span></span>

### <span data-ttu-id="e7ddf-112">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="e7ddf-112">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              :
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="e7ddf-113">Bu örnekte, Add-AzEnvironment kullanarak örnek uç noktaları içeren yeni bir Azure ortamı oluşturduk ve cmdlet Set-AzEnvironment kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="e7ddf-114">Örnek 2: URI ile yeni bir ortam bulunuyor</span><span class="sxs-lookup"><span data-stu-id="e7ddf-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="e7ddf-115">Bu örnekte URI 'den yeni bir Azure ortamı keşfediyoruz https://configuredmetadata.net .</span><span class="sxs-lookup"><span data-stu-id="e7ddf-115">In this example, we are discovering a new Azure environment from the https://configuredmetadata.net Uri.</span></span>

## <span data-ttu-id="e7ddf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7ddf-116">PARAMETERS</span></span>

### <span data-ttu-id="e7ddf-117">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="e7ddf-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="e7ddf-118">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-119">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ddf-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-120">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="e7ddf-121">-AdTenant</span></span>
<span data-ttu-id="e7ddf-122">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-122">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-123">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="e7ddf-123">-ARMEndpoint</span></span>
<span data-ttu-id="e7ddf-124">Azure Resource Manager uç noktası</span><span class="sxs-lookup"><span data-stu-id="e7ddf-124">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-125">-Otomatik bulma</span><span class="sxs-lookup"><span data-stu-id="e7ddf-125">-AutoDiscover</span></span>
<span data-ttu-id="e7ddf-126">Varsayılan veya yapılandırılmış uç nokta aracılığıyla ortamları bulur.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ddf-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-128">Azure Analysis Services kaynağının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="e7ddf-130">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-131">-Azureattestationserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ddf-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-132">Azure kanıtlama hizmetinin, istenen belirtecin alıcısı olan kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="e7ddf-134">Azure kanıtlama hizmetinin DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="e7ddf-136">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="e7ddf-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="e7ddf-138">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="e7ddf-139">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="e7ddf-139">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="e7ddf-141">Azure Anahtar Kasası hizmetinin DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="e7ddf-142">Örnek vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="e7ddf-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ddf-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-144">İstenen belirtecin alıcısı olan Azure Key kasa veri hizmetinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="e7ddf-146">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ddf-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-148">Azure Log Analytics API ile kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-149">-Azuresynapseanaliz Ticsendporesourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ddf-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-150">Azure SYNAPSE Analytics 'in, istenen belirtecin alıcısı olan kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-151">-Azuresynapseanalyzer Ticsendpointsuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="e7ddf-152">Azure SYNAPSE Analytics 'in DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-153">-Batchendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="e7ddf-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="e7ddf-154">İstenen belirtecin alıcısı olan Azure toplu Iş hizmetinin kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="e7ddf-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-155">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="e7ddf-155">-DataLakeAudience</span></span>
<span data-ttu-id="e7ddf-156">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-156">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ddf-157">-DefaultProfile</span></span>
<span data-ttu-id="e7ddf-158">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e7ddf-158">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-159">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="e7ddf-159">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="e7ddf-160">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-160">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-161">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-161">-GalleryEndpoint</span></span>
<span data-ttu-id="e7ddf-162">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-162">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-163">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="e7ddf-163">-GraphAudience</span></span>
<span data-ttu-id="e7ddf-164">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-164">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-165">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-165">-GraphEndpoint</span></span>
<span data-ttu-id="e7ddf-166">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-166">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-167">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="e7ddf-167">-ManagementPortalUrl</span></span>
<span data-ttu-id="e7ddf-168">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-168">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-169">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7ddf-169">-Name</span></span>
<span data-ttu-id="e7ddf-170">Eklenecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-170">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-171">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="e7ddf-171">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="e7ddf-172">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-172">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-173">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-173">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="e7ddf-174">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-174">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-175">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e7ddf-175">-Scope</span></span>
<span data-ttu-id="e7ddf-176">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-176">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-177">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-177">-ServiceEndpoint</span></span>
<span data-ttu-id="e7ddf-178">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-178">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-179">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-179">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="e7ddf-180">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-180">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-181">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="e7ddf-181">-StorageEndpoint</span></span>
<span data-ttu-id="e7ddf-182">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-182">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-183">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="e7ddf-183">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="e7ddf-184">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-184">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-185">-URI</span><span class="sxs-lookup"><span data-stu-id="e7ddf-185">-Uri</span></span>
<span data-ttu-id="e7ddf-186">Ortamları getirmek için internet kaynağının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-186">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7ddf-187">-Confirm</span></span>
<span data-ttu-id="e7ddf-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ddf-189">-WhatIf</span></span>
<span data-ttu-id="e7ddf-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7ddf-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ddf-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ddf-192">CommonParameters</span></span>
<span data-ttu-id="e7ddf-193">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ddf-194">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7ddf-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ddf-195">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7ddf-195">INPUTS</span></span>

### <span data-ttu-id="e7ddf-196">System. String</span><span class="sxs-lookup"><span data-stu-id="e7ddf-196">System.String</span></span>

### <span data-ttu-id="e7ddf-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7ddf-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7ddf-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7ddf-198">OUTPUTS</span></span>

### <span data-ttu-id="e7ddf-199">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7ddf-199">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="e7ddf-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7ddf-200">NOTES</span></span>

## <span data-ttu-id="e7ddf-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7ddf-201">RELATED LINKS</span></span>

[<span data-ttu-id="e7ddf-202">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7ddf-202">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="e7ddf-203">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7ddf-203">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="e7ddf-204">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="e7ddf-204">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

