---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098046"
---
# <span data-ttu-id="9e47c-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9e47c-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="9e47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e47c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e47c-103">Self-hosted Integration Runtime düğümünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9e47c-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="9e47c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e47c-104">SYNTAX</span></span>

### <span data-ttu-id="9e47c-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e47c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e47c-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9e47c-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e47c-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="9e47c-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e47c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e47c-108">DESCRIPTION</span></span>
<span data-ttu-id="9e47c-109">**Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet 'i, Veri Fabrikası içinde self-hosted Integration Runtime düğümünün özelliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="9e47c-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="9e47c-110">Şu anda yalnızca ' Concurrentjobslimıt ' güncelleştirmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="9e47c-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="9e47c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e47c-111">EXAMPLES</span></span>

### <span data-ttu-id="9e47c-112">Örnek 1: self-hosted Integration Runtime düğümünü güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="9e47c-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="9e47c-113">Cmdlet, Self ile barındırılan tümleştirme çalışma zamanı ' test-Selfhost-IR ' ' Node_1</span><span class="sxs-lookup"><span data-stu-id="9e47c-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="9e47c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e47c-114">PARAMETERS</span></span>

### <span data-ttu-id="9e47c-115">-Concurrentjobslimıt</span><span class="sxs-lookup"><span data-stu-id="9e47c-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="9e47c-116">Tümleştirme çalışma zamanı düğümünde çalışmasına izin verilen eşzamanlı iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="9e47c-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="9e47c-117">1 ila maxConcurrentJobs değerlerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="9e47c-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="9e47c-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9e47c-118">-DataFactoryName</span></span>
<span data-ttu-id="9e47c-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="9e47c-119">The data factory name.</span></span>

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

### <span data-ttu-id="9e47c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e47c-120">-DefaultProfile</span></span>
<span data-ttu-id="9e47c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e47c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e47c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e47c-122">-InputObject</span></span>
<span data-ttu-id="9e47c-123">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e47c-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="9e47c-124">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="9e47c-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="9e47c-125">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="9e47c-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="9e47c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e47c-126">-Name</span></span>
<span data-ttu-id="9e47c-127">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="9e47c-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="9e47c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e47c-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e47c-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9e47c-129">The resource group name.</span></span>

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

### <span data-ttu-id="9e47c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9e47c-130">-ResourceId</span></span>
<span data-ttu-id="9e47c-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="9e47c-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="9e47c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e47c-132">-Confirm</span></span>
<span data-ttu-id="9e47c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e47c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e47c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e47c-134">-WhatIf</span></span>
<span data-ttu-id="9e47c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e47c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e47c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e47c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e47c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e47c-137">CommonParameters</span></span>
<span data-ttu-id="9e47c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e47c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e47c-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e47c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e47c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e47c-140">INPUTS</span></span>

### <span data-ttu-id="9e47c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9e47c-141">System.String</span></span>

### <span data-ttu-id="9e47c-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="9e47c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9e47c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e47c-143">OUTPUTS</span></span>

### <span data-ttu-id="9e47c-144">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="9e47c-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="9e47c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e47c-145">NOTES</span></span>
<span data-ttu-id="9e47c-146">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="9e47c-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="9e47c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e47c-147">RELATED LINKS</span></span>

<span data-ttu-id="9e47c-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="9e47c-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>
