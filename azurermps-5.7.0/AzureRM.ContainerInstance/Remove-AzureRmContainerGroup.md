---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: 80343713c9bf7a0e34a1d9a3b3b75825cbb97a12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594107"
---
# <span data-ttu-id="59f4c-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="59f4c-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="59f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="59f4c-103">Kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59f4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59f4c-104">SYNTAX</span></span>

### <span data-ttu-id="59f4c-105">RemoveContainerGroupByResourceGroupAndNameParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59f4c-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f4c-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="59f4c-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59f4c-107">Removecontainergroupbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="59f4c-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f4c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59f4c-108">DESCRIPTION</span></span>
<span data-ttu-id="59f4c-109">**Remove-AzureRmContainerGroup** cmdlet 'i bir kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="59f4c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59f4c-110">EXAMPLES</span></span>

### <span data-ttu-id="59f4c-111">Örnek 1: kapsayıcı grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="59f4c-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="59f4c-112">Bu komut belirtilen kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="59f4c-113">Örnek 2: bir kapsayıcı grubunu boru by ile kaldırır</span><span class="sxs-lookup"><span data-stu-id="59f4c-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="59f4c-114">Bu komut, bir kapsayıcı grubunu boruları kullanarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="59f4c-115">Örnek 3: bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="59f4c-116">Bu komut, bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59f4c-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="59f4c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59f4c-117">PARAMETERS</span></span>

### <span data-ttu-id="59f4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f4c-118">-DefaultProfile</span></span>
<span data-ttu-id="59f4c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59f4c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f4c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59f4c-120">-InputObject</span></span>
<span data-ttu-id="59f4c-121">Kaldırılacak kapsayıcı grubu.</span><span class="sxs-lookup"><span data-stu-id="59f4c-121">The container group to remove.</span></span>

```yaml
Type: PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59f4c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="59f4c-122">-Name</span></span>
<span data-ttu-id="59f4c-123">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="59f4c-123">The container group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f4c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59f4c-124">-PassThru</span></span>
<span data-ttu-id="59f4c-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="59f4c-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="59f4c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f4c-126">-ResourceGroupName</span></span>
<span data-ttu-id="59f4c-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="59f4c-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59f4c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="59f4c-128">-ResourceId</span></span>
<span data-ttu-id="59f4c-129">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="59f4c-129">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f4c-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="59f4c-130">-Confirm</span></span>
<span data-ttu-id="59f4c-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59f4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f4c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f4c-132">-WhatIf</span></span>
<span data-ttu-id="59f4c-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59f4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f4c-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59f4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f4c-135">CommonParameters</span></span>
<span data-ttu-id="59f4c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59f4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f4c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59f4c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59f4c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59f4c-138">INPUTS</span></span>

### <span data-ttu-id="59f4c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59f4c-139">System.String</span></span>
<span data-ttu-id="59f4c-140">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="59f4c-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="59f4c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59f4c-141">OUTPUTS</span></span>

### <span data-ttu-id="59f4c-142">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="59f4c-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="59f4c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59f4c-143">NOTES</span></span>

## <span data-ttu-id="59f4c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59f4c-144">RELATED LINKS</span></span>
