---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: ed50d8e25dca0998e7e3e026783fe4ec78e6ce7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572685"
---
# <span data-ttu-id="372bd-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="372bd-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="372bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372bd-102">SYNOPSIS</span></span>
<span data-ttu-id="372bd-103">Bir Azure Resource Manager örneğine uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="372bd-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="372bd-104">SYNTAX</span></span>

### <span data-ttu-id="372bd-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="372bd-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372bd-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="372bd-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="372bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="372bd-107">DESCRIPTION</span></span>
<span data-ttu-id="372bd-108">Add-AzureRmEnvironment cmdlet 'i Azure Resource Manager cmdlet 'lerinin yeni bir Azure Kaynak Yöneticisi örneğine bağlanmasını sağlamak için uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="372bd-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="372bd-109">Yerleşik ortamlar Azurecsesli ve AzureChinaCloud hedefi Azure Resource Manager 'ın var olan genel örneklerini hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="372bd-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="372bd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="372bd-110">EXAMPLES</span></span>

### <span data-ttu-id="372bd-111">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="372bd-111">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment `
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
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.
```

## <span data-ttu-id="372bd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="372bd-112">PARAMETERS</span></span>

### <span data-ttu-id="372bd-113">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="372bd-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="372bd-114">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="372bd-115">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="372bd-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="372bd-116">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="372bd-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="372bd-117">-AdTenant</span></span>
<span data-ttu-id="372bd-118">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="372bd-119">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="372bd-119">-ARMEndpoint</span></span>
<span data-ttu-id="372bd-120">Azure Resource Manager uç noktası</span><span class="sxs-lookup"><span data-stu-id="372bd-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="372bd-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="372bd-122">Azure Analysis Services hizmet uç noktalarının DNS soneki</span><span class="sxs-lookup"><span data-stu-id="372bd-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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


### <span data-ttu-id="372bd-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="372bd-124">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="372bd-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="372bd-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="372bd-126">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="372bd-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="372bd-127">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="372bd-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="372bd-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="372bd-129">Anahtar Kasası Hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="372bd-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="372bd-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="372bd-131">Anahtar Kasası Hizmetleri isteklerine yetki veren erişim belirteçlerinin kitlesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="372bd-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="372bd-133">Işlemsel Öngörüler sorgu erişimi için uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

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

### <span data-ttu-id="372bd-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="372bd-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="372bd-135">Işlemsel Öngörüler Hizmetleri için isteklere yetki veren erişim belirteçlerinin Audience öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

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

### <span data-ttu-id="372bd-136">-Batchendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="372bd-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="372bd-137">İstenen belirtecin alıcısı olan Azure toplu Iş hizmetinin kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="372bd-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="372bd-138">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="372bd-138">-DataLakeAudience</span></span>
<span data-ttu-id="372bd-139">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="372bd-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="372bd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372bd-140">-DefaultProfile</span></span>
<span data-ttu-id="372bd-141">Azure ile iletişimde kullanılan credeetnaıls, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="372bd-141">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="372bd-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="372bd-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="372bd-143">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="372bd-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="372bd-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-144">-GalleryEndpoint</span></span>
<span data-ttu-id="372bd-145">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="372bd-146">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="372bd-146">-GraphAudience</span></span>
<span data-ttu-id="372bd-147">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="372bd-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="372bd-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-148">-GraphEndpoint</span></span>
<span data-ttu-id="372bd-149">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="372bd-150">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="372bd-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="372bd-151">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="372bd-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="372bd-152">-Name</span></span>
<span data-ttu-id="372bd-153">Eklenecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-153">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="372bd-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="372bd-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="372bd-155">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="372bd-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="372bd-157">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="372bd-158">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="372bd-158">-Scope</span></span>
<span data-ttu-id="372bd-159">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="372bd-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="372bd-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-160">-ServiceEndpoint</span></span>
<span data-ttu-id="372bd-161">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="372bd-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="372bd-163">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="372bd-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="372bd-164">-StorageEndpoint</span></span>
<span data-ttu-id="372bd-165">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="372bd-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="372bd-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="372bd-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="372bd-167">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="372bd-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="372bd-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="372bd-168">-Confirm</span></span>
<span data-ttu-id="372bd-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="372bd-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372bd-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372bd-170">-WhatIf</span></span>
<span data-ttu-id="372bd-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="372bd-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="372bd-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="372bd-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372bd-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372bd-173">CommonParameters</span></span>
<span data-ttu-id="372bd-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="372bd-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372bd-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372bd-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372bd-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="372bd-176">INPUTS</span></span>

### <span data-ttu-id="372bd-177">System. String</span><span class="sxs-lookup"><span data-stu-id="372bd-177">System.String</span></span>

### <span data-ttu-id="372bd-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="372bd-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="372bd-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="372bd-179">OUTPUTS</span></span>

### <span data-ttu-id="372bd-180">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="372bd-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="372bd-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="372bd-181">NOTES</span></span>

## <span data-ttu-id="372bd-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="372bd-182">RELATED LINKS</span></span>

[<span data-ttu-id="372bd-183">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="372bd-183">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="372bd-184">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="372bd-184">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="372bd-185">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="372bd-185">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

