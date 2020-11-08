---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109611"
---
# <span data-ttu-id="d769e-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="d769e-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="d769e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d769e-102">SYNOPSIS</span></span>
<span data-ttu-id="d769e-103">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d769e-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="d769e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d769e-104">SYNTAX</span></span>

### <span data-ttu-id="d769e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d769e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d769e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d769e-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d769e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d769e-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d769e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d769e-108">DESCRIPTION</span></span>
<span data-ttu-id="d769e-109">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d769e-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="d769e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d769e-110">EXAMPLES</span></span>

### <span data-ttu-id="d769e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d769e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="d769e-112">Cihaz için dağıtılmış izleme seçeneklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d769e-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="d769e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d769e-113">PARAMETERS</span></span>

### <span data-ttu-id="d769e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d769e-114">-DefaultProfile</span></span>
<span data-ttu-id="d769e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d769e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d769e-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="d769e-116">-DeviceId</span></span>
<span data-ttu-id="d769e-117">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="d769e-117">Target Device Id.</span></span>

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

### <span data-ttu-id="d769e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d769e-118">-InputObject</span></span>
<span data-ttu-id="d769e-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="d769e-119">IotHub object</span></span>

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

### <span data-ttu-id="d769e-120">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="d769e-120">-IotHubName</span></span>
<span data-ttu-id="d769e-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="d769e-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d769e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d769e-122">-ResourceGroupName</span></span>
<span data-ttu-id="d769e-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d769e-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d769e-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d769e-124">-ResourceId</span></span>
<span data-ttu-id="d769e-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d769e-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d769e-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="d769e-126">-SamplingMode</span></span>
<span data-ttu-id="d769e-127">Dağıtılmış izleme için örneklemeyi etkinleştirir ve devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d769e-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="d769e-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="d769e-128">-SamplingRate</span></span>
<span data-ttu-id="d769e-129">İzleme bağlamını eklemek için örneklenen ileti miktarını denetler.</span><span class="sxs-lookup"><span data-stu-id="d769e-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="d769e-130">Bu değer yüzde değeridir.</span><span class="sxs-lookup"><span data-stu-id="d769e-130">This value is a percentage.</span></span>
<span data-ttu-id="d769e-131">Yalnızca 0 ile 100 arasındaki değerlere izin verilir.</span><span class="sxs-lookup"><span data-stu-id="d769e-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="d769e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d769e-132">-Confirm</span></span>
<span data-ttu-id="d769e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d769e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d769e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d769e-134">-WhatIf</span></span>
<span data-ttu-id="d769e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d769e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d769e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d769e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d769e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d769e-137">CommonParameters</span></span>
<span data-ttu-id="d769e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d769e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d769e-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d769e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d769e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d769e-140">INPUTS</span></span>

### <span data-ttu-id="d769e-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="d769e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d769e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d769e-142">System.String</span></span>

## <span data-ttu-id="d769e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d769e-143">OUTPUTS</span></span>

### <span data-ttu-id="d769e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etyarış</span><span class="sxs-lookup"><span data-stu-id="d769e-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="d769e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d769e-145">NOTES</span></span>

## <span data-ttu-id="d769e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d769e-146">RELATED LINKS</span></span>
