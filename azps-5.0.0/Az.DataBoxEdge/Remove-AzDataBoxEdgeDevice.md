---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321153"
---
# <span data-ttu-id="95ed9-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="95ed9-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="95ed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="95ed9-103">Bir veri kutusu uç aygıtını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95ed9-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="95ed9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95ed9-104">SYNTAX</span></span>

### <span data-ttu-id="95ed9-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="95ed9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ed9-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="95ed9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95ed9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95ed9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95ed9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="95ed9-108">DESCRIPTION</span></span>
<span data-ttu-id="95ed9-109">**Remove-AzDataBoxEdgeDevice** cmdlet 'i, bir veri kutusu uç aygıtının yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95ed9-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="95ed9-110">Cihazın yalnızca sipariş yerleştirdikten ve cihaz Microsoft tarafından sevkıyata hazırlanmadan önce silinebilirler.</span><span class="sxs-lookup"><span data-stu-id="95ed9-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="95ed9-111">Bu [cmdlet 'i](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) kullanmadan önce kaynağı silme hakkındaki belgelere bakın</span><span class="sxs-lookup"><span data-stu-id="95ed9-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="95ed9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95ed9-112">EXAMPLES</span></span>

### <span data-ttu-id="95ed9-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95ed9-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="95ed9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95ed9-114">PARAMETERS</span></span>

### <span data-ttu-id="95ed9-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="95ed9-115">-AsJob</span></span>
<span data-ttu-id="95ed9-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="95ed9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95ed9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ed9-117">-DefaultProfile</span></span>
<span data-ttu-id="95ed9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95ed9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ed9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ed9-119">-InputObject</span></span>
<span data-ttu-id="95ed9-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="95ed9-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95ed9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="95ed9-121">-Name</span></span>
<span data-ttu-id="95ed9-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="95ed9-122">Resource Name</span></span>

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

### <span data-ttu-id="95ed9-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="95ed9-123">-PassThru</span></span>
<span data-ttu-id="95ed9-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="95ed9-124">returns true if successful</span></span>

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

### <span data-ttu-id="95ed9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ed9-125">-ResourceGroupName</span></span>
<span data-ttu-id="95ed9-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="95ed9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="95ed9-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="95ed9-127">-ResourceId</span></span>
<span data-ttu-id="95ed9-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="95ed9-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="95ed9-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="95ed9-129">-Confirm</span></span>
<span data-ttu-id="95ed9-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95ed9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ed9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ed9-131">-WhatIf</span></span>
<span data-ttu-id="95ed9-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95ed9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95ed9-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95ed9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ed9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ed9-134">CommonParameters</span></span>
<span data-ttu-id="95ed9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95ed9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ed9-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95ed9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ed9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95ed9-137">INPUTS</span></span>

### <span data-ttu-id="95ed9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="95ed9-138">System.String</span></span>

### <span data-ttu-id="95ed9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="95ed9-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="95ed9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95ed9-140">OUTPUTS</span></span>

### <span data-ttu-id="95ed9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95ed9-141">System.Boolean</span></span>

## <span data-ttu-id="95ed9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95ed9-142">NOTES</span></span>

## <span data-ttu-id="95ed9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95ed9-143">RELATED LINKS</span></span>
