---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098882"
---
# <span data-ttu-id="ae6d9-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ae6d9-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="ae6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6d9-103">Bir paylaşımda belirli eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="ae6d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae6d9-104">SYNTAX</span></span>

### <span data-ttu-id="ae6d9-105">Invokebynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae6d9-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae6d9-106">Invokebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ae6d9-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae6d9-107">Invokebyinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="ae6d9-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6d9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae6d9-108">DESCRIPTION</span></span>
<span data-ttu-id="ae6d9-109">**Invoke-Azdataboxedgesshare** cmdlet 'ı, veri kutusu uç aygıtındaki bir paylaşımdaki verileri yenileme eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="ae6d9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae6d9-110">EXAMPLES</span></span>

### <span data-ttu-id="ae6d9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae6d9-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="ae6d9-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ae6d9-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="ae6d9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae6d9-113">PARAMETERS</span></span>

### <span data-ttu-id="ae6d9-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ae6d9-114">-AsJob</span></span>
<span data-ttu-id="ae6d9-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ae6d9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae6d9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6d9-116">-DefaultProfile</span></span>
<span data-ttu-id="ae6d9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6d9-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="ae6d9-118">-DeviceName</span></span>
<span data-ttu-id="ae6d9-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="ae6d9-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae6d9-120">-InputObject</span></span>
<span data-ttu-id="ae6d9-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="ae6d9-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae6d9-122">-Name</span></span>
<span data-ttu-id="ae6d9-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="ae6d9-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d9-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ae6d9-124">-PassThru</span></span>
<span data-ttu-id="ae6d9-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="ae6d9-125">returns true if successful</span></span>

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

### <span data-ttu-id="ae6d9-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="ae6d9-126">-RefreshData</span></span>
<span data-ttu-id="ae6d9-127">Buluttan verileri buluttan paylaşma</span><span class="sxs-lookup"><span data-stu-id="ae6d9-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="ae6d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ae6d9-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ae6d9-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d9-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ae6d9-130">-ResourceId</span></span>
<span data-ttu-id="ae6d9-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ae6d9-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6d9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae6d9-132">-Confirm</span></span>
<span data-ttu-id="ae6d9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6d9-134">-WhatIf</span></span>
<span data-ttu-id="ae6d9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae6d9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6d9-137">CommonParameters</span></span>
<span data-ttu-id="ae6d9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6d9-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ae6d9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6d9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae6d9-140">INPUTS</span></span>

### <span data-ttu-id="ae6d9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6d9-141">System.String</span></span>

### <span data-ttu-id="ae6d9-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaboxedges,</span><span class="sxs-lookup"><span data-stu-id="ae6d9-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="ae6d9-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae6d9-143">OUTPUTS</span></span>

### <span data-ttu-id="ae6d9-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae6d9-144">System.Boolean</span></span>

## <span data-ttu-id="ae6d9-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae6d9-145">NOTES</span></span>

## <span data-ttu-id="ae6d9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae6d9-146">RELATED LINKS</span></span>
