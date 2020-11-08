---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267826"
---
# <span data-ttu-id="8c1d6-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8c1d6-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="8c1d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8c1d6-103">Aygıtın ilişkili IoT rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="8c1d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c1d6-104">SYNTAX</span></span>

### <span data-ttu-id="8c1d6-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8c1d6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1d6-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8c1d6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c1d6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c1d6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c1d6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c1d6-108">DESCRIPTION</span></span>
<span data-ttu-id="8c1d6-109">**Remove-AzDataBoxEdgeRole** cmdlet 'i, bir veri kutusu uç aygıtının ilişkili IoT rolünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="8c1d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c1d6-110">EXAMPLES</span></span>

### <span data-ttu-id="8c1d6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8c1d6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="8c1d6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c1d6-112">PARAMETERS</span></span>

### <span data-ttu-id="8c1d6-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8c1d6-113">-AsJob</span></span>
<span data-ttu-id="8c1d6-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8c1d6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c1d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c1d6-115">-DefaultProfile</span></span>
<span data-ttu-id="8c1d6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c1d6-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="8c1d6-117">-DeviceName</span></span>
<span data-ttu-id="8c1d6-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="8c1d6-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1d6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c1d6-119">-InputObject</span></span>
<span data-ttu-id="8c1d6-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="8c1d6-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c1d6-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c1d6-121">-Name</span></span>
<span data-ttu-id="8c1d6-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="8c1d6-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1d6-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8c1d6-123">-PassThru</span></span>
<span data-ttu-id="8c1d6-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="8c1d6-124">returns true if successful</span></span>

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

### <span data-ttu-id="8c1d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c1d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="8c1d6-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8c1d6-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c1d6-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8c1d6-127">-ResourceId</span></span>
<span data-ttu-id="8c1d6-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8c1d6-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8c1d6-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c1d6-129">-Confirm</span></span>
<span data-ttu-id="8c1d6-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c1d6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c1d6-131">-WhatIf</span></span>
<span data-ttu-id="8c1d6-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c1d6-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c1d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c1d6-134">CommonParameters</span></span>
<span data-ttu-id="8c1d6-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c1d6-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c1d6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c1d6-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c1d6-137">INPUTS</span></span>

### <span data-ttu-id="8c1d6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8c1d6-138">System.String</span></span>

### <span data-ttu-id="8c1d6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8c1d6-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8c1d6-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c1d6-140">OUTPUTS</span></span>

### <span data-ttu-id="8c1d6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="8c1d6-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="8c1d6-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c1d6-142">NOTES</span></span>

## <span data-ttu-id="8c1d6-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c1d6-143">RELATED LINKS</span></span>
