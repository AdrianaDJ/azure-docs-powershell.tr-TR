---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571518"
---
# <span data-ttu-id="8c7c5-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c7c5-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="8c7c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7c5-103">Azure ortamının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="8c7c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c7c5-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c7c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7c5-106">Set-AzureRMEnvironment cmdlet, bir Azure örneğine bağlanmak için uç noktaları ve meta verileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="8c7c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7c5-108">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="8c7c5-108">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="8c7c5-109">Bu örnekte, Add-AzureRmEnvironment ' ı kullanarak örnek uç noktaları olan yeni bir Azure ortamı oluşturduk ve ardından set-AzureRmEnvironment cmdlet 'ini kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="8c7c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c7c5-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7c5-111">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="8c7c5-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="8c7c5-112">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-113">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="8c7c5-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="8c7c5-114">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-115">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="8c7c5-115">-AdTenant</span></span>
<span data-ttu-id="8c7c5-116">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-116">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8c7c5-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="8c7c5-118">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="8c7c5-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="8c7c5-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="8c7c5-120">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="8c7c5-121">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="8c7c5-121">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8c7c5-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="8c7c5-123">Anahtar Kasası Hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-123">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="8c7c5-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="8c7c5-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="8c7c5-125">Anahtar Kasası Hizmetleri isteklerine yetki veren erişim belirteçlerinin kitlesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

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

### <span data-ttu-id="8c7c5-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="8c7c5-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="8c7c5-127">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c7c5-128">-GalleryEndpoint</span></span>
<span data-ttu-id="8c7c5-129">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-130">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="8c7c5-130">-GraphAudience</span></span>
<span data-ttu-id="8c7c5-131">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c7c5-132">-GraphEndpoint</span></span>
<span data-ttu-id="8c7c5-133">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-134">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="8c7c5-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="8c7c5-135">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-135">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c7c5-136">-Name</span></span>
<span data-ttu-id="8c7c5-137">Değiştirilecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-137">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="8c7c5-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="8c7c5-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="8c7c5-139">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c7c5-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="8c7c5-141">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-141">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c7c5-142">-ServiceEndpoint</span></span>
<span data-ttu-id="8c7c5-143">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8c7c5-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="8c7c5-145">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="8c7c5-146">-StorageEndpoint</span></span>
<span data-ttu-id="8c7c5-147">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="8c7c5-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="8c7c5-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="8c7c5-149">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c7c5-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c7c5-150">-Confirm</span></span>
<span data-ttu-id="8c7c5-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c7c5-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7c5-152">-WhatIf</span></span>
<span data-ttu-id="8c7c5-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c7c5-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c7c5-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7c5-155">CommonParameters</span></span>
<span data-ttu-id="8c7c5-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c7c5-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7c5-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7c5-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7c5-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c7c5-158">INPUTS</span></span>

## <span data-ttu-id="8c7c5-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c7c5-159">OUTPUTS</span></span>

### <span data-ttu-id="8c7c5-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c7c5-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="8c7c5-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c7c5-161">NOTES</span></span>

## <span data-ttu-id="8c7c5-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c7c5-162">RELATED LINKS</span></span>

[<span data-ttu-id="8c7c5-163">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c7c5-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="8c7c5-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c7c5-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="8c7c5-165">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="8c7c5-165">Remove-AzureRMEnvironment</span></span>]()

