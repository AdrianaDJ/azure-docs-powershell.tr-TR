---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572749"
---
# <span data-ttu-id="424e4-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="424e4-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="424e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="424e4-102">SYNOPSIS</span></span>
<span data-ttu-id="424e4-103">WAF ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="424e4-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="424e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="424e4-104">SYNTAX</span></span>

### <span data-ttu-id="424e4-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="424e4-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424e4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="424e4-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="424e4-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="424e4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="424e4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="424e4-108">DESCRIPTION</span></span>
<span data-ttu-id="424e4-109">**Remove-Azurermfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki WAF ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="424e4-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="424e4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="424e4-110">EXAMPLES</span></span>

### <span data-ttu-id="424e4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="424e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="424e4-112">$ResourceGroup $name adındaki WAF ilkesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="424e4-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="424e4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="424e4-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="424e4-114">$ResourceGroup tüm WAF ilkesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="424e4-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="424e4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="424e4-115">PARAMETERS</span></span>

### <span data-ttu-id="424e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="424e4-116">-DefaultProfile</span></span>
<span data-ttu-id="424e4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="424e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="424e4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="424e4-118">-InputObject</span></span>
<span data-ttu-id="424e4-119">Silinecek WAF ilke nesnesi.</span><span class="sxs-lookup"><span data-stu-id="424e4-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="424e4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="424e4-120">-Name</span></span>
<span data-ttu-id="424e4-121">Silinecek WAF ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="424e4-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e4-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="424e4-122">-PassThru</span></span>
<span data-ttu-id="424e4-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="424e4-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="424e4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="424e4-124">-ResourceGroupName</span></span>
<span data-ttu-id="424e4-125">WAF ilkesinin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="424e4-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="424e4-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="424e4-126">-ResourceId</span></span>
<span data-ttu-id="424e4-127">Silinecek WAF ilkesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="424e4-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="424e4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="424e4-128">-Confirm</span></span>
<span data-ttu-id="424e4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="424e4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="424e4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="424e4-130">-WhatIf</span></span>
<span data-ttu-id="424e4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="424e4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="424e4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="424e4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="424e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="424e4-133">CommonParameters</span></span>
<span data-ttu-id="424e4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="424e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="424e4-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="424e4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="424e4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="424e4-136">INPUTS</span></span>

### <span data-ttu-id="424e4-137">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="424e4-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="424e4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="424e4-138">System.String</span></span>

### <span data-ttu-id="424e4-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="424e4-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="424e4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="424e4-140">OUTPUTS</span></span>

### <span data-ttu-id="424e4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="424e4-141">System.Boolean</span></span>

## <span data-ttu-id="424e4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="424e4-142">NOTES</span></span>

## <span data-ttu-id="424e4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="424e4-143">RELATED LINKS</span></span>

<span data-ttu-id="424e4-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="424e4-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
