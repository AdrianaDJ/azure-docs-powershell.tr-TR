---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096890"
---
# <span data-ttu-id="56dda-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="56dda-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="56dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56dda-102">SYNOPSIS</span></span>
<span data-ttu-id="56dda-103">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="56dda-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="56dda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56dda-104">SYNTAX</span></span>

### <span data-ttu-id="56dda-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56dda-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56dda-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="56dda-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56dda-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="56dda-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56dda-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56dda-108">DESCRIPTION</span></span>
<span data-ttu-id="56dda-109">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="56dda-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="56dda-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56dda-110">EXAMPLES</span></span>

### <span data-ttu-id="56dda-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56dda-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="56dda-112">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="56dda-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="56dda-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56dda-113">PARAMETERS</span></span>

### <span data-ttu-id="56dda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56dda-114">-DefaultProfile</span></span>
<span data-ttu-id="56dda-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56dda-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56dda-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="56dda-116">-DeviceId</span></span>
<span data-ttu-id="56dda-117">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="56dda-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56dda-118">-InputObject</span></span>
<span data-ttu-id="56dda-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="56dda-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-120">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="56dda-120">-IotHubName</span></span>
<span data-ttu-id="56dda-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="56dda-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56dda-122">-ResourceGroupName</span></span>
<span data-ttu-id="56dda-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="56dda-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="56dda-124">-ResourceId</span></span>
<span data-ttu-id="56dda-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="56dda-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="56dda-126">-SamplingMode</span></span>
<span data-ttu-id="56dda-127">Dağıtılmış izleme için örneklemeyi etkinleştirir ve devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="56dda-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="56dda-128">-SamplingRate</span></span>
<span data-ttu-id="56dda-129">İzleme bağlamını eklemek için örneklenen ileti miktarını denetler.</span><span class="sxs-lookup"><span data-stu-id="56dda-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="56dda-130">Bu değer yüzde değeridir.</span><span class="sxs-lookup"><span data-stu-id="56dda-130">This value is a percentage.</span></span>
<span data-ttu-id="56dda-131">Yalnızca 0 ile 100 arasındaki değerlere izin verilir.</span><span class="sxs-lookup"><span data-stu-id="56dda-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56dda-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="56dda-132">-Confirm</span></span>
<span data-ttu-id="56dda-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56dda-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56dda-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56dda-134">-WhatIf</span></span>
<span data-ttu-id="56dda-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56dda-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56dda-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56dda-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56dda-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56dda-137">CommonParameters</span></span>
<span data-ttu-id="56dda-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56dda-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56dda-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56dda-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56dda-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56dda-140">INPUTS</span></span>

### <span data-ttu-id="56dda-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="56dda-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56dda-142">System. String</span><span class="sxs-lookup"><span data-stu-id="56dda-142">System.String</span></span>

## <span data-ttu-id="56dda-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56dda-143">OUTPUTS</span></span>

### <span data-ttu-id="56dda-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etyarış</span><span class="sxs-lookup"><span data-stu-id="56dda-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="56dda-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56dda-145">NOTES</span></span>

## <span data-ttu-id="56dda-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56dda-146">RELATED LINKS</span></span>
