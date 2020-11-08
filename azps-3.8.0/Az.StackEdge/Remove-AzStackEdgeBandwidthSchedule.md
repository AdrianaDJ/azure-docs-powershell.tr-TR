---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096214"
---
# <span data-ttu-id="1b0bd-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="1b0bd-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="1b0bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0bd-103">Bant genişliği zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="1b0bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b0bd-104">SYNTAX</span></span>

### <span data-ttu-id="1b0bd-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b0bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b0bd-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1b0bd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b0bd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0bd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b0bd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b0bd-108">DESCRIPTION</span></span>
<span data-ttu-id="1b0bd-109">**Remove-AzStackEdgeBandwidthSchedule** cmdlet 'ı, yığın uç aygıtının bant genişliği zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="1b0bd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b0bd-110">EXAMPLES</span></span>

### <span data-ttu-id="1b0bd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b0bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="1b0bd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b0bd-112">PARAMETERS</span></span>

### <span data-ttu-id="1b0bd-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="1b0bd-113">-AsJob</span></span>
<span data-ttu-id="1b0bd-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1b0bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b0bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0bd-115">-DefaultProfile</span></span>
<span data-ttu-id="1b0bd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b0bd-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="1b0bd-117">-DeviceName</span></span>
<span data-ttu-id="1b0bd-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="1b0bd-118">Device Name</span></span>

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

### <span data-ttu-id="1b0bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b0bd-119">-InputObject</span></span>
<span data-ttu-id="1b0bd-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="1b0bd-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b0bd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b0bd-121">-Name</span></span>
<span data-ttu-id="1b0bd-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="1b0bd-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b0bd-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1b0bd-123">-PassThru</span></span>
<span data-ttu-id="1b0bd-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="1b0bd-124">returns true if successful</span></span>

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

### <span data-ttu-id="1b0bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b0bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b0bd-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="1b0bd-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1b0bd-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b0bd-127">-ResourceId</span></span>
<span data-ttu-id="1b0bd-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1b0bd-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1b0bd-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b0bd-129">-Confirm</span></span>
<span data-ttu-id="1b0bd-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b0bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b0bd-131">-WhatIf</span></span>
<span data-ttu-id="1b0bd-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b0bd-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b0bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0bd-134">CommonParameters</span></span>
<span data-ttu-id="1b0bd-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0bd-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b0bd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0bd-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b0bd-137">INPUTS</span></span>

### <span data-ttu-id="1b0bd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b0bd-138">System.String</span></span>

### <span data-ttu-id="1b0bd-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="1b0bd-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="1b0bd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b0bd-140">OUTPUTS</span></span>

### <span data-ttu-id="1b0bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b0bd-141">System.Boolean</span></span>

## <span data-ttu-id="1b0bd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b0bd-142">NOTES</span></span>

## <span data-ttu-id="1b0bd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b0bd-143">RELATED LINKS</span></span>