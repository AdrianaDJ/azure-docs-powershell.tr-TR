---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917031"
---
# <span data-ttu-id="fd7a5-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fd7a5-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="fd7a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7a5-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="fd7a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd7a5-104">SYNTAX</span></span>

### <span data-ttu-id="fd7a5-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd7a5-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a5-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fd7a5-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a5-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="fd7a5-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a5-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="fd7a5-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a5-109">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="fd7a5-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd7a5-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fd7a5-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd7a5-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd7a5-111">DESCRIPTION</span></span>
<span data-ttu-id="fd7a5-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="fd7a5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd7a5-113">EXAMPLES</span></span>

### <span data-ttu-id="fd7a5-114">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="fd7a5-115">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="fd7a5-116">Örnek 2: Self ile barındırılan tümleştirme çalışma zamanını paylaşın.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="fd7a5-117">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için ADF 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="fd7a5-118">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="fd7a5-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="fd7a5-119">Veri fabrikasına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izninizin olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="fd7a5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd7a5-120">PARAMETERS</span></span>

### <span data-ttu-id="fd7a5-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="fd7a5-121">-AuthKey</span></span>
<span data-ttu-id="fd7a5-122">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="fd7a5-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="fd7a5-124">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="fd7a5-125">-CatalogPricingTier</span></span>
<span data-ttu-id="fd7a5-126">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fd7a5-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="fd7a5-128">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fd7a5-129">-DataFactoryName</span></span>
<span data-ttu-id="fd7a5-130">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-130">The data factory name.</span></span>

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

### <span data-ttu-id="fd7a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7a5-131">-DefaultProfile</span></span>
<span data-ttu-id="fd7a5-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7a5-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="fd7a5-133">-Description</span></span>
<span data-ttu-id="fd7a5-134">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="fd7a5-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="fd7a5-135">-Edition</span></span>
<span data-ttu-id="fd7a5-136">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="fd7a5-137">-Force</span><span class="sxs-lookup"><span data-stu-id="fd7a5-137">-Force</span></span>
<span data-ttu-id="fd7a5-138">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fd7a5-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd7a5-139">-InputObject</span></span>
<span data-ttu-id="fd7a5-140">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="fd7a5-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fd7a5-141">-LicenseType</span></span>
<span data-ttu-id="fd7a5-142">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="fd7a5-143">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="fd7a5-144">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="fd7a5-145">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="fd7a5-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="fd7a5-146">-Location</span></span>
<span data-ttu-id="fd7a5-147">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="fd7a5-148">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="fd7a5-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="fd7a5-149">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd7a5-150">-Name</span></span>
<span data-ttu-id="fd7a5-151">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="fd7a5-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="fd7a5-152">-NodeCount</span></span>
<span data-ttu-id="fd7a5-153">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="fd7a5-154">-NodeSize</span></span>
<span data-ttu-id="fd7a5-155">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="fd7a5-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd7a5-156">-ResourceGroupName</span></span>
<span data-ttu-id="fd7a5-157">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-157">The resource group name.</span></span>

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

### <span data-ttu-id="fd7a5-158">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fd7a5-158">-ResourceId</span></span>
<span data-ttu-id="fd7a5-159">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fd7a5-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="fd7a5-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="fd7a5-161">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="fd7a5-162">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="fd7a5-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="fd7a5-163">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="fd7a5-164">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="fd7a5-164">-Subnet</span></span>
<span data-ttu-id="fd7a5-165">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="fd7a5-166">-Tür</span><span class="sxs-lookup"><span data-stu-id="fd7a5-166">-Type</span></span>
<span data-ttu-id="fd7a5-167">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="fd7a5-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="fd7a5-168">-VNetId</span></span>
<span data-ttu-id="fd7a5-169">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="fd7a5-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd7a5-170">-Confirm</span></span>
<span data-ttu-id="fd7a5-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd7a5-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd7a5-172">-WhatIf</span></span>
<span data-ttu-id="fd7a5-173">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="fd7a5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7a5-174">CommonParameters</span></span>
<span data-ttu-id="fd7a5-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd7a5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7a5-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7a5-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7a5-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd7a5-177">INPUTS</span></span>

### <span data-ttu-id="fd7a5-178">System. String</span><span class="sxs-lookup"><span data-stu-id="fd7a5-178">System.String</span></span>

### <span data-ttu-id="fd7a5-179">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="fd7a5-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fd7a5-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd7a5-180">OUTPUTS</span></span>

### <span data-ttu-id="fd7a5-181">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="fd7a5-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fd7a5-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd7a5-182">NOTES</span></span>

## <span data-ttu-id="fd7a5-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd7a5-183">RELATED LINKS</span></span>

[<span data-ttu-id="fd7a5-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fd7a5-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
