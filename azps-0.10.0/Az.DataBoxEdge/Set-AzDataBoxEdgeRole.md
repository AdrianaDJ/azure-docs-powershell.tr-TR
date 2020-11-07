---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 22dee84aadc590d140d64cbd71eeaed3c16f03e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935923"
---
# <span data-ttu-id="2c1f3-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="2c1f3-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="2c1f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1f3-103">Cihaz için rol güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2c1f3-103">Updates a Role for a device</span></span>

## <span data-ttu-id="2c1f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c1f3-104">SYNTAX</span></span>

### <span data-ttu-id="2c1f3-105">SetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c1f3-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1f3-106">Setbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2c1f3-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c1f3-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c1f3-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c1f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c1f3-108">DESCRIPTION</span></span>
<span data-ttu-id="2c1f3-109">**Set-AzDataBoxEdgeRole** cmdlet 'ı bir veri kutusu uç aygıtı için IoT rolünü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="2c1f3-110">Eski takılan paylaşımlar, yeni sağlanan PaylaşımAdı, PaylaşımAdı parametresindeki dosyalarla değiştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="2c1f3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c1f3-111">EXAMPLES</span></span>

### <span data-ttu-id="2c1f3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c1f3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="2c1f3-113">Adları Paylaş, eski takılı paylaşımların yerine yeni sağlanan olanları değiştirir</span><span class="sxs-lookup"><span data-stu-id="2c1f3-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="2c1f3-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2c1f3-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="2c1f3-115">Tüm paylaşımları çıkarmak için</span><span class="sxs-lookup"><span data-stu-id="2c1f3-115">To unmount all shares</span></span>

## <span data-ttu-id="2c1f3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c1f3-116">PARAMETERS</span></span>

### <span data-ttu-id="2c1f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1f3-117">-DefaultProfile</span></span>
<span data-ttu-id="2c1f3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1f3-119">-Aygıtadı</span><span class="sxs-lookup"><span data-stu-id="2c1f3-119">-DeviceName</span></span>
<span data-ttu-id="2c1f3-120">Cihaz adı</span><span class="sxs-lookup"><span data-stu-id="2c1f3-120">Device Name</span></span>

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

### <span data-ttu-id="2c1f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c1f3-121">-InputObject</span></span>
<span data-ttu-id="2c1f3-122">Lütfen ilgili cihaz nesnesini sağlayın</span><span class="sxs-lookup"><span data-stu-id="2c1f3-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c1f3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c1f3-123">-Name</span></span>
<span data-ttu-id="2c1f3-124">Rolün adı</span><span class="sxs-lookup"><span data-stu-id="2c1f3-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c1f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="2c1f3-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2c1f3-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2c1f3-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c1f3-127">-ResourceId</span></span>
<span data-ttu-id="2c1f3-128">Azure RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c1f3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="2c1f3-129">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="2c1f3-129">-ShareName</span></span>
<span data-ttu-id="2c1f3-130">Rolde paylaşma</span><span class="sxs-lookup"><span data-stu-id="2c1f3-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c1f3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c1f3-131">-Confirm</span></span>
<span data-ttu-id="2c1f3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1f3-133">-WhatIf</span></span>
<span data-ttu-id="2c1f3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c1f3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c1f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1f3-136">CommonParameters</span></span>
<span data-ttu-id="2c1f3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1f3-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c1f3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1f3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c1f3-139">INPUTS</span></span>

### <span data-ttu-id="2c1f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c1f3-140">System.String</span></span>

### <span data-ttu-id="2c1f3-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="2c1f3-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="2c1f3-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c1f3-142">OUTPUTS</span></span>

### <span data-ttu-id="2c1f3-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="2c1f3-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="2c1f3-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c1f3-144">NOTES</span></span>

## <span data-ttu-id="2c1f3-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c1f3-145">RELATED LINKS</span></span>
