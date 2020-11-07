---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: be9a289e7d3aca0bc0a4cc4e2ae8e23dbe5b1ae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763776"
---
# <span data-ttu-id="f8058-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f8058-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="f8058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8058-102">SYNOPSIS</span></span>
<span data-ttu-id="f8058-103">Kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8058-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8058-104">SYNTAX</span></span>

### <span data-ttu-id="f8058-105">RemoveContainerGroupByResourceGroupAndNameParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8058-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8058-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="f8058-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8058-107">Removecontainergroupbyresourceıdparamset</span><span class="sxs-lookup"><span data-stu-id="f8058-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8058-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8058-108">DESCRIPTION</span></span>
<span data-ttu-id="f8058-109">**Remove-AzureRmContainerGroup** cmdlet 'i bir kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="f8058-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8058-110">EXAMPLES</span></span>

### <span data-ttu-id="f8058-111">Örnek 1: kapsayıcı grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="f8058-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="f8058-112">Bu komut belirtilen kapsayıcı grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="f8058-113">Örnek 2: bir kapsayıcı grubunu boru by ile kaldırır</span><span class="sxs-lookup"><span data-stu-id="f8058-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f8058-114">Bu komut, bir kapsayıcı grubunu boruları kullanarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="f8058-115">Örnek 3: bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="f8058-116">Bu komut, bir kapsayıcı grubunu kaynak kimliğiyle kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f8058-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="f8058-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8058-117">PARAMETERS</span></span>

### <span data-ttu-id="f8058-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8058-118">-Confirm</span></span>
<span data-ttu-id="f8058-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8058-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8058-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8058-120">-InputObject</span></span>
<span data-ttu-id="f8058-121">Kaldırılacak kapsayıcı grubu.</span><span class="sxs-lookup"><span data-stu-id="f8058-121">The container group to remove.</span></span>

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

### <span data-ttu-id="f8058-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8058-122">-Name</span></span>
<span data-ttu-id="f8058-123">Kapsayıcı grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f8058-123">The container group name.</span></span>

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

### <span data-ttu-id="f8058-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f8058-124">-PassThru</span></span>
<span data-ttu-id="f8058-125">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f8058-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f8058-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8058-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8058-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f8058-127">The resource group name.</span></span>

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

### <span data-ttu-id="f8058-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f8058-128">-ResourceId</span></span>
<span data-ttu-id="f8058-129">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f8058-129">The resource id.</span></span>

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

### <span data-ttu-id="f8058-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8058-130">-WhatIf</span></span>
<span data-ttu-id="f8058-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8058-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8058-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8058-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8058-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8058-133">-DefaultProfile</span></span>
<span data-ttu-id="f8058-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8058-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8058-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8058-135">CommonParameters</span></span>
<span data-ttu-id="f8058-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8058-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8058-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8058-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8058-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8058-138">INPUTS</span></span>

### <span data-ttu-id="f8058-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f8058-139">System.String</span></span>
<span data-ttu-id="f8058-140">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f8058-140">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f8058-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8058-141">OUTPUTS</span></span>

### <span data-ttu-id="f8058-142">Microsoft. Azure. Commands. Containerınstance. modeller. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="f8058-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="f8058-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8058-143">NOTES</span></span>

## <span data-ttu-id="f8058-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8058-144">RELATED LINKS</span></span>

