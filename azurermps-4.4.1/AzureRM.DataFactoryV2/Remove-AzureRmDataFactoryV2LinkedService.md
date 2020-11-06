---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 24c84657dd33c5ea313f1d6d2c0710b6a3801afd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595194"
---
# <span data-ttu-id="0a21d-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a21d-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0a21d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a21d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a21d-103">Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a21d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a21d-104">SYNTAX</span></span>

### <span data-ttu-id="0a21d-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0a21d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0a21d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a21d-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0a21d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0a21d-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0a21d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a21d-108">DESCRIPTION</span></span>
<span data-ttu-id="0a21d-109">Remove-AzureRmDataFactoryV2LinkedService cmdlet 'i Azure Veri Fabrikası 'ndan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="0a21d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a21d-110">EXAMPLES</span></span>

### <span data-ttu-id="0a21d-111">Örnek 1: bağlantılı hizmeti kaldırma</span><span class="sxs-lookup"><span data-stu-id="0a21d-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="0a21d-112">Bu komut, WikiADF adlı Data Factory 'den LinkedServiceTest adlı bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="0a21d-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0a21d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="0a21d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a21d-114">PARAMETERS</span></span>

### <span data-ttu-id="0a21d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a21d-115">-Confirm</span></span>
<span data-ttu-id="0a21d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a21d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a21d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0a21d-117">-DataFactoryName</span></span>
<span data-ttu-id="0a21d-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a21d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0a21d-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0a21d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0a21d-120">-Force</span></span>
<span data-ttu-id="0a21d-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0a21d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a21d-122">-InputObject</span></span>
<span data-ttu-id="0a21d-123">Kaldırılacak LinkedService nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a21d-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a21d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a21d-124">-Name</span></span>
<span data-ttu-id="0a21d-125">Kaldırılacak bağlı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a21d-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="0a21d-126">Bağlantılı hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="0a21d-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a21d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a21d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a21d-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a21d-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0a21d-129">Bu cmdlet, bu parametrenin belirttiği gruptan bağlantılı hizmeti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a21d-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


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

### <span data-ttu-id="0a21d-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0a21d-130">-ResourceId</span></span>
<span data-ttu-id="0a21d-131">Kaldırılacak bağlı hizmetin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0a21d-131">The Azure resource ID of the linked service to remove.</span></span>

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

### <span data-ttu-id="0a21d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a21d-132">-WhatIf</span></span>
<span data-ttu-id="0a21d-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="0a21d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="0a21d-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a21d-134">INPUTS</span></span>

### <span data-ttu-id="0a21d-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0a21d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="0a21d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0a21d-136">System.String</span></span>


## <span data-ttu-id="0a21d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a21d-137">OUTPUTS</span></span>

### <span data-ttu-id="0a21d-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a21d-138">System.Object</span></span>

## <span data-ttu-id="0a21d-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a21d-139">NOTES</span></span>
<span data-ttu-id="0a21d-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0a21d-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0a21d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a21d-141">RELATED LINKS</span></span>
[<span data-ttu-id="0a21d-142">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a21d-142">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0a21d-143">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0a21d-143">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

