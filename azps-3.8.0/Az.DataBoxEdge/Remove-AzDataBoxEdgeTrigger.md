---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104567"
---
# <span data-ttu-id="cd185-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cd185-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cd185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd185-102">SYNOPSIS</span></span>
<span data-ttu-id="cd185-103">Cihazda varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd185-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="cd185-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd185-104">SYNTAX</span></span>

### <span data-ttu-id="cd185-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd185-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd185-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cd185-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd185-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd185-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd185-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd185-108">DESCRIPTION</span></span>
<span data-ttu-id="cd185-109">**Remove-AzDataBoxEdgeTrigger** cmdlet 'ı, veri kutusu Edge cihazında varolan bir tetikleyiciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cd185-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="cd185-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd185-110">EXAMPLES</span></span>

### <span data-ttu-id="cd185-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd185-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="cd185-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd185-112">PARAMETERS</span></span>

### <span data-ttu-id="cd185-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd185-113">-AsJob</span></span>
<span data-ttu-id="cd185-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd185-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd185-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd185-115">-DefaultProfile</span></span>
<span data-ttu-id="cd185-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd185-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd185-117">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="cd185-117">-DeviceName</span></span>
<span data-ttu-id="cd185-118">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="cd185-118">Device Name</span></span>

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

### <span data-ttu-id="cd185-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd185-119">-InputObject</span></span>
<span data-ttu-id="cd185-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="cd185-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd185-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd185-121">-Name</span></span>
<span data-ttu-id="cd185-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="cd185-122">Resource Name</span></span>

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

### <span data-ttu-id="cd185-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cd185-123">-PassThru</span></span>
<span data-ttu-id="cd185-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="cd185-124">returns true if successful</span></span>

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

### <span data-ttu-id="cd185-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd185-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd185-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cd185-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cd185-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd185-127">-ResourceId</span></span>
<span data-ttu-id="cd185-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd185-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd185-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd185-129">-Confirm</span></span>
<span data-ttu-id="cd185-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd185-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd185-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd185-131">-WhatIf</span></span>
<span data-ttu-id="cd185-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd185-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd185-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd185-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd185-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd185-134">CommonParameters</span></span>
<span data-ttu-id="cd185-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd185-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd185-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cd185-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd185-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd185-137">INPUTS</span></span>

### <span data-ttu-id="cd185-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cd185-138">System.String</span></span>

### <span data-ttu-id="cd185-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="cd185-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="cd185-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd185-140">OUTPUTS</span></span>

### <span data-ttu-id="cd185-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd185-141">System.Boolean</span></span>

## <span data-ttu-id="cd185-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd185-142">NOTES</span></span>

## <span data-ttu-id="cd185-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd185-143">RELATED LINKS</span></span>
