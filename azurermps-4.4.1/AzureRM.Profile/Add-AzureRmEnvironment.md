---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764538"
---
# <span data-ttu-id="7f2be-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f2be-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="7f2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2be-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2be-103">Bir Azure Resource Manager örneğine uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="7f2be-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f2be-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f2be-104">SYNTAX</span></span>

### <span data-ttu-id="7f2be-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f2be-105">Name (Default)</span></span>
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
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f2be-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="7f2be-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f2be-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f2be-107">DESCRIPTION</span></span>
<span data-ttu-id="7f2be-108">Add-AzureRmEnvironment cmdlet 'i Azure Resource Manager cmdlet 'lerinin yeni bir Azure Kaynak Yöneticisi örneğine bağlanmasını sağlamak için uç noktalar ve meta veriler ekler.</span><span class="sxs-lookup"><span data-stu-id="7f2be-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="7f2be-109">Yerleşik ortamlar Azurecsesli ve AzureChinaCloud hedefi Azure Resource Manager 'ın var olan genel örneklerini hedefleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f2be-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="7f2be-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f2be-110">EXAMPLES</span></span>

### <span data-ttu-id="7f2be-111">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="7f2be-111">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="7f2be-112">Bu örnekte, Add-AzureRmEnvironment ' ı kullanarak örnek uç noktaları olan yeni bir Azure ortamı oluşturduk ve ardından set-AzureRmEnvironment cmdlet 'ini kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="7f2be-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="7f2be-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f2be-113">PARAMETERS</span></span>

### <span data-ttu-id="7f2be-114">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="7f2be-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="7f2be-115">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="7f2be-116">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="7f2be-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="7f2be-117">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="7f2be-118">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="7f2be-118">-AdTenant</span></span>
<span data-ttu-id="7f2be-119">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-119">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="7f2be-120">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="7f2be-120">-ARMEndpoint</span></span>
<span data-ttu-id="7f2be-121">Azure Resource Manager uç noktası</span><span class="sxs-lookup"><span data-stu-id="7f2be-121">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="7f2be-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7f2be-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="7f2be-123">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="7f2be-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="7f2be-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7f2be-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="7f2be-125">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="7f2be-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="7f2be-126">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="7f2be-126">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="7f2be-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7f2be-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="7f2be-128">Anahtar Kasası Hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-128">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="7f2be-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7f2be-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="7f2be-130">Anahtar Kasası Hizmetleri isteklerine yetki veren erişim belirteçlerinin kitlesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f2be-131">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="7f2be-131">-DataLakeAudience</span></span>
<span data-ttu-id="7f2be-132">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="7f2be-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="7f2be-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2be-133">-DefaultProfile</span></span>
<span data-ttu-id="7f2be-134">Azure ile iletişimde kullanılan credeetnaıls, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f2be-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f2be-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="7f2be-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="7f2be-136">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="7f2be-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f2be-137">-GalleryEndpoint</span></span>
<span data-ttu-id="7f2be-138">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="7f2be-139">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="7f2be-139">-GraphAudience</span></span>
<span data-ttu-id="7f2be-140">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="7f2be-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="7f2be-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f2be-141">-GraphEndpoint</span></span>
<span data-ttu-id="7f2be-142">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="7f2be-143">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="7f2be-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="7f2be-144">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-144">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="7f2be-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f2be-145">-Name</span></span>
<span data-ttu-id="7f2be-146">Eklenecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-146">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="7f2be-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="7f2be-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="7f2be-148">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="7f2be-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f2be-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="7f2be-150">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-150">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="7f2be-151">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="7f2be-151">-Scope</span></span>
<span data-ttu-id="7f2be-152">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="7f2be-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7f2be-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f2be-153">-ServiceEndpoint</span></span>
<span data-ttu-id="7f2be-154">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="7f2be-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7f2be-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="7f2be-156">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="7f2be-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f2be-157">-StorageEndpoint</span></span>
<span data-ttu-id="7f2be-158">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="7f2be-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="7f2be-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7f2be-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="7f2be-160">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="7f2be-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f2be-161">-Confirm</span></span>
<span data-ttu-id="7f2be-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f2be-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f2be-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f2be-163">-WhatIf</span></span>
<span data-ttu-id="7f2be-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f2be-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f2be-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f2be-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f2be-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2be-166">CommonParameters</span></span>
<span data-ttu-id="7f2be-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f2be-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2be-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f2be-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2be-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f2be-169">INPUTS</span></span>

## <span data-ttu-id="7f2be-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f2be-170">OUTPUTS</span></span>

### <span data-ttu-id="7f2be-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f2be-171">PSAzureEnvironment</span></span>
<span data-ttu-id="7f2be-172">Bu cmdlet, Azure örneği ile iletişim kurmak için gereken uç noktaları ve meta veri kümesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f2be-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="7f2be-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f2be-173">NOTES</span></span>

## <span data-ttu-id="7f2be-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f2be-174">RELATED LINKS</span></span>

[<span data-ttu-id="7f2be-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f2be-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="7f2be-176">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f2be-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="7f2be-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f2be-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)
