---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: fbbd2b5047811f09a8142eea2a84e8f77c405be3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916711"
---
# <span data-ttu-id="6b9cb-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6b9cb-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="6b9cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b9cb-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9cb-103">Ön kapı yük dengeleyiciden kaldır</span><span class="sxs-lookup"><span data-stu-id="6b9cb-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="6b9cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6b9cb-104">SYNTAX</span></span>

### <span data-ttu-id="6b9cb-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6b9cb-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9cb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b9cb-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b9cb-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6b9cb-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b9cb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b9cb-108">DESCRIPTION</span></span>
<span data-ttu-id="6b9cb-109">**Remove-Azfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki ön kapı yük dengeleyicisinin kaldırılmasına</span><span class="sxs-lookup"><span data-stu-id="6b9cb-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="6b9cb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6b9cb-110">EXAMPLES</span></span>

### <span data-ttu-id="6b9cb-111">Örnek 1: geçerli aboneliğin altındaki "RG1" kaynak grubundaki "frontdoor1" öğesini kaldır.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="6b9cb-112">Geçerli aboneliğin altındaki "RG1" kaynak grubundaki "frontdoor1" öğesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6b9cb-113">Örnek 2: geçerli aboneliğin altındaki "RG1" kaynak grubundaki tüm Frontkapılar kaldırılsın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="6b9cb-114">Geçerli aboneliğin altındaki "RG1" kaynak grubundaki tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="6b9cb-115">Örnek 3: geçerli aboneliğin altındaki tüm Frontkapılar kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="6b9cb-116">Geçerli aboneliğin altındaki tüm Frontkapılar kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="6b9cb-117">Örnek 4: geçerli aboneliğin altındaki "frontdoor1" adlı tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="6b9cb-118">Geçerli aboneliğin altındaki "frontdoor1" adlı tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="6b9cb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6b9cb-119">PARAMETERS</span></span>

### <span data-ttu-id="6b9cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9cb-120">-DefaultProfile</span></span>
<span data-ttu-id="6b9cb-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b9cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b9cb-122">-InputObject</span></span>
<span data-ttu-id="6b9cb-123">Silinecek ön kapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b9cb-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6b9cb-124">-Name</span></span>
<span data-ttu-id="6b9cb-125">Silinecek ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="6b9cb-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6b9cb-126">-PassThru</span></span>
<span data-ttu-id="6b9cb-127">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="6b9cb-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="6b9cb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9cb-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b9cb-129">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="6b9cb-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6b9cb-130">-ResourceId</span></span>
<span data-ttu-id="6b9cb-131">Silinecek ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6b9cb-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="6b9cb-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6b9cb-132">-Confirm</span></span>
<span data-ttu-id="6b9cb-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9cb-134">-WhatIf</span></span>
<span data-ttu-id="6b9cb-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9cb-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9cb-137">CommonParameters</span></span>
<span data-ttu-id="6b9cb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9cb-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6b9cb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9cb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6b9cb-140">INPUTS</span></span>

### <span data-ttu-id="6b9cb-141">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="6b9cb-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="6b9cb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6b9cb-142">System.String</span></span>

## <span data-ttu-id="6b9cb-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6b9cb-143">OUTPUTS</span></span>

### <span data-ttu-id="6b9cb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b9cb-144">System.Boolean</span></span>

## <span data-ttu-id="6b9cb-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6b9cb-145">NOTES</span></span>

## <span data-ttu-id="6b9cb-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6b9cb-146">RELATED LINKS</span></span>

<span data-ttu-id="6b9cb-147">[Yeni-azön kapı](./New-AzFrontDoor.md) 
 [Get-Azfrontkapısı](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="6b9cb-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>