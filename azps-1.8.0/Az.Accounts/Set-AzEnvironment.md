---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751244"
---
# <span data-ttu-id="c08e6-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c08e6-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="c08e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c08e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c08e6-103">Azure ortamının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c08e6-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="c08e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c08e6-104">SYNTAX</span></span>

### <span data-ttu-id="c08e6-105">Ad (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c08e6-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08e6-106">Ermenistan</span><span class="sxs-lookup"><span data-stu-id="c08e6-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c08e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c08e6-107">DESCRIPTION</span></span>
<span data-ttu-id="c08e6-108">Set-AzEnvironment cmdlet, bir Azure örneğine bağlanmak için uç noktaları ve meta verileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c08e6-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="c08e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c08e6-109">EXAMPLES</span></span>

### <span data-ttu-id="c08e6-110">Örnek 1: yeni bir ortam oluşturma ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="c08e6-110">Example 1: Creating and modifying a new environment</span></span>
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
```

<span data-ttu-id="c08e6-111">Bu örnekte, Add-AzEnvironment kullanarak örnek uç noktaları içeren yeni bir Azure ortamı oluşturduk ve cmdlet Set-AzEnvironment kullanarak oluşturulan ortamın ActiveDirectoryEndpoint ve GraphEndpoint özniteliklerinin değerini değiştiriyoruz.</span><span class="sxs-lookup"><span data-stu-id="c08e6-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="c08e6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c08e6-112">PARAMETERS</span></span>

### <span data-ttu-id="c08e6-113">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="c08e6-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="c08e6-114">Azure Active Directory kimlik doğrulaması için temel yetkiyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="c08e6-115">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="c08e6-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="c08e6-116">Azure Resource Manager veya hizmet yönetimi (RDFE) uç noktalarına yönelik isteklerin doğrulanmasında kullanılan belirteçlerin Audience ifadesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="c08e6-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="c08e6-117">-AdTenant</span></span>
<span data-ttu-id="c08e6-118">Varsayılan Active Directory kiracısı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="c08e6-119">-Ermenistan</span><span class="sxs-lookup"><span data-stu-id="c08e6-119">-ARMEndpoint</span></span>
<span data-ttu-id="c08e6-120">Azure Resource Manager uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c08e6-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="c08e6-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c08e6-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="c08e6-122">Azure Analysis Services kaynağının kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c08e6-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="c08e6-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="c08e6-124">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="c08e6-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c08e6-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="c08e6-126">Azure Data Lake Analytics iş ve Katalog hizmetlerinin DNS soneki</span><span class="sxs-lookup"><span data-stu-id="c08e6-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="c08e6-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="c08e6-128">Azure Data Lake Store FileSystem 'ın DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="c08e6-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="c08e6-129">Örnek: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="c08e6-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="c08e6-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="c08e6-131">Azure Anahtar Kasası hizmetinin DNS soneki.</span><span class="sxs-lookup"><span data-stu-id="c08e6-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="c08e6-132">Örnek vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="c08e6-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="c08e6-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c08e6-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="c08e6-134">İstenen belirtecin alıcısı olan Azure Key kasa veri hizmetinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c08e6-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="c08e6-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="c08e6-136">Azure Log Analytics API ile iletişim kurarken kullanılacak uç nokta.</span><span class="sxs-lookup"><span data-stu-id="c08e6-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c08e6-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="c08e6-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="c08e6-138">Azure Log Analytics API ile kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="c08e6-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="c08e6-139">-Batchendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="c08e6-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="c08e6-140">İstenen belirtecin alıcısı olan Azure toplu Iş hizmetinin kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="c08e6-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="c08e6-141">-Datalakeizleyiciyi</span><span class="sxs-lookup"><span data-stu-id="c08e6-141">-DataLakeAudience</span></span>
<span data-ttu-id="c08e6-142">AD veri Lake Services uç noktasında kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="c08e6-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="c08e6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08e6-143">-DefaultProfile</span></span>
<span data-ttu-id="c08e6-144">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c08e6-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c08e6-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="c08e6-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="c08e6-146">Active Directory Federasyon Hizmetleri (ADFS) Şirket içi kimlik doğrulamasına izin verildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="c08e6-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-147">-GalleryEndpoint</span></span>
<span data-ttu-id="c08e6-148">Dağıtım şablonlarının Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="c08e6-149">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="c08e6-149">-GraphAudience</span></span>
<span data-ttu-id="c08e6-150">AD grafik uç noktasıyla kimlik doğrulama belirteçleri için hedef kitle.</span><span class="sxs-lookup"><span data-stu-id="c08e6-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="c08e6-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-151">-GraphEndpoint</span></span>
<span data-ttu-id="c08e6-152">Grafik (Active Directory meta verileri) isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="c08e6-153">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="c08e6-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="c08e6-154">Yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="c08e6-155">-Ad</span><span class="sxs-lookup"><span data-stu-id="c08e6-155">-Name</span></span>
<span data-ttu-id="c08e6-156">Değiştirilecek ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="c08e6-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="c08e6-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="c08e6-158">. Publishsettings dosyalarının indirileceği URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="c08e6-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="c08e6-160">Azure Resource Manager isteklerinin URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="c08e6-161">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c08e6-161">-Scope</span></span>
<span data-ttu-id="c08e6-162">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="c08e6-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c08e6-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-163">-ServiceEndpoint</span></span>
<span data-ttu-id="c08e6-164">Hizmet yönetimi (RDFE) isteklerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="c08e6-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="c08e6-166">Azure SQL veritabanı sunucuları için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="c08e6-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="c08e6-167">-StorageEndpoint</span></span>
<span data-ttu-id="c08e6-168">Depolama uç noktasını belirtir (blob, tablo, kuyruk ve dosya) erişimi.</span><span class="sxs-lookup"><span data-stu-id="c08e6-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="c08e6-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="c08e6-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="c08e6-170">Azure Traffic Manager hizmetleri için etki alanı adı sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="c08e6-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="c08e6-171">-Confirm</span></span>
<span data-ttu-id="c08e6-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c08e6-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08e6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08e6-173">-WhatIf</span></span>
<span data-ttu-id="c08e6-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c08e6-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c08e6-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c08e6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08e6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08e6-176">CommonParameters</span></span>
<span data-ttu-id="c08e6-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c08e6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08e6-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08e6-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08e6-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c08e6-179">INPUTS</span></span>

### <span data-ttu-id="c08e6-180">System. String</span><span class="sxs-lookup"><span data-stu-id="c08e6-180">System.String</span></span>

### <span data-ttu-id="c08e6-181">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c08e6-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c08e6-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c08e6-182">OUTPUTS</span></span>

### <span data-ttu-id="c08e6-183">Microsoft. Azure. Commands. Profile. modeller. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c08e6-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="c08e6-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c08e6-184">NOTES</span></span>

## <span data-ttu-id="c08e6-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c08e6-185">RELATED LINKS</span></span>

[<span data-ttu-id="c08e6-186">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c08e6-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="c08e6-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c08e6-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="c08e6-188">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="c08e6-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

