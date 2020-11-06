---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595188"
---
# <span data-ttu-id="efa02-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="efa02-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="efa02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa02-102">SYNOPSIS</span></span>
<span data-ttu-id="efa02-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa02-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efa02-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efa02-104">SYNTAX</span></span>

### <span data-ttu-id="efa02-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="efa02-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="efa02-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="efa02-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="efa02-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="efa02-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="efa02-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="efa02-108">DESCRIPTION</span></span>
<span data-ttu-id="efa02-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa02-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="efa02-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efa02-110">EXAMPLES</span></span>

### <span data-ttu-id="efa02-111">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="efa02-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="efa02-112">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efa02-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="efa02-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efa02-113">PARAMETERS</span></span>

### <span data-ttu-id="efa02-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="efa02-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="efa02-115">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="efa02-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="efa02-116">-CatalogPricingTier</span></span>
<span data-ttu-id="efa02-117">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="efa02-117">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="efa02-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="efa02-119">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="efa02-119">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="efa02-120">-Confirm</span></span>
<span data-ttu-id="efa02-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="efa02-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="efa02-122">-DataFactoryName</span></span>
<span data-ttu-id="efa02-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="efa02-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="efa02-124">-Description</span></span>
<span data-ttu-id="efa02-125">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="efa02-125">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-126">-Force</span><span class="sxs-lookup"><span data-stu-id="efa02-126">-Force</span></span>
<span data-ttu-id="efa02-127">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="efa02-127">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efa02-128">-InputObject</span></span>
<span data-ttu-id="efa02-129">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="efa02-129">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="efa02-130">-Location</span></span>
<span data-ttu-id="efa02-131">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="efa02-131">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-132">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="efa02-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="efa02-133">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="efa02-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="efa02-134">-Name</span></span>
<span data-ttu-id="efa02-135">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="efa02-135">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="efa02-136">-NodeCount</span></span>
<span data-ttu-id="efa02-137">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="efa02-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="efa02-138">-NodeSize</span></span>
<span data-ttu-id="efa02-139">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="efa02-139">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa02-140">-ResourceGroupName</span></span>
<span data-ttu-id="efa02-141">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="efa02-141">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="efa02-142">-ResourceId</span></span>
<span data-ttu-id="efa02-143">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="efa02-143">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-144">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="efa02-144">-Subnet</span></span>
<span data-ttu-id="efa02-145">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="efa02-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-146">-Tür</span><span class="sxs-lookup"><span data-stu-id="efa02-146">-Type</span></span>
<span data-ttu-id="efa02-147">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="efa02-147">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="efa02-148">-VNetId</span></span>
<span data-ttu-id="efa02-149">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="efa02-149">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa02-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa02-150">-WhatIf</span></span>
<span data-ttu-id="efa02-151">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="efa02-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="efa02-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efa02-152">INPUTS</span></span>

### <span data-ttu-id="efa02-153">System. String</span><span class="sxs-lookup"><span data-stu-id="efa02-153">System.String</span></span>
<span data-ttu-id="efa02-154">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="efa02-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="efa02-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efa02-155">OUTPUTS</span></span>

### <span data-ttu-id="efa02-156">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="efa02-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="efa02-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efa02-157">NOTES</span></span>

## <span data-ttu-id="efa02-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efa02-158">RELATED LINKS</span></span>
[<span data-ttu-id="efa02-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="efa02-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
