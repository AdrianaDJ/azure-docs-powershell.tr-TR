---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107876"
---
# <span data-ttu-id="65664-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65664-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="65664-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65664-102">SYNOPSIS</span></span>
<span data-ttu-id="65664-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65664-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="65664-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65664-104">SYNTAX</span></span>

### <span data-ttu-id="65664-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65664-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65664-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="65664-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65664-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="65664-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65664-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="65664-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65664-109">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="65664-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65664-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="65664-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65664-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="65664-111">DESCRIPTION</span></span>
<span data-ttu-id="65664-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65664-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="65664-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65664-113">EXAMPLES</span></span>

### <span data-ttu-id="65664-114">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="65664-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="65664-115">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="65664-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="65664-116">Örnek 2: Self ile barındırılan tümleştirme çalışma zamanını paylaşın.</span><span class="sxs-lookup"><span data-stu-id="65664-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="65664-117">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için ADF 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="65664-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="65664-118">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="65664-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="65664-119">Veri fabrikasına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izninizin olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="65664-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="65664-120">Örnek 3: ADF 'de Self-Hosted IR 'yi Azure-SSIS IR olarak yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="65664-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="65664-121">Azure-SSA cmdlet 'i güncelleştirmesi, veri ara</span><span class="sxs-lookup"><span data-stu-id="65664-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="65664-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65664-122">PARAMETERS</span></span>

### <span data-ttu-id="65664-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="65664-123">-AuthKey</span></span>
<span data-ttu-id="65664-124">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="65664-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="65664-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="65664-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="65664-126">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="65664-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="65664-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="65664-127">-CatalogPricingTier</span></span>
<span data-ttu-id="65664-128">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="65664-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="65664-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="65664-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="65664-130">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="65664-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="65664-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="65664-131">-DataFactoryName</span></span>
<span data-ttu-id="65664-132">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="65664-132">The data factory name.</span></span>

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

### <span data-ttu-id="65664-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="65664-133">-DataFlowComputeType</span></span>
<span data-ttu-id="65664-134">Veri akışı işini yürütecek veri akışı kümesinin işlem türü.</span><span class="sxs-lookup"><span data-stu-id="65664-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="65664-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="65664-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="65664-136">Veri akışı işini yürütecek veri akışı kümesinin çekirdek sayısı.</span><span class="sxs-lookup"><span data-stu-id="65664-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="65664-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="65664-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="65664-138">Veri akışı işi yürütecek veri akışı kümesinin (dakika olarak) yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="65664-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="65664-139">-Dataproxyıntegrationruntimename</span><span class="sxs-lookup"><span data-stu-id="65664-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="65664-140">Proxy olarak kullanılan Self-Hosted Integration Runtime adı</span><span class="sxs-lookup"><span data-stu-id="65664-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="65664-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="65664-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="65664-142">Self-Hosted ile Azure-SSIS tümleştirmesi çalışma zamanı arasında verileri taşırken kullanılacak hazırlama veri deposuna başvuruda bulunan Azure Blob depolama bağlantılı hizmet adı</span><span class="sxs-lookup"><span data-stu-id="65664-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="65664-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="65664-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="65664-144">Verileri Self-Hosted ile Azure-SSIN arasında taşırken kullanılacak hazırlama verileri deposundaki yol, belirtilmemişse varsayılan bir kapsayıcı kullanılır</span><span class="sxs-lookup"><span data-stu-id="65664-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="65664-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65664-145">-DefaultProfile</span></span>
<span data-ttu-id="65664-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65664-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65664-147">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="65664-147">-Description</span></span>
<span data-ttu-id="65664-148">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="65664-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="65664-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="65664-149">-Edition</span></span>
<span data-ttu-id="65664-150">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="65664-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="65664-151">-Force</span><span class="sxs-lookup"><span data-stu-id="65664-151">-Force</span></span>
<span data-ttu-id="65664-152">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="65664-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="65664-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65664-153">-InputObject</span></span>
<span data-ttu-id="65664-154">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="65664-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="65664-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="65664-155">-LicenseType</span></span>
<span data-ttu-id="65664-156">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="65664-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="65664-157">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="65664-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="65664-158">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="65664-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="65664-159">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65664-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="65664-160">-Konum</span><span class="sxs-lookup"><span data-stu-id="65664-160">-Location</span></span>
<span data-ttu-id="65664-161">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="65664-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="65664-162">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="65664-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="65664-163">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="65664-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="65664-164">-Ad</span><span class="sxs-lookup"><span data-stu-id="65664-164">-Name</span></span>
<span data-ttu-id="65664-165">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="65664-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="65664-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="65664-166">-NodeCount</span></span>
<span data-ttu-id="65664-167">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="65664-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="65664-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="65664-168">-NodeSize</span></span>
<span data-ttu-id="65664-169">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="65664-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="65664-170">-Publicıp 'Ler</span><span class="sxs-lookup"><span data-stu-id="65664-170">-PublicIPs</span></span>
<span data-ttu-id="65664-171">Tümleştirme çalışma zamanının kullanacağı statik genel IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="65664-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="65664-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65664-172">-ResourceGroupName</span></span>
<span data-ttu-id="65664-173">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="65664-173">The resource group name.</span></span>

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

### <span data-ttu-id="65664-174">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65664-174">-ResourceId</span></span>
<span data-ttu-id="65664-175">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="65664-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="65664-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="65664-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="65664-177">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="65664-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="65664-178">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="65664-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="65664-179">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="65664-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="65664-180">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="65664-180">-Subnet</span></span>
<span data-ttu-id="65664-181">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="65664-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="65664-182">-Tür</span><span class="sxs-lookup"><span data-stu-id="65664-182">-Type</span></span>
<span data-ttu-id="65664-183">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="65664-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="65664-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="65664-184">-VNetId</span></span>
<span data-ttu-id="65664-185">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="65664-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="65664-186">-Onay</span><span class="sxs-lookup"><span data-stu-id="65664-186">-Confirm</span></span>
<span data-ttu-id="65664-187">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65664-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65664-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65664-188">-WhatIf</span></span>
<span data-ttu-id="65664-189">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="65664-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="65664-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65664-190">CommonParameters</span></span>
<span data-ttu-id="65664-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65664-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65664-192">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65664-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65664-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65664-193">INPUTS</span></span>

### <span data-ttu-id="65664-194">System. String</span><span class="sxs-lookup"><span data-stu-id="65664-194">System.String</span></span>

### <span data-ttu-id="65664-195">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="65664-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="65664-196">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65664-196">OUTPUTS</span></span>

### <span data-ttu-id="65664-197">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="65664-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="65664-198">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65664-198">NOTES</span></span>

## <span data-ttu-id="65664-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65664-199">RELATED LINKS</span></span>

[<span data-ttu-id="65664-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65664-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
