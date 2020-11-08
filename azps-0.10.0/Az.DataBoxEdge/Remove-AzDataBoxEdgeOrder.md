---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeOrder.md
ms.openlocfilehash: 7ac5bce520e566208ddac18374ef01f2cff843ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936746"
---
# <span data-ttu-id="a80f3-101">Remove-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a80f3-101">Remove-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a80f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a80f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a80f3-103">Aygıtın sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a80f3-103">Removes the order for a device.</span></span>

## <span data-ttu-id="a80f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a80f3-104">SYNTAX</span></span>

### <span data-ttu-id="a80f3-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a80f3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a80f3-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a80f3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a80f3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a80f3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeOrder -InputObject <PSDataBoxEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a80f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a80f3-108">DESCRIPTION</span></span>
<span data-ttu-id="a80f3-109">**Remove-AzDataBoxEdgeOrder** cmdlet 'i, bir veri kutusu uç aygıtının varolan sırasını siler.</span><span class="sxs-lookup"><span data-stu-id="a80f3-109">The **Remove-AzDataBoxEdgeOrder** cmdlet deletes an existing order for a Data Box Edge device.</span></span>

## <span data-ttu-id="a80f3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a80f3-110">EXAMPLES</span></span>

### <span data-ttu-id="a80f3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a80f3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="a80f3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a80f3-112">PARAMETERS</span></span>

### <span data-ttu-id="a80f3-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a80f3-113">-AsJob</span></span>
<span data-ttu-id="a80f3-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a80f3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a80f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a80f3-115">-DefaultProfile</span></span>
<span data-ttu-id="a80f3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a80f3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a80f3-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="a80f3-117">-DeviceName</span></span>
<span data-ttu-id="a80f3-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="a80f3-118">Device Name</span></span>

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

### <span data-ttu-id="a80f3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a80f3-119">-InputObject</span></span>
<span data-ttu-id="a80f3-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="a80f3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a80f3-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a80f3-121">-PassThru</span></span>
<span data-ttu-id="a80f3-122">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="a80f3-122">returns true if successful</span></span>

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

### <span data-ttu-id="a80f3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a80f3-123">-ResourceGroupName</span></span>
<span data-ttu-id="a80f3-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a80f3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a80f3-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a80f3-125">-ResourceId</span></span>
<span data-ttu-id="a80f3-126">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a80f3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="a80f3-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a80f3-127">-Confirm</span></span>
<span data-ttu-id="a80f3-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a80f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a80f3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a80f3-129">-WhatIf</span></span>
<span data-ttu-id="a80f3-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a80f3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a80f3-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a80f3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a80f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a80f3-132">CommonParameters</span></span>
<span data-ttu-id="a80f3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a80f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a80f3-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a80f3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a80f3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a80f3-135">INPUTS</span></span>

### <span data-ttu-id="a80f3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a80f3-136">System.String</span></span>

### <span data-ttu-id="a80f3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a80f3-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a80f3-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a80f3-138">OUTPUTS</span></span>

### <span data-ttu-id="a80f3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a80f3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a80f3-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a80f3-140">NOTES</span></span>

## <span data-ttu-id="a80f3-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a80f3-141">RELATED LINKS</span></span>