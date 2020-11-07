---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761969"
---
# <span data-ttu-id="2d348-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2d348-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="2d348-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d348-102">SYNOPSIS</span></span>
<span data-ttu-id="2d348-103">Ön kapı yük dengeleyiciden kaldır</span><span class="sxs-lookup"><span data-stu-id="2d348-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d348-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d348-104">SYNTAX</span></span>

### <span data-ttu-id="2d348-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d348-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d348-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d348-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d348-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2d348-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d348-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d348-108">DESCRIPTION</span></span>
<span data-ttu-id="2d348-109">**Remove-Azurermfrontkapısı** cmdlet 'i, geçerli aboneliğin altındaki ön kapı yük dengeleyicisinin kaldırılmasına</span><span class="sxs-lookup"><span data-stu-id="2d348-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="2d348-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d348-110">EXAMPLES</span></span>

### <span data-ttu-id="2d348-111">Örnek 1: geçerli aboneliğin altındaki "RG1" kaynak grubundaki "frontdoor1" öğesini kaldır.</span><span class="sxs-lookup"><span data-stu-id="2d348-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="2d348-112">Geçerli aboneliğin altındaki "RG1" kaynak grubundaki "frontdoor1" öğesini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="2d348-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="2d348-113">Örnek 2: geçerli aboneliğin altındaki "RG1" kaynak grubundaki tüm Frontkapılar kaldırılsın.</span><span class="sxs-lookup"><span data-stu-id="2d348-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2d348-114">Geçerli aboneliğin altındaki "RG1" kaynak grubundaki tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d348-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="2d348-115">Örnek 3: geçerli aboneliğin altındaki tüm Frontkapılar kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d348-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2d348-116">Geçerli aboneliğin altındaki tüm Frontkapılar kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d348-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="2d348-117">Örnek 4: geçerli aboneliğin altındaki "frontdoor1" adlı tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d348-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2d348-118">Geçerli aboneliğin altındaki "frontdoor1" adlı tüm Frontkapıları kaldırın.</span><span class="sxs-lookup"><span data-stu-id="2d348-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="2d348-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d348-119">PARAMETERS</span></span>

### <span data-ttu-id="2d348-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d348-120">-DefaultProfile</span></span>
<span data-ttu-id="2d348-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d348-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d348-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d348-122">-InputObject</span></span>
<span data-ttu-id="2d348-123">Silinecek ön kapı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2d348-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="2d348-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d348-124">-Name</span></span>
<span data-ttu-id="2d348-125">Silinecek ön kapı adı.</span><span class="sxs-lookup"><span data-stu-id="2d348-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="2d348-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2d348-126">-PassThru</span></span>
<span data-ttu-id="2d348-127">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="2d348-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="2d348-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d348-128">-ResourceGroupName</span></span>
<span data-ttu-id="2d348-129">Ön kapıya ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="2d348-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="2d348-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2d348-130">-ResourceId</span></span>
<span data-ttu-id="2d348-131">Silinecek ön kapı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2d348-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="2d348-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d348-132">-Confirm</span></span>
<span data-ttu-id="2d348-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d348-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d348-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d348-134">-WhatIf</span></span>
<span data-ttu-id="2d348-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d348-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d348-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d348-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d348-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d348-137">CommonParameters</span></span>
<span data-ttu-id="2d348-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d348-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d348-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d348-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d348-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d348-140">INPUTS</span></span>

### <span data-ttu-id="2d348-141">Microsoft. Azure. Commands. Frontkapısı. modeller. Psfrontkapısı</span><span class="sxs-lookup"><span data-stu-id="2d348-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="2d348-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2d348-142">System.String</span></span>

### <span data-ttu-id="2d348-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d348-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d348-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d348-144">OUTPUTS</span></span>

### <span data-ttu-id="2d348-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d348-145">System.Boolean</span></span>

## <span data-ttu-id="2d348-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d348-146">NOTES</span></span>

## <span data-ttu-id="2d348-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d348-147">RELATED LINKS</span></span>

<span data-ttu-id="2d348-148">[Yeni-Azurermfrontkapısı](./New-AzureRmFrontDoor.md) 
 [Get-Azurermfrontkapısı](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2d348-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
