---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937583"
---
# <span data-ttu-id="2e529-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2e529-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="2e529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e529-102">SYNOPSIS</span></span>
<span data-ttu-id="2e529-103">Kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-103">Removes a container group.</span></span>

## <span data-ttu-id="2e529-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e529-104">SYNTAX</span></span>

### <span data-ttu-id="2e529-105">RemoveContainerGroupByResourceGroupAndNameParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e529-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e529-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="2e529-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e529-107">Removecontainergroupbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="2e529-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e529-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e529-108">DESCRIPTION</span></span>
<span data-ttu-id="2e529-109">**Remove-AzContainerGroup** cmdlet 'i bir kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="2e529-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e529-110">EXAMPLES</span></span>

### <span data-ttu-id="2e529-111">Örnek 1: kapsayıcı grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="2e529-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="2e529-112">Bu komut belirtilen kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="2e529-113">Örnek 2: bir kapsayıcı grubunu boru by ile kaldırır</span><span class="sxs-lookup"><span data-stu-id="2e529-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="2e529-114">Bu komut, bir kapsayıcı grubunu boruları kullanarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="2e529-115">Örnek 3: bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="2e529-116">Bu komut, bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2e529-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="2e529-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e529-117">PARAMETERS</span></span>

### <span data-ttu-id="2e529-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e529-118">-DefaultProfile</span></span>
<span data-ttu-id="2e529-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e529-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e529-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e529-120">-InputObject</span></span>
<span data-ttu-id="2e529-121">Kaldırılacak kapsayıcı grubu.</span><span class="sxs-lookup"><span data-stu-id="2e529-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e529-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e529-122">-Name</span></span>
<span data-ttu-id="2e529-123">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2e529-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e529-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2e529-124">-PassThru</span></span>
<span data-ttu-id="2e529-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2e529-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2e529-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e529-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e529-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2e529-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e529-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2e529-128">-ResourceId</span></span>
<span data-ttu-id="2e529-129">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2e529-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e529-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e529-130">-Confirm</span></span>
<span data-ttu-id="2e529-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e529-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e529-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e529-132">-WhatIf</span></span>
<span data-ttu-id="2e529-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e529-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e529-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e529-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e529-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e529-135">CommonParameters</span></span>
<span data-ttu-id="2e529-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e529-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e529-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e529-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e529-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e529-138">INPUTS</span></span>

### <span data-ttu-id="2e529-139">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2e529-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="2e529-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2e529-140">System.String</span></span>

## <span data-ttu-id="2e529-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e529-141">OUTPUTS</span></span>

### <span data-ttu-id="2e529-142">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2e529-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2e529-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e529-143">NOTES</span></span>

## <span data-ttu-id="2e529-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e529-144">RELATED LINKS</span></span>
