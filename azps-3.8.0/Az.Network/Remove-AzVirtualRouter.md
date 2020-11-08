---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6d879357a71e18d9f1b6beb25044bd5d4394a497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103969"
---
# <span data-ttu-id="bd1c5-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bd1c5-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="bd1c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="bd1c5-103">Bir Azure VirtualRouter siler.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="bd1c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd1c5-104">SYNTAX</span></span>

### <span data-ttu-id="bd1c5-105">VirtualRouterNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd1c5-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c5-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd1c5-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd1c5-107">Virtualrouterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bd1c5-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd1c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="bd1c5-109">**Remove-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter 'i siler</span><span class="sxs-lookup"><span data-stu-id="bd1c5-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="bd1c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd1c5-110">EXAMPLES</span></span>

### <span data-ttu-id="bd1c5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bd1c5-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="bd1c5-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="bd1c5-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="bd1c5-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="bd1c5-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="bd1c5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd1c5-114">PARAMETERS</span></span>

### <span data-ttu-id="bd1c5-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="bd1c5-115">-AsJob</span></span>
<span data-ttu-id="bd1c5-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bd1c5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd1c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd1c5-117">-DefaultProfile</span></span>
<span data-ttu-id="bd1c5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd1c5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bd1c5-119">-Force</span></span>
<span data-ttu-id="bd1c5-120">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="bd1c5-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bd1c5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd1c5-121">-InputObject</span></span>
<span data-ttu-id="bd1c5-122">Sanal yönlendirici giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-122">The virtual router input object.</span></span>

```yaml
Type: PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1c5-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="bd1c5-123">-PassThru</span></span>
<span data-ttu-id="bd1c5-124">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="bd1c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd1c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd1c5-126">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-126">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1c5-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bd1c5-127">-ResourceId</span></span>
<span data-ttu-id="bd1c5-128">Sanal yönlendirici kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-128">The virtual router resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1c5-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="bd1c5-129">-RouterName</span></span>
<span data-ttu-id="bd1c5-130">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-130">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd1c5-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd1c5-131">-Confirm</span></span>
<span data-ttu-id="bd1c5-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd1c5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd1c5-133">-WhatIf</span></span>
<span data-ttu-id="bd1c5-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd1c5-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd1c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd1c5-136">CommonParameters</span></span>
<span data-ttu-id="bd1c5-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd1c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd1c5-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd1c5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd1c5-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd1c5-139">INPUTS</span></span>

### <span data-ttu-id="bd1c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bd1c5-140">System.String</span></span>

### <span data-ttu-id="bd1c5-141">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bd1c5-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="bd1c5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd1c5-142">OUTPUTS</span></span>

### <span data-ttu-id="bd1c5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd1c5-143">System.Boolean</span></span>

## <span data-ttu-id="bd1c5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd1c5-144">NOTES</span></span>

## <span data-ttu-id="bd1c5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd1c5-145">RELATED LINKS</span></span>
