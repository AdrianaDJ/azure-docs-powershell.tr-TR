---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593573"
---
# <span data-ttu-id="d4a2f-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="d4a2f-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="d4a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a2f-103">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4a2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4a2f-104">SYNTAX</span></span>

### <span data-ttu-id="d4a2f-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4a2f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="d4a2f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d4a2f-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="d4a2f-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="d4a2f-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d4a2f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4a2f-108">DESCRIPTION</span></span>
<span data-ttu-id="d4a2f-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet 'i Integration Runtime 'de bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="d4a2f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4a2f-110">EXAMPLES</span></span>

### <span data-ttu-id="d4a2f-111">Örnek 1: Tümleştirme çalışma zamanından düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="d4a2f-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="d4a2f-112">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubu ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' Node_1 ' adlı bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="d4a2f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4a2f-113">PARAMETERS</span></span>

### <span data-ttu-id="d4a2f-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4a2f-114">-Confirm</span></span>
<span data-ttu-id="d4a2f-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a2f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d4a2f-116">-DataFactoryName</span></span>
<span data-ttu-id="d4a2f-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-117">The data factory name.</span></span>

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

### <span data-ttu-id="d4a2f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d4a2f-118">-Force</span></span>
<span data-ttu-id="d4a2f-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d4a2f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a2f-120">-InputObject</span></span>
<span data-ttu-id="d4a2f-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="d4a2f-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="d4a2f-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d4a2f-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a2f-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="d4a2f-124">-NodeName</span></span>
<span data-ttu-id="d4a2f-125">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4a2f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a2f-126">-ResourceGroupName</span></span>
<span data-ttu-id="d4a2f-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-127">The resource group name.</span></span>

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

### <span data-ttu-id="d4a2f-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4a2f-128">-ResourceId</span></span>
<span data-ttu-id="d4a2f-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d4a2f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a2f-130">-WhatIf</span></span>
<span data-ttu-id="d4a2f-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="d4a2f-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="d4a2f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4a2f-132">INPUTS</span></span>

### <span data-ttu-id="d4a2f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a2f-133">System.String</span></span>
<span data-ttu-id="d4a2f-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="d4a2f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="d4a2f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4a2f-135">OUTPUTS</span></span>

### <span data-ttu-id="d4a2f-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="d4a2f-136">System.Object</span></span>

## <span data-ttu-id="d4a2f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4a2f-137">NOTES</span></span>

## <span data-ttu-id="d4a2f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4a2f-138">RELATED LINKS</span></span>

