---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: a749c90a77c486e9e3e75f5a5fdbb48488a23559
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108051"
---
# <span data-ttu-id="4ef05-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ef05-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="4ef05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef05-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef05-103">Azure ortamının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ef05-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="4ef05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ef05-104">SYNTAX</span></span>

### <span data-ttu-id="4ef05-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ef05-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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

### <span data-ttu-id="4ef05-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="4ef05-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ef05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ef05-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef05-108">Set-AzEnvironment cmdlet, bir Azure örneğine bağlanmak için uç noktaları ve meta verileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ef05-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="4ef05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ef05-109">EXAMPLES</span></span>

### <span data-ttu-id="4ef05-110">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="4ef05-110">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
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
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="4ef05-111">Bu örnekte, Add-AzEnvironment kullanarak örnek uç noktaları içeren yeni bir Azure ortamı oluşturduk ve cmdlet Set-AzEnvironment kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="4ef05-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="4ef05-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ef05-112">PARAMETERS</span></span>

### <span data-ttu-id="4ef05-113">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="4ef05-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4ef05-114">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4ef05-115">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ef05-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4ef05-116">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4ef05-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="4ef05-117">-AdTenant</span></span>
<span data-ttu-id="4ef05-118">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4ef05-119">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="4ef05-119">-ARMEndpoint</span></span>
<span data-ttu-id="4ef05-120">Azure Resource Manager uç noktası.</span><span class="sxs-lookup"><span data-stu-id="4ef05-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="4ef05-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4ef05-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="4ef05-122">Azure Analysis Services kaynağının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4ef05-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="4ef05-124">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="4ef05-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="4ef05-125">-Azureattestationserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ef05-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="4ef05-126">Azure kanıtlama hizmetinin, istenen belirtecin alıcısı olan kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4ef05-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="4ef05-128">Azure kanıtlama hizmetinin DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="4ef05-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4ef05-130">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="4ef05-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4ef05-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4ef05-132">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="4ef05-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="4ef05-133">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4ef05-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4ef05-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4ef05-135">Azure Anahtar Kasası hizmetinin DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="4ef05-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="4ef05-136">Örnek vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="4ef05-136">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4ef05-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4ef05-138">İstenen belirtecin alıcısı olan Azure Key kasa veri hizmetinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4ef05-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4ef05-140">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="4ef05-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4ef05-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4ef05-142">Azure Log Analytics API ile kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="4ef05-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-143">-Azuresynapseanaliz Ticsendporesourceıd</span><span class="sxs-lookup"><span data-stu-id="4ef05-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="4ef05-144">Azure SYNAPSE Analytics 'in, istenen belirtecin alıcısı olan kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4ef05-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-145">-Azuresynapseanalyzer Ticsendpointsuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="4ef05-146">Azure SYNAPSE Analytics 'in DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="4ef05-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-147">-Batchendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ef05-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4ef05-148">İstenen belirtecin alıcısı olan Azure toplu Iş hizmetinin kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="4ef05-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-149">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="4ef05-149">-DataLakeAudience</span></span>
<span data-ttu-id="4ef05-150">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="4ef05-150">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef05-151">-DefaultProfile</span></span>
<span data-ttu-id="4ef05-152">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ef05-152">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ef05-153">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ef05-153">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4ef05-154">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-154">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4ef05-155">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-155">-GalleryEndpoint</span></span>
<span data-ttu-id="4ef05-156">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-156">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4ef05-157">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4ef05-157">-GraphAudience</span></span>
<span data-ttu-id="4ef05-158">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="4ef05-158">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4ef05-159">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-159">-GraphEndpoint</span></span>
<span data-ttu-id="4ef05-160">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-160">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4ef05-161">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="4ef05-161">-ManagementPortalUrl</span></span>
<span data-ttu-id="4ef05-162">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-162">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4ef05-163">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ef05-163">-Name</span></span>
<span data-ttu-id="4ef05-164">Değiştirilecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-164">Specifies the name of the environment to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-165">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4ef05-165">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4ef05-166">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-166">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4ef05-167">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-167">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4ef05-168">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-168">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4ef05-169">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="4ef05-169">-Scope</span></span>
<span data-ttu-id="4ef05-170">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="4ef05-170">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4ef05-171">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-171">-ServiceEndpoint</span></span>
<span data-ttu-id="4ef05-172">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-172">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4ef05-173">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-173">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4ef05-174">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-174">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4ef05-175">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4ef05-175">-StorageEndpoint</span></span>
<span data-ttu-id="4ef05-176">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="4ef05-176">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef05-177">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4ef05-177">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4ef05-178">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-178">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4ef05-179">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ef05-179">-Confirm</span></span>
<span data-ttu-id="4ef05-180">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ef05-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ef05-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ef05-181">-WhatIf</span></span>
<span data-ttu-id="4ef05-182">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ef05-182">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ef05-183">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ef05-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ef05-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef05-184">CommonParameters</span></span>
<span data-ttu-id="4ef05-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ef05-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef05-186">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ef05-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef05-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ef05-187">INPUTS</span></span>

### <span data-ttu-id="4ef05-188">System. String</span><span class="sxs-lookup"><span data-stu-id="4ef05-188">System.String</span></span>

### <span data-ttu-id="4ef05-189">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ef05-189">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ef05-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ef05-190">OUTPUTS</span></span>

### <span data-ttu-id="4ef05-191">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ef05-191">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4ef05-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ef05-192">NOTES</span></span>

## <span data-ttu-id="4ef05-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ef05-193">RELATED LINKS</span></span>

[<span data-ttu-id="4ef05-194">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ef05-194">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="4ef05-195">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ef05-195">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4ef05-196">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4ef05-196">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

