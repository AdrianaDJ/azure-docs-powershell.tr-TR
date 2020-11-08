---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096522"
---
# <span data-ttu-id="fb6e3-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="fb6e3-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="fb6e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6e3-103">Bir paylaşımda belirli eylemleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="fb6e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb6e3-104">SYNTAX</span></span>

### <span data-ttu-id="fb6e3-105">Invokebynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb6e3-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb6e3-106">Invokebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fb6e3-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb6e3-107">Invokebyinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="fb6e3-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb6e3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb6e3-108">DESCRIPTION</span></span>
<span data-ttu-id="fb6e3-109">**Invoke-Azstackedgesshare** cmdlet 'ı, yığın uç aygıtındaki bir paylaşımdaki verileri yenileme eylemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="fb6e3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb6e3-110">EXAMPLES</span></span>

### <span data-ttu-id="fb6e3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fb6e3-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="fb6e3-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fb6e3-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="fb6e3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb6e3-113">PARAMETERS</span></span>

### <span data-ttu-id="fb6e3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="fb6e3-114">-AsJob</span></span>
<span data-ttu-id="fb6e3-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fb6e3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb6e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6e3-116">-DefaultProfile</span></span>
<span data-ttu-id="fb6e3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb6e3-118">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="fb6e3-118">-DeviceName</span></span>
<span data-ttu-id="fb6e3-119">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="fb6e3-119">Device Name</span></span>

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

### <span data-ttu-id="fb6e3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6e3-120">-InputObject</span></span>
<span data-ttu-id="fb6e3-121">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb6e3-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb6e3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb6e3-122">-Name</span></span>
<span data-ttu-id="fb6e3-123">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="fb6e3-123">Resource Name</span></span>

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

### <span data-ttu-id="fb6e3-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fb6e3-124">-PassThru</span></span>
<span data-ttu-id="fb6e3-125">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="fb6e3-125">returns true if successful</span></span>

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

### <span data-ttu-id="fb6e3-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="fb6e3-126">-RefreshData</span></span>
<span data-ttu-id="fb6e3-127">Buluttan verileri buluttan paylaşma</span><span class="sxs-lookup"><span data-stu-id="fb6e3-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="fb6e3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6e3-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb6e3-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fb6e3-129">Resource Group Name</span></span>

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

### <span data-ttu-id="fb6e3-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb6e3-130">-ResourceId</span></span>
<span data-ttu-id="fb6e3-131">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb6e3-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="fb6e3-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="fb6e3-132">-Confirm</span></span>
<span data-ttu-id="fb6e3-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6e3-134">-WhatIf</span></span>
<span data-ttu-id="fb6e3-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb6e3-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6e3-137">CommonParameters</span></span>
<span data-ttu-id="fb6e3-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6e3-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fb6e3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6e3-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb6e3-140">INPUTS</span></span>

### <span data-ttu-id="fb6e3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fb6e3-141">System.String</span></span>

### <span data-ttu-id="fb6e3-142">Microsoft. Azure. PowerShell. cmdlet. yığın</span><span class="sxs-lookup"><span data-stu-id="fb6e3-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="fb6e3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb6e3-143">OUTPUTS</span></span>

### <span data-ttu-id="fb6e3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb6e3-144">System.Boolean</span></span>

## <span data-ttu-id="fb6e3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb6e3-145">NOTES</span></span>

## <span data-ttu-id="fb6e3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb6e3-146">RELATED LINKS</span></span>
