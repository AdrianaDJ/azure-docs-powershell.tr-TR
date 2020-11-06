---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595193"
---
# <span data-ttu-id="fe9f0-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe9f0-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="fe9f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9f0-103">Veri Fabrikası 'nden bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe9f0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe9f0-104">SYNTAX</span></span>

### <span data-ttu-id="fe9f0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe9f0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe9f0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe9f0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fe9f0-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fe9f0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fe9f0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe9f0-108">DESCRIPTION</span></span>
<span data-ttu-id="fe9f0-109">Remove-AzureRmDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="fe9f0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe9f0-110">EXAMPLES</span></span>

### <span data-ttu-id="fe9f0-111">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe9f0-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="fe9f0-112">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="fe9f0-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="fe9f0-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="fe9f0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe9f0-114">PARAMETERS</span></span>

### <span data-ttu-id="fe9f0-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe9f0-115">-Confirm</span></span>
<span data-ttu-id="fe9f0-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe9f0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fe9f0-117">-DataFactoryName</span></span>
<span data-ttu-id="fe9f0-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fe9f0-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fe9f0-120">-Force</span></span>
<span data-ttu-id="fe9f0-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fe9f0-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe9f0-122">-Name</span></span>
<span data-ttu-id="fe9f0-123">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe9f0-124">-InputObject</span></span>
<span data-ttu-id="fe9f0-125">Potansiyel satış nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="fe9f0-126">Bu cmdlet, bu parametrenin belirttiği ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9f0-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe9f0-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fe9f0-129">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f0-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fe9f0-130">-ResourceId</span></span>
<span data-ttu-id="fe9f0-131">Kaldırılacak ardışık düzenin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9f0-132">-WhatIf</span></span>
<span data-ttu-id="fe9f0-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="fe9f0-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="fe9f0-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe9f0-134">INPUTS</span></span>

### <span data-ttu-id="fe9f0-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fe9f0-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="fe9f0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fe9f0-136">System.String</span></span>


## <span data-ttu-id="fe9f0-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe9f0-137">OUTPUTS</span></span>

### <span data-ttu-id="fe9f0-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="fe9f0-138">System.Object</span></span>

## <span data-ttu-id="fe9f0-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe9f0-139">NOTES</span></span>
<span data-ttu-id="fe9f0-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="fe9f0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fe9f0-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe9f0-141">RELATED LINKS</span></span>
[<span data-ttu-id="fe9f0-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe9f0-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fe9f0-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe9f0-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="fe9f0-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="fe9f0-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

