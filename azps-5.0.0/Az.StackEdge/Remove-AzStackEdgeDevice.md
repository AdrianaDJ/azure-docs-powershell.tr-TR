---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322281"
---
# <span data-ttu-id="6fdf2-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6fdf2-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="6fdf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fdf2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdf2-103">Yığın uç aygıtını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="6fdf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fdf2-104">SYNTAX</span></span>

### <span data-ttu-id="6fdf2-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fdf2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fdf2-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6fdf2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fdf2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fdf2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fdf2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fdf2-108">DESCRIPTION</span></span>
<span data-ttu-id="6fdf2-109">**Remove-AzStackEdgeDevice** cmdlet 'ı yığın uç aygıtının yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="6fdf2-110">Cihazın yalnızca sipariş yerleştirdikten ve cihaz Microsoft tarafından sevkıyata hazırlanmadan önce silinebilirler.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="6fdf2-111">Bu [cmdlet 'i](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) kullanmadan önce kaynağı silme hakkındaki belgelere bakın</span><span class="sxs-lookup"><span data-stu-id="6fdf2-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="6fdf2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fdf2-112">EXAMPLES</span></span>

### <span data-ttu-id="6fdf2-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fdf2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="6fdf2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fdf2-114">PARAMETERS</span></span>

### <span data-ttu-id="6fdf2-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="6fdf2-115">-AsJob</span></span>
<span data-ttu-id="6fdf2-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6fdf2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fdf2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdf2-117">-DefaultProfile</span></span>
<span data-ttu-id="6fdf2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fdf2-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="6fdf2-119">-DeviceObject</span></span>
<span data-ttu-id="6fdf2-120">Giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fdf2-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fdf2-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fdf2-121">-Name</span></span>
<span data-ttu-id="6fdf2-122">Kaynak adı</span><span class="sxs-lookup"><span data-stu-id="6fdf2-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fdf2-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6fdf2-123">-PassThru</span></span>
<span data-ttu-id="6fdf2-124">başarılı olursa doğru verir</span><span class="sxs-lookup"><span data-stu-id="6fdf2-124">returns true if successful</span></span>

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

### <span data-ttu-id="6fdf2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdf2-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fdf2-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6fdf2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6fdf2-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fdf2-127">-ResourceId</span></span>
<span data-ttu-id="6fdf2-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fdf2-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="6fdf2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fdf2-129">-Confirm</span></span>
<span data-ttu-id="6fdf2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fdf2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fdf2-131">-WhatIf</span></span>
<span data-ttu-id="6fdf2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fdf2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fdf2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdf2-134">CommonParameters</span></span>
<span data-ttu-id="6fdf2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdf2-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6fdf2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdf2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fdf2-137">INPUTS</span></span>

### <span data-ttu-id="6fdf2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6fdf2-138">System.String</span></span>

### <span data-ttu-id="6fdf2-139">Microsoft. Azure. PowerShell. cmdlet. StackEdge. modeller. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6fdf2-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="6fdf2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fdf2-140">OUTPUTS</span></span>

### <span data-ttu-id="6fdf2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fdf2-141">System.Boolean</span></span>

## <span data-ttu-id="6fdf2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fdf2-142">NOTES</span></span>

## <span data-ttu-id="6fdf2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fdf2-143">RELATED LINKS</span></span>
