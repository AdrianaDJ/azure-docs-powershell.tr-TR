---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 73cc7df9dcb32dac592df56f16ad819219e06b7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764070"
---
# <span data-ttu-id="fa740-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fa740-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="fa740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa740-102">SYNOPSIS</span></span>
<span data-ttu-id="fa740-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa740-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa740-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa740-104">SYNTAX</span></span>

### <span data-ttu-id="fa740-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa740-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fa740-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fa740-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="fa740-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fa740-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="fa740-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa740-108">DESCRIPTION</span></span>
<span data-ttu-id="fa740-109">Remove-AzureRmDataFactoryV2 cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="fa740-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="fa740-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa740-110">EXAMPLES</span></span>

### <span data-ttu-id="fa740-111">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="fa740-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="fa740-112">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="fa740-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="fa740-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa740-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fa740-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa740-114">PARAMETERS</span></span>

### <span data-ttu-id="fa740-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa740-115">-Confirm</span></span>
<span data-ttu-id="fa740-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa740-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa740-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa740-117">-InputObject</span></span>
<span data-ttu-id="fa740-118">Kaldırılacak DataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa740-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa740-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fa740-119">-Force</span></span>
<span data-ttu-id="fa740-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="fa740-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fa740-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa740-121">-Name</span></span>
<span data-ttu-id="fa740-122">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa740-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa740-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa740-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa740-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa740-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa740-125">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa740-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa740-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa740-126">-ResourceId</span></span>
<span data-ttu-id="fa740-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fa740-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="fa740-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa740-128">-WhatIf</span></span>
<span data-ttu-id="fa740-129">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="fa740-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="fa740-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa740-130">INPUTS</span></span>

### <span data-ttu-id="fa740-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="fa740-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="fa740-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fa740-132">System.String</span></span>


## <span data-ttu-id="fa740-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa740-133">OUTPUTS</span></span>

### <span data-ttu-id="fa740-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="fa740-134">System.Object</span></span>

## <span data-ttu-id="fa740-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa740-135">NOTES</span></span>
<span data-ttu-id="fa740-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="fa740-136">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa740-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa740-137">RELATED LINKS</span></span>
[<span data-ttu-id="fa740-138">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fa740-138">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="fa740-139">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fa740-139">Set-AzureRmDataFactoryV2</span></span>]()
