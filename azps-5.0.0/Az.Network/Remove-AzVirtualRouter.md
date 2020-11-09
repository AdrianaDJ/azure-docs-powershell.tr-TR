---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323632"
---
# <span data-ttu-id="819f4-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="819f4-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="819f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="819f4-102">SYNOPSIS</span></span>
<span data-ttu-id="819f4-103">Bir Azure VirtualRouter siler.</span><span class="sxs-lookup"><span data-stu-id="819f4-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="819f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="819f4-104">SYNTAX</span></span>

### <span data-ttu-id="819f4-105">VirtualRouterNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="819f4-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="819f4-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="819f4-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="819f4-107">Virtualrouterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="819f4-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="819f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="819f4-108">DESCRIPTION</span></span>
<span data-ttu-id="819f4-109">**Remove-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter 'i siler</span><span class="sxs-lookup"><span data-stu-id="819f4-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="819f4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="819f4-110">EXAMPLES</span></span>

### <span data-ttu-id="819f4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="819f4-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="819f4-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="819f4-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="819f4-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="819f4-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="819f4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="819f4-114">PARAMETERS</span></span>

### <span data-ttu-id="819f4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="819f4-115">-AsJob</span></span>
<span data-ttu-id="819f4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="819f4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="819f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819f4-117">-DefaultProfile</span></span>
<span data-ttu-id="819f4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="819f4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="819f4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="819f4-119">-Force</span></span>
<span data-ttu-id="819f4-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="819f4-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="819f4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="819f4-121">-InputObject</span></span>
<span data-ttu-id="819f4-122">Sanal yönlendirici giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="819f4-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="819f4-123">-PassThru</span></span>
<span data-ttu-id="819f4-124">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="819f4-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="819f4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819f4-125">-ResourceGroupName</span></span>
<span data-ttu-id="819f4-126">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="819f4-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="819f4-127">-ResourceId</span></span>
<span data-ttu-id="819f4-128">Sanal yönlendirici kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="819f4-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="819f4-129">-RouterName</span></span>
<span data-ttu-id="819f4-130">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="819f4-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="819f4-131">-Confirm</span></span>
<span data-ttu-id="819f4-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="819f4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="819f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819f4-133">-WhatIf</span></span>
<span data-ttu-id="819f4-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="819f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="819f4-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="819f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="819f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f4-136">CommonParameters</span></span>
<span data-ttu-id="819f4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="819f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f4-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="819f4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="819f4-139">INPUTS</span></span>

### <span data-ttu-id="819f4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="819f4-140">System.String</span></span>

### <span data-ttu-id="819f4-141">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="819f4-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="819f4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="819f4-142">OUTPUTS</span></span>

### <span data-ttu-id="819f4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="819f4-143">System.Boolean</span></span>

## <span data-ttu-id="819f4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="819f4-144">NOTES</span></span>

## <span data-ttu-id="819f4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="819f4-145">RELATED LINKS</span></span>
