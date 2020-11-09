---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: a31759c1ec1d1f3e0e3715c9faa3c0171a6e8537
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321154"
---
# <span data-ttu-id="8f0cc-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0cc-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="8f0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8f0cc-103">Bant genişliği zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="8f0cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f0cc-104">SYNTAX</span></span>

### <span data-ttu-id="8f0cc-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f0cc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f0cc-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8f0cc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f0cc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f0cc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f0cc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f0cc-108">DESCRIPTION</span></span>
<span data-ttu-id="8f0cc-109">**Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet 'ı bir veri kutusu uç aygıtının bant genişliği zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="8f0cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f0cc-110">EXAMPLES</span></span>

### <span data-ttu-id="8f0cc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8f0cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="8f0cc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f0cc-112">PARAMETERS</span></span>

### <span data-ttu-id="8f0cc-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8f0cc-113">-AsJob</span></span>
<span data-ttu-id="8f0cc-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8f0cc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f0cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f0cc-115">-DefaultProfile</span></span>
<span data-ttu-id="8f0cc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f0cc-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="8f0cc-117">-DeviceName</span></span>
<span data-ttu-id="8f0cc-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="8f0cc-118">Device Name</span></span>

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

### <span data-ttu-id="8f0cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f0cc-119">-InputObject</span></span>
<span data-ttu-id="8f0cc-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="8f0cc-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f0cc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f0cc-121">-Name</span></span>
<span data-ttu-id="8f0cc-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="8f0cc-122">Resource Name</span></span>

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

### <span data-ttu-id="8f0cc-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8f0cc-123">-PassThru</span></span>
<span data-ttu-id="8f0cc-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="8f0cc-124">returns true if successful</span></span>

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

### <span data-ttu-id="8f0cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f0cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f0cc-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8f0cc-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8f0cc-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f0cc-127">-ResourceId</span></span>
<span data-ttu-id="8f0cc-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f0cc-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8f0cc-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f0cc-129">-Confirm</span></span>
<span data-ttu-id="8f0cc-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f0cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f0cc-131">-WhatIf</span></span>
<span data-ttu-id="8f0cc-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f0cc-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f0cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f0cc-134">CommonParameters</span></span>
<span data-ttu-id="8f0cc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f0cc-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8f0cc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f0cc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f0cc-137">INPUTS</span></span>

### <span data-ttu-id="8f0cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8f0cc-138">System.String</span></span>

### <span data-ttu-id="8f0cc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="8f0cc-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="8f0cc-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f0cc-140">OUTPUTS</span></span>

### <span data-ttu-id="8f0cc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f0cc-141">System.Boolean</span></span>

## <span data-ttu-id="8f0cc-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f0cc-142">NOTES</span></span>

## <span data-ttu-id="8f0cc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f0cc-143">RELATED LINKS</span></span>
