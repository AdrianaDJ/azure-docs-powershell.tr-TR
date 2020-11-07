---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 020a492ddab075d121025623f5c731bdc71c440b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938291"
---
# <span data-ttu-id="be549-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be549-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="be549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be549-102">SYNOPSIS</span></span>
<span data-ttu-id="be549-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be549-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="be549-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be549-104">SYNTAX</span></span>

### <span data-ttu-id="be549-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be549-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] 
 [-PublicIPs <String[]>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="be549-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="be549-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>] [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="be549-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="be549-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be549-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="be549-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be549-109">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="be549-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
 [-ExpressCustomSetup <ArrayList>]
```

### <span data-ttu-id="be549-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="be549-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be549-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="be549-111">DESCRIPTION</span></span>
<span data-ttu-id="be549-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be549-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="be549-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be549-113">EXAMPLES</span></span>

### <span data-ttu-id="be549-114">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="be549-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="be549-115">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="be549-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="be549-116">Örnek 2: Self ile barındırılan tümleştirme çalışma zamanını paylaşın.</span><span class="sxs-lookup"><span data-stu-id="be549-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="be549-117">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için ADF 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="be549-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="be549-118">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="be549-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="be549-119">Veri fabrikasına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izninizin olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="be549-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="be549-120">Örnek 3: ADF 'de Self-Hosted IR 'yi Azure-SSIS IR olarak yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="be549-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    PublicIPs                         : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="be549-121">Azure-SSA cmdlet 'i güncelleştirmesi, veri ara</span><span class="sxs-lookup"><span data-stu-id="be549-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="be549-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be549-122">PARAMETERS</span></span>

### <span data-ttu-id="be549-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="be549-123">-AuthKey</span></span>
<span data-ttu-id="be549-124">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="be549-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="be549-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="be549-126">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="be549-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="be549-127">-CatalogPricingTier</span></span>
<span data-ttu-id="be549-128">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="be549-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="be549-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="be549-130">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="be549-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="be549-131">-DataFactoryName</span></span>
<span data-ttu-id="be549-132">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="be549-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be549-133">-Dataproxyıntegrationruntimename</span><span class="sxs-lookup"><span data-stu-id="be549-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="be549-134">Proxy olarak kullanılan Self-Hosted Integration Runtime adı</span><span class="sxs-lookup"><span data-stu-id="be549-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="be549-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="be549-136">Self-Hosted ile Azure-SSIS tümleştirmesi çalışma zamanı arasında verileri taşırken kullanılacak hazırlama veri deposuna başvuruda bulunan Azure Blob depolama bağlantılı hizmet adı</span><span class="sxs-lookup"><span data-stu-id="be549-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="be549-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="be549-138">Verileri Self-Hosted ile Azure-SSIN arasında taşırken kullanılacak hazırlama verileri deposundaki yol, belirtilmemişse varsayılan bir kapsayıcı kullanılır</span><span class="sxs-lookup"><span data-stu-id="be549-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be549-139">-DefaultProfile</span></span>
<span data-ttu-id="be549-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be549-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be549-141">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="be549-141">-Description</span></span>
<span data-ttu-id="be549-142">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="be549-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="be549-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="be549-143">-Edition</span></span>
<span data-ttu-id="be549-144">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="be549-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-145">-Force</span><span class="sxs-lookup"><span data-stu-id="be549-145">-Force</span></span>
<span data-ttu-id="be549-146">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="be549-146">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be549-147">-InputObject</span></span>
<span data-ttu-id="be549-148">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="be549-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be549-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="be549-149">-LicenseType</span></span>
<span data-ttu-id="be549-150">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="be549-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="be549-151">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="be549-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="be549-152">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="be549-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="be549-153">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="be549-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-154">-Konum</span><span class="sxs-lookup"><span data-stu-id="be549-154">-Location</span></span>
<span data-ttu-id="be549-155">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="be549-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-156">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="be549-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="be549-157">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="be549-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-158">-Ad</span><span class="sxs-lookup"><span data-stu-id="be549-158">-Name</span></span>
<span data-ttu-id="be549-159">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="be549-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be549-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="be549-160">-NodeCount</span></span>
<span data-ttu-id="be549-161">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="be549-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="be549-162">-NodeSize</span></span>
<span data-ttu-id="be549-163">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="be549-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-164">-Publicıp 'Ler</span><span class="sxs-lookup"><span data-stu-id="be549-164">-PublicIPs</span></span>
<span data-ttu-id="be549-165">Tümleştirme çalışma zamanının kullanacağı statik genel IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="be549-165">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be549-166">-ResourceGroupName</span></span>
<span data-ttu-id="be549-167">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="be549-167">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be549-168">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="be549-168">-ResourceId</span></span>
<span data-ttu-id="be549-169">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="be549-169">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be549-170">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="be549-170">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="be549-171">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="be549-171">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-172">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="be549-172">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="be549-173">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="be549-173">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-174">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="be549-174">-Subnet</span></span>
<span data-ttu-id="be549-175">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="be549-175">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-176">-Tür</span><span class="sxs-lookup"><span data-stu-id="be549-176">-Type</span></span>
<span data-ttu-id="be549-177">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="be549-177">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-178">-VNetId</span><span class="sxs-lookup"><span data-stu-id="be549-178">-VNetId</span></span>
<span data-ttu-id="be549-179">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="be549-179">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-180">-Onay</span><span class="sxs-lookup"><span data-stu-id="be549-180">-Confirm</span></span>
<span data-ttu-id="be549-181">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be549-181">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be549-182">-WhatIf</span></span>
<span data-ttu-id="be549-183">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="be549-183">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be549-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be549-184">CommonParameters</span></span>
<span data-ttu-id="be549-185">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be549-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be549-186">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be549-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be549-187">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be549-187">INPUTS</span></span>

### <span data-ttu-id="be549-188">System. String</span><span class="sxs-lookup"><span data-stu-id="be549-188">System.String</span></span>

### <span data-ttu-id="be549-189">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="be549-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="be549-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be549-190">OUTPUTS</span></span>

### <span data-ttu-id="be549-191">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="be549-191">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="be549-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be549-192">NOTES</span></span>

## <span data-ttu-id="be549-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be549-193">RELATED LINKS</span></span>

[<span data-ttu-id="be549-194">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="be549-194">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
