---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 468abd4edc2e60ec0e13c80d345bafdac7ad2be5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764013"
---
# <span data-ttu-id="0a6e1-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="0a6e1-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="0a6e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6e1-103">Azure ortamının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a6e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a6e1-104">SYNTAX</span></span>

### <span data-ttu-id="0a6e1-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a6e1-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>] 
 [-Scope <ContextModificationScope>][-DefaultProfile <IAzureContextContainer>] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a6e1-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="0a6e1-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId <String>]] [[-AzureOperationalInsightsEndpoint] <String>] 
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [-Scope <ContextModificationScope>] 
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a6e1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a6e1-107">DESCRIPTION</span></span>
<span data-ttu-id="0a6e1-108">Set-AzureRMEnvironment cmdlet, bir Azure örneğine bağlanmak için uç noktaları ve meta verileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="0a6e1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a6e1-109">EXAMPLES</span></span>

### <span data-ttu-id="0a6e1-110">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="0a6e1-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

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
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

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
```

<span data-ttu-id="0a6e1-111">Bu örnekte, Add-AzureRmEnvironment ' ı kullanarak örnek uç noktaları olan yeni bir Azure ortamı oluşturduk ve ardından set-AzureRmEnvironment cmdlet 'ini kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="0a6e1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a6e1-112">PARAMETERS</span></span>

### <span data-ttu-id="0a6e1-113">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="0a6e1-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="0a6e1-114">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-115">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="0a6e1-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="0a6e1-116">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="0a6e1-117">-AdTenant</span></span>
<span data-ttu-id="0a6e1-118">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-118">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-119">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="0a6e1-119">-ARMEndpoint</span></span>
<span data-ttu-id="0a6e1-120">Azure Resource Manager uç noktası.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-120">The Azure Resource Manager endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0a6e1-121">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="0a6e1-122">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="0a6e1-122">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0a6e1-123">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="0a6e1-124">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-124">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="0a6e1-125">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="0a6e1-125">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-126">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0a6e1-126">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="0a6e1-127">Anahtar Kasası Hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-127">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-128">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0a6e1-128">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="0a6e1-129">Anahtar Kasası Hizmetleri isteklerine yetki veren erişim belirteçlerinin kitlesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-129">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-130">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="0a6e1-130">-DataLakeAudience</span></span>
<span data-ttu-id="0a6e1-131">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-131">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6e1-132">-DefaultProfile</span></span>
<span data-ttu-id="0a6e1-133">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-133">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-134">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="0a6e1-134">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="0a6e1-135">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-135">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-136">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-136">-GalleryEndpoint</span></span>
<span data-ttu-id="0a6e1-137">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-137">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-138">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="0a6e1-138">-GraphAudience</span></span>
<span data-ttu-id="0a6e1-139">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-139">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-140">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-140">-GraphEndpoint</span></span>
<span data-ttu-id="0a6e1-141">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-141">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-142">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="0a6e1-142">-ManagementPortalUrl</span></span>
<span data-ttu-id="0a6e1-143">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-143">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a6e1-144">-Name</span></span>
<span data-ttu-id="0a6e1-145">Değiştirilecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-145">Specifies the name of the environment to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-146">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="0a6e1-146">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="0a6e1-147">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-147">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-148">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-148">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="0a6e1-149">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-149">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-150">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="0a6e1-150">-Scope</span></span>
<span data-ttu-id="0a6e1-151">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-151">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-152">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-152">-ServiceEndpoint</span></span>
<span data-ttu-id="0a6e1-153">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-153">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-154">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0a6e1-154">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="0a6e1-155">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-155">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-156">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-156">-StorageEndpoint</span></span>
<span data-ttu-id="0a6e1-157">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-157">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-158">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="0a6e1-158">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="0a6e1-159">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-159">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-160">-Batchendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="0a6e1-160">-BatchEndpointResourceId</span></span>
<span data-ttu-id="0a6e1-161">İstenen belirtecin alıcısı olan Azure toplu Iş hizmetinin kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="0a6e1-161">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-162">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a6e1-162">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="0a6e1-163">Işlemsel Öngörüler sorgu erişimi için uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-163">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-164">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0a6e1-164">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="0a6e1-165">Işlemsel Öngörüler Hizmetleri için isteklere yetki veren erişim belirteçlerinin Audience öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-165">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-166">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a6e1-166">-Confirm</span></span>
<span data-ttu-id="0a6e1-167">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-167">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a6e1-168">-WhatIf</span></span>
<span data-ttu-id="0a6e1-169">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-169">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a6e1-170">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-170">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a6e1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6e1-171">CommonParameters</span></span>
<span data-ttu-id="0a6e1-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6e1-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a6e1-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6e1-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a6e1-174">INPUTS</span></span>

### <span data-ttu-id="0a6e1-175">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0a6e1-175">None</span></span>
<span data-ttu-id="0a6e1-176">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0a6e1-176">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a6e1-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a6e1-177">OUTPUTS</span></span>

### <span data-ttu-id="0a6e1-178">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0a6e1-178">PSAzureEnvironment</span></span>

## <span data-ttu-id="0a6e1-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a6e1-179">NOTES</span></span>

## <span data-ttu-id="0a6e1-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a6e1-180">RELATED LINKS</span></span>

[<span data-ttu-id="0a6e1-181">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="0a6e1-181">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="0a6e1-182">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="0a6e1-182">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="0a6e1-183">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="0a6e1-183">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

