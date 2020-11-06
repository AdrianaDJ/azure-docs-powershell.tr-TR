---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aae3b830a55b5a2a7683aa1608d15eb4a49a49fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594420"
---
# <span data-ttu-id="ff018-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff018-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ff018-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff018-102">SYNOPSIS</span></span>
<span data-ttu-id="ff018-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff018-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff018-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff018-104">SYNTAX</span></span>

### <span data-ttu-id="ff018-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff018-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff018-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ff018-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff018-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="ff018-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff018-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ff018-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff018-109">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="ff018-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff018-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ff018-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff018-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff018-111">DESCRIPTION</span></span>
<span data-ttu-id="ff018-112">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff018-112">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="ff018-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff018-113">EXAMPLES</span></span>

### <span data-ttu-id="ff018-114">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ff018-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="ff018-115">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff018-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="ff018-116">Örnek 2: Self ile barındırılan tümleştirme çalışma zamanını paylaşın.</span><span class="sxs-lookup"><span data-stu-id="ff018-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="ff018-117">Cmdlet, paylaşılan tümleştirme çalışma zamanını kullanmak için ADF 'yi ekler.</span><span class="sxs-lookup"><span data-stu-id="ff018-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="ff018-118">Parametre kullanılırken `-SharedIntegrationRuntimeResourceId` de eklenmelidir `-Type` .</span><span class="sxs-lookup"><span data-stu-id="ff018-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="ff018-119">Veri fabrikasına cmdlet 'i çalıştırmadan önce tümleştirme çalışma zamanını kullanma izninizin olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ff018-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="ff018-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff018-120">PARAMETERS</span></span>

### <span data-ttu-id="ff018-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="ff018-121">-AuthKey</span></span>
<span data-ttu-id="ff018-122">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="ff018-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ff018-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="ff018-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="ff018-124">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="ff018-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="ff018-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="ff018-125">-CatalogPricingTier</span></span>
<span data-ttu-id="ff018-126">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="ff018-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="ff018-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff018-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="ff018-128">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="ff018-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="ff018-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ff018-129">-DataFactoryName</span></span>
<span data-ttu-id="ff018-130">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="ff018-130">The data factory name.</span></span>

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

### <span data-ttu-id="ff018-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff018-131">-DefaultProfile</span></span>
<span data-ttu-id="ff018-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff018-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff018-133">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ff018-133">-Description</span></span>
<span data-ttu-id="ff018-134">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="ff018-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="ff018-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="ff018-135">-Edition</span></span>
<span data-ttu-id="ff018-136">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="ff018-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="ff018-137">-Force</span><span class="sxs-lookup"><span data-stu-id="ff018-137">-Force</span></span>
<span data-ttu-id="ff018-138">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ff018-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ff018-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff018-139">-InputObject</span></span>
<span data-ttu-id="ff018-140">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ff018-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="ff018-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ff018-141">-LicenseType</span></span>
<span data-ttu-id="ff018-142">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="ff018-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="ff018-143">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="ff018-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="ff018-144">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ff018-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="ff018-145">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ff018-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="ff018-146">-Konum</span><span class="sxs-lookup"><span data-stu-id="ff018-146">-Location</span></span>
<span data-ttu-id="ff018-147">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="ff018-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="ff018-148">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="ff018-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="ff018-149">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="ff018-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="ff018-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff018-150">-Name</span></span>
<span data-ttu-id="ff018-151">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="ff018-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="ff018-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ff018-152">-NodeCount</span></span>
<span data-ttu-id="ff018-153">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="ff018-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="ff018-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="ff018-154">-NodeSize</span></span>
<span data-ttu-id="ff018-155">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="ff018-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="ff018-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff018-156">-ResourceGroupName</span></span>
<span data-ttu-id="ff018-157">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ff018-157">The resource group name.</span></span>

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

### <span data-ttu-id="ff018-158">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ff018-158">-ResourceId</span></span>
<span data-ttu-id="ff018-159">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ff018-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ff018-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="ff018-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="ff018-161">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="ff018-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="ff018-162">-Sharedıntegrationruntimeresourceıd</span><span class="sxs-lookup"><span data-stu-id="ff018-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="ff018-163">Paylaşılan Self-hosted Integration Runtime 'ın kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ff018-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ff018-164">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="ff018-164">-Subnet</span></span>
<span data-ttu-id="ff018-165">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="ff018-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="ff018-166">-Tür</span><span class="sxs-lookup"><span data-stu-id="ff018-166">-Type</span></span>
<span data-ttu-id="ff018-167">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="ff018-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="ff018-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="ff018-168">-VNetId</span></span>
<span data-ttu-id="ff018-169">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ff018-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="ff018-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff018-170">-Confirm</span></span>
<span data-ttu-id="ff018-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff018-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff018-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff018-172">-WhatIf</span></span>
<span data-ttu-id="ff018-173">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="ff018-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ff018-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff018-174">CommonParameters</span></span>
<span data-ttu-id="ff018-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff018-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff018-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff018-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff018-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff018-177">INPUTS</span></span>

### <span data-ttu-id="ff018-178">System. String</span><span class="sxs-lookup"><span data-stu-id="ff018-178">System.String</span></span>

### <span data-ttu-id="ff018-179">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="ff018-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="ff018-180">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff018-180">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ff018-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff018-181">OUTPUTS</span></span>

### <span data-ttu-id="ff018-182">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="ff018-182">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ff018-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff018-183">NOTES</span></span>

## <span data-ttu-id="ff018-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff018-184">RELATED LINKS</span></span>

[<span data-ttu-id="ff018-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff018-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
