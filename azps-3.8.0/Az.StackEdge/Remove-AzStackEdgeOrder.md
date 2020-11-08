---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097797"
---
# <span data-ttu-id="8421e-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8421e-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="8421e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8421e-102">SYNOPSIS</span></span>
<span data-ttu-id="8421e-103">Aygıtın sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8421e-103">Removes the order for a device.</span></span>

## <span data-ttu-id="8421e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8421e-104">SYNTAX</span></span>

### <span data-ttu-id="8421e-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8421e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8421e-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8421e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8421e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8421e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8421e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8421e-108">DESCRIPTION</span></span>
<span data-ttu-id="8421e-109">**Remove-AzStackEdgeOrder** cmdlet 'ı, yığın uç aygıtının varolan bir sırasını siler.</span><span class="sxs-lookup"><span data-stu-id="8421e-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="8421e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8421e-110">EXAMPLES</span></span>

### <span data-ttu-id="8421e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8421e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="8421e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8421e-112">PARAMETERS</span></span>

### <span data-ttu-id="8421e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8421e-113">-AsJob</span></span>
<span data-ttu-id="8421e-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8421e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8421e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8421e-115">-DefaultProfile</span></span>
<span data-ttu-id="8421e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8421e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8421e-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="8421e-117">-DeviceName</span></span>
<span data-ttu-id="8421e-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="8421e-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8421e-119">-InputObject</span></span>
<span data-ttu-id="8421e-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="8421e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8421e-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8421e-121">-PassThru</span></span>
<span data-ttu-id="8421e-122">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="8421e-122">returns true if successful</span></span>

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

### <span data-ttu-id="8421e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8421e-123">-ResourceGroupName</span></span>
<span data-ttu-id="8421e-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8421e-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421e-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8421e-125">-ResourceId</span></span>
<span data-ttu-id="8421e-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8421e-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8421e-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8421e-127">-Confirm</span></span>
<span data-ttu-id="8421e-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8421e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8421e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8421e-129">-WhatIf</span></span>
<span data-ttu-id="8421e-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8421e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8421e-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8421e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8421e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8421e-132">CommonParameters</span></span>
<span data-ttu-id="8421e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8421e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8421e-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8421e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8421e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8421e-135">INPUTS</span></span>

### <span data-ttu-id="8421e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8421e-136">System.String</span></span>

### <span data-ttu-id="8421e-137">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8421e-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="8421e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8421e-138">OUTPUTS</span></span>

### <span data-ttu-id="8421e-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="8421e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="8421e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8421e-140">NOTES</span></span>

## <span data-ttu-id="8421e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8421e-141">RELATED LINKS</span></span>
