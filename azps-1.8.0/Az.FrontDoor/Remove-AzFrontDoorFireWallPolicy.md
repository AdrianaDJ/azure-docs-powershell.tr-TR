---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: f081d403a47f457c48320238436d72ca4ebd15fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916703"
---
# <span data-ttu-id="9518a-101">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="9518a-101">Remove-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="9518a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9518a-102">SYNOPSIS</span></span>
<span data-ttu-id="9518a-103">WAF ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="9518a-103">Remove WAF policy</span></span>

## <span data-ttu-id="9518a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9518a-104">SYNTAX</span></span>

### <span data-ttu-id="9518a-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9518a-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9518a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9518a-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9518a-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9518a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9518a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9518a-108">DESCRIPTION</span></span>
<span data-ttu-id="9518a-109">**Remove-AzFrontDoorFireWallPolicy** cmdlet 'i, geçerli aboneliğin altındaki WAF ilkesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="9518a-109">The **Remove-AzFrontDoorFireWallPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="9518a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9518a-110">EXAMPLES</span></span>

### <span data-ttu-id="9518a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9518a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="9518a-112">$ResourceGroupName $policyName adındaki WAF ilkesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9518a-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="9518a-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9518a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorFireWallPolicy
```

<span data-ttu-id="9518a-114">$ResourceGroupName tüm WAF ilkesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9518a-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="9518a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9518a-115">PARAMETERS</span></span>

### <span data-ttu-id="9518a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9518a-116">-DefaultProfile</span></span>
<span data-ttu-id="9518a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9518a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9518a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9518a-118">-InputObject</span></span>
<span data-ttu-id="9518a-119">Silinecek WAF ilke nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9518a-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="9518a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9518a-120">-Name</span></span>
<span data-ttu-id="9518a-121">Silinecek WAF ilkesinin adı.</span><span class="sxs-lookup"><span data-stu-id="9518a-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="9518a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9518a-122">-PassThru</span></span>
<span data-ttu-id="9518a-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="9518a-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="9518a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9518a-124">-ResourceGroupName</span></span>
<span data-ttu-id="9518a-125">WAF ilkesinin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="9518a-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="9518a-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9518a-126">-ResourceId</span></span>
<span data-ttu-id="9518a-127">Silinecek WAF ilkesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9518a-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9518a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9518a-128">-Confirm</span></span>
<span data-ttu-id="9518a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9518a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9518a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9518a-130">-WhatIf</span></span>
<span data-ttu-id="9518a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9518a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9518a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9518a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9518a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9518a-133">CommonParameters</span></span>
<span data-ttu-id="9518a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9518a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9518a-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9518a-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9518a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9518a-136">INPUTS</span></span>

### <span data-ttu-id="9518a-137">Microsoft. Azure. Commands. Frontkapısı. modeller. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9518a-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="9518a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9518a-138">System.String</span></span>

## <span data-ttu-id="9518a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9518a-139">OUTPUTS</span></span>

### <span data-ttu-id="9518a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9518a-140">System.Boolean</span></span>

## <span data-ttu-id="9518a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9518a-141">NOTES</span></span>

## <span data-ttu-id="9518a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9518a-142">RELATED LINKS</span></span>

<span data-ttu-id="9518a-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="9518a-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span></span>