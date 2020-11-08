---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277205"
---
# <span data-ttu-id="ae750-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ae750-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="ae750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae750-102">SYNOPSIS</span></span>
<span data-ttu-id="ae750-103">Cihaz için rol güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ae750-103">Updates a Role for a device</span></span>

## <span data-ttu-id="ae750-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae750-104">SYNTAX</span></span>

### <span data-ttu-id="ae750-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ae750-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae750-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ae750-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae750-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae750-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae750-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae750-108">DESCRIPTION</span></span>
<span data-ttu-id="ae750-109">**Set-AzStackEdgeRole** cmdlet 'ı yığın uç aygıtı için IoT rolünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ae750-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="ae750-110">Eski takılan paylaşımlar, yeni sağlanan PaylaşımAdı, PaylaşımAdı parametresindeki dosyalarla değiştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="ae750-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="ae750-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae750-111">EXAMPLES</span></span>

### <span data-ttu-id="ae750-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ae750-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="ae750-113">Adları Paylaş, eski takılı paylaşımların yerine yeni sağlanan olanları değiştirir</span><span class="sxs-lookup"><span data-stu-id="ae750-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="ae750-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="ae750-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="ae750-115">Tüm paylaşımları çıkarmak için</span><span class="sxs-lookup"><span data-stu-id="ae750-115">To unmount all shares</span></span>

## <span data-ttu-id="ae750-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae750-116">PARAMETERS</span></span>

### <span data-ttu-id="ae750-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae750-117">-DefaultProfile</span></span>
<span data-ttu-id="ae750-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae750-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae750-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="ae750-119">-DeviceName</span></span>
<span data-ttu-id="ae750-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="ae750-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae750-121">-InputObject</span></span>
<span data-ttu-id="ae750-122">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="ae750-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae750-123">-Name</span></span>
<span data-ttu-id="ae750-124">Rolün adı</span><span class="sxs-lookup"><span data-stu-id="ae750-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae750-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae750-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ae750-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ae750-127">-ResourceId</span></span>
<span data-ttu-id="ae750-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ae750-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-129">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="ae750-129">-ShareName</span></span>
<span data-ttu-id="ae750-130">Rolde paylaşma</span><span class="sxs-lookup"><span data-stu-id="ae750-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae750-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae750-131">-Confirm</span></span>
<span data-ttu-id="ae750-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae750-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae750-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae750-133">-WhatIf</span></span>
<span data-ttu-id="ae750-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae750-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae750-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae750-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae750-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae750-136">CommonParameters</span></span>
<span data-ttu-id="ae750-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae750-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae750-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ae750-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae750-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae750-139">INPUTS</span></span>

### <span data-ttu-id="ae750-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ae750-140">System.String</span></span>

### <span data-ttu-id="ae750-141">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ae750-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="ae750-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae750-142">OUTPUTS</span></span>

### <span data-ttu-id="ae750-143">Microsoft. Azure. PowerShell. cmdlet. StackEdge. model. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="ae750-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="ae750-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae750-144">NOTES</span></span>

## <span data-ttu-id="ae750-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae750-145">RELATED LINKS</span></span>
