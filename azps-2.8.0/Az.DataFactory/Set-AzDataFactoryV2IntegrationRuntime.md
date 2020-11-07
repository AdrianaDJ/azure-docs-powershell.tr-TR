---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752444"
---
# <span data-ttu-id="c025b-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c025b-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c025b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c025b-102">SYNOPSIS</span></span>
<span data-ttu-id="c025b-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c025b-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="c025b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c025b-104">SYNTAX</span></span>

### <span data-ttu-id="c025b-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c025b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025b-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c025b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025b-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="c025b-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025b-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="c025b-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025b-109">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="c025b-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c025b-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c025b-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c025b-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c025b-111">DESCRIPTION</span></span>
<span data-ttu-id="c025b-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c025b-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="c025b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c025b-113">EXAMPLES</span></span>

### <span data-ttu-id="c025b-114">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="c025b-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="c025b-115">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c025b-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="c025b-116">Örnek 2: Self ile barındırılan tümleştirme çalışma zamanını paylaşın.</span><span class="sxs-lookup"><span data-stu-id="c025b-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="c025b-117">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için ADF 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="c025b-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="c025b-118">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="c025b-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="c025b-119">Veri fabrikasına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izninizin olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c025b-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="c025b-120">Örnek 3: ADF 'de Self-Hosted IR 'yi Azure-SSIS IR olarak yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="c025b-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="c025b-121">Azure-SSA cmdlet 'i güncelleştirmesi, veri ara</span><span class="sxs-lookup"><span data-stu-id="c025b-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="c025b-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c025b-122">PARAMETERS</span></span>

### <span data-ttu-id="c025b-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="c025b-123">-AuthKey</span></span>
<span data-ttu-id="c025b-124">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="c025b-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c025b-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="c025b-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="c025b-126">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="c025b-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="c025b-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="c025b-127">-CatalogPricingTier</span></span>
<span data-ttu-id="c025b-128">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="c025b-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="c025b-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c025b-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="c025b-130">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="c025b-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="c025b-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c025b-131">-DataFactoryName</span></span>
<span data-ttu-id="c025b-132">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="c025b-132">The data factory name.</span></span>

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

### <span data-ttu-id="c025b-133">-Dataproxyıntegrationruntimename</span><span class="sxs-lookup"><span data-stu-id="c025b-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="c025b-134">Proxy olarak kullanılan Self-Hosted Integration Runtime adı</span><span class="sxs-lookup"><span data-stu-id="c025b-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="c025b-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="c025b-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="c025b-136">Self-Hosted ile Azure-SSIS tümleştirmesi çalışma zamanı arasında verileri taşırken kullanılacak hazırlama veri deposuna başvuruda bulunan Azure Blob depolama bağlantılı hizmet adı</span><span class="sxs-lookup"><span data-stu-id="c025b-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="c025b-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="c025b-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="c025b-138">Verileri Self-Hosted ile Azure-SSIN arasında taşırken kullanılacak hazırlama verileri deposundaki yol, belirtilmemişse varsayılan bir kapsayıcı kullanılır</span><span class="sxs-lookup"><span data-stu-id="c025b-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="c025b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c025b-139">-DefaultProfile</span></span>
<span data-ttu-id="c025b-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c025b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c025b-141">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="c025b-141">-Description</span></span>
<span data-ttu-id="c025b-142">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="c025b-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="c025b-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="c025b-143">-Edition</span></span>
<span data-ttu-id="c025b-144">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="c025b-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="c025b-145">-Force</span><span class="sxs-lookup"><span data-stu-id="c025b-145">-Force</span></span>
<span data-ttu-id="c025b-146">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="c025b-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c025b-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c025b-147">-InputObject</span></span>
<span data-ttu-id="c025b-148">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c025b-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="c025b-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c025b-149">-LicenseType</span></span>
<span data-ttu-id="c025b-150">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="c025b-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="c025b-151">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="c025b-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="c025b-152">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c025b-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="c025b-153">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c025b-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="c025b-154">-Konum</span><span class="sxs-lookup"><span data-stu-id="c025b-154">-Location</span></span>
<span data-ttu-id="c025b-155">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="c025b-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="c025b-156">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="c025b-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="c025b-157">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="c025b-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="c025b-158">-Ad</span><span class="sxs-lookup"><span data-stu-id="c025b-158">-Name</span></span>
<span data-ttu-id="c025b-159">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="c025b-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="c025b-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c025b-160">-NodeCount</span></span>
<span data-ttu-id="c025b-161">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="c025b-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="c025b-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c025b-162">-NodeSize</span></span>
<span data-ttu-id="c025b-163">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="c025b-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="c025b-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c025b-164">-ResourceGroupName</span></span>
<span data-ttu-id="c025b-165">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c025b-165">The resource group name.</span></span>

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

### <span data-ttu-id="c025b-166">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c025b-166">-ResourceId</span></span>
<span data-ttu-id="c025b-167">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c025b-167">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c025b-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="c025b-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="c025b-169">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="c025b-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="c025b-170">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="c025b-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="c025b-171">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c025b-171">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="c025b-172">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c025b-172">-Subnet</span></span>
<span data-ttu-id="c025b-173">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="c025b-173">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="c025b-174">-Tür</span><span class="sxs-lookup"><span data-stu-id="c025b-174">-Type</span></span>
<span data-ttu-id="c025b-175">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="c025b-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="c025b-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="c025b-176">-VNetId</span></span>
<span data-ttu-id="c025b-177">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c025b-177">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="c025b-178">-Onay</span><span class="sxs-lookup"><span data-stu-id="c025b-178">-Confirm</span></span>
<span data-ttu-id="c025b-179">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c025b-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c025b-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c025b-180">-WhatIf</span></span>
<span data-ttu-id="c025b-181">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="c025b-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c025b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c025b-182">CommonParameters</span></span>
<span data-ttu-id="c025b-183">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c025b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c025b-184">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c025b-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c025b-185">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c025b-185">INPUTS</span></span>

### <span data-ttu-id="c025b-186">System. String</span><span class="sxs-lookup"><span data-stu-id="c025b-186">System.String</span></span>

### <span data-ttu-id="c025b-187">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="c025b-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c025b-188">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c025b-188">OUTPUTS</span></span>

### <span data-ttu-id="c025b-189">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="c025b-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c025b-190">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c025b-190">NOTES</span></span>

## <span data-ttu-id="c025b-191">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c025b-191">RELATED LINKS</span></span>

[<span data-ttu-id="c025b-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c025b-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
