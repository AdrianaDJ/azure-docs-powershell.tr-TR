---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a69e051fb8f2cba30fba8419a818346e044f8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590315"
---
# <span data-ttu-id="0df39-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0df39-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="0df39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df39-102">SYNOPSIS</span></span>
<span data-ttu-id="0df39-103">Self-hosted Integration Runtime düğümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0df39-103">Updates self-hosted integration runtime node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0df39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0df39-104">SYNTAX</span></span>

### <span data-ttu-id="0df39-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0df39-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df39-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0df39-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0df39-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="0df39-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0df39-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0df39-108">DESCRIPTION</span></span>
<span data-ttu-id="0df39-109">**Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet 'i, Veri Fabrikası içinde self-hosted Integration Runtime düğümünün özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="0df39-109">The **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="0df39-110">Şu anda yalnızca ' Concurrentjobslimıt ' güncelleştirmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="0df39-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="0df39-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0df39-111">EXAMPLES</span></span>

### <span data-ttu-id="0df39-112">Örnek 1: self-hosted Integration Runtime düğümünü güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="0df39-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="0df39-113">Cmdlet, Self ile barındırılan tümleştirme çalışma zamanı ' test-Selfhost-IR ' ' Node_1</span><span class="sxs-lookup"><span data-stu-id="0df39-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0df39-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0df39-114">PARAMETERS</span></span>

### <span data-ttu-id="0df39-115">-Concurrentjobslimıt</span><span class="sxs-lookup"><span data-stu-id="0df39-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="0df39-116">Tümleştirme çalışma zamanı düğümünde çalışmasına izin verilen eşzamanlı iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="0df39-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="0df39-117">1 ila maxConcurrentJobs değerlerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="0df39-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df39-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0df39-118">-DataFactoryName</span></span>
<span data-ttu-id="0df39-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="0df39-119">The data factory name.</span></span>

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

### <span data-ttu-id="0df39-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df39-120">-DefaultProfile</span></span>
<span data-ttu-id="0df39-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0df39-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0df39-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0df39-122">-InputObject</span></span>
<span data-ttu-id="0df39-123">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0df39-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="0df39-124">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="0df39-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0df39-125">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="0df39-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0df39-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0df39-126">-Name</span></span>
<span data-ttu-id="0df39-127">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="0df39-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0df39-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df39-128">-ResourceGroupName</span></span>
<span data-ttu-id="0df39-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0df39-129">The resource group name.</span></span>

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

### <span data-ttu-id="0df39-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0df39-130">-ResourceId</span></span>
<span data-ttu-id="0df39-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0df39-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0df39-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0df39-132">-Confirm</span></span>
<span data-ttu-id="0df39-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0df39-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0df39-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0df39-134">-WhatIf</span></span>
<span data-ttu-id="0df39-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0df39-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0df39-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0df39-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0df39-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df39-137">CommonParameters</span></span>
<span data-ttu-id="0df39-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0df39-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df39-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0df39-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df39-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0df39-140">INPUTS</span></span>

### <span data-ttu-id="0df39-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0df39-141">System.String</span></span>

### <span data-ttu-id="0df39-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="0df39-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0df39-143">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0df39-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0df39-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0df39-144">OUTPUTS</span></span>

### <span data-ttu-id="0df39-145">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="0df39-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="0df39-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0df39-146">NOTES</span></span>
<span data-ttu-id="0df39-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="0df39-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0df39-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0df39-148">RELATED LINKS</span></span>

<span data-ttu-id="0df39-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="0df39-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

