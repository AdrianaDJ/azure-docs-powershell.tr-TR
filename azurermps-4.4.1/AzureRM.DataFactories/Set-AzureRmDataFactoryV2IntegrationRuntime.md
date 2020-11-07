---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764875"
---
# <span data-ttu-id="6ab66-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ab66-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6ab66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab66-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab66-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ab66-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ab66-104">SYNTAX</span></span>

### <span data-ttu-id="6ab66-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ab66-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ab66-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ab66-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ab66-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="6ab66-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ab66-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ab66-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab66-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ab66-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="6ab66-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ab66-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab66-111">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="6ab66-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="6ab66-112">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ab66-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6ab66-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ab66-113">PARAMETERS</span></span>

### <span data-ttu-id="6ab66-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="6ab66-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="6ab66-115">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="6ab66-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="6ab66-116">-CatalogPricingTier</span></span>
<span data-ttu-id="6ab66-117">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="6ab66-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ab66-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="6ab66-119">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="6ab66-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="6ab66-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ab66-120">-Confirm</span></span>
<span data-ttu-id="6ab66-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ab66-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab66-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6ab66-122">-DataFactoryName</span></span>
<span data-ttu-id="6ab66-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6ab66-124">-Description</span></span>
<span data-ttu-id="6ab66-125">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="6ab66-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="6ab66-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6ab66-126">-Force</span></span>
<span data-ttu-id="6ab66-127">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6ab66-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6ab66-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ab66-128">-InputObject</span></span>
<span data-ttu-id="6ab66-129">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6ab66-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="6ab66-130">-Location</span></span>
<span data-ttu-id="6ab66-131">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="6ab66-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="6ab66-132">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="6ab66-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="6ab66-133">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ab66-134">-Name</span></span>
<span data-ttu-id="6ab66-135">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="6ab66-136">-NodeCount</span></span>
<span data-ttu-id="6ab66-137">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="6ab66-138">-NodeSize</span></span>
<span data-ttu-id="6ab66-139">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="6ab66-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="6ab66-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab66-140">-ResourceGroupName</span></span>
<span data-ttu-id="6ab66-141">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-142">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ab66-142">-ResourceId</span></span>
<span data-ttu-id="6ab66-143">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="6ab66-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-144">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="6ab66-144">-Subnet</span></span>
<span data-ttu-id="6ab66-145">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="6ab66-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab66-146">-Tür</span><span class="sxs-lookup"><span data-stu-id="6ab66-146">-Type</span></span>
<span data-ttu-id="6ab66-147">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="6ab66-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="6ab66-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="6ab66-148">-VNetId</span></span>
<span data-ttu-id="6ab66-149">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6ab66-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="6ab66-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab66-150">-WhatIf</span></span>
<span data-ttu-id="6ab66-151">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="6ab66-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6ab66-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab66-152">-DefaultProfile</span></span>
<span data-ttu-id="6ab66-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ab66-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab66-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab66-154">CommonParameters</span></span>
<span data-ttu-id="6ab66-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ab66-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab66-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab66-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab66-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ab66-157">INPUTS</span></span>

### <span data-ttu-id="6ab66-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6ab66-158">System.String</span></span>
<span data-ttu-id="6ab66-159">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="6ab66-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6ab66-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ab66-160">OUTPUTS</span></span>

### <span data-ttu-id="6ab66-161">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="6ab66-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6ab66-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ab66-162">NOTES</span></span>

## <span data-ttu-id="6ab66-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ab66-163">RELATED LINKS</span></span>

[<span data-ttu-id="6ab66-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6ab66-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
