---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmodulemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubModuleMethod.md
ms.openlocfilehash: e9faa07f4addabcb556819e1d45b63a0dec0f6b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280260"
---
# <span data-ttu-id="e29f5-101">Invoke-AzIotHubModuleMethod</span><span class="sxs-lookup"><span data-stu-id="e29f5-101">Invoke-AzIotHubModuleMethod</span></span>

## <span data-ttu-id="e29f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29f5-102">SYNOPSIS</span></span>
<span data-ttu-id="e29f5-103">Edge modülü yöntemini çağırma.</span><span class="sxs-lookup"><span data-stu-id="e29f5-103">Invoke an Edge module method.</span></span>

## <span data-ttu-id="e29f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e29f5-104">SYNTAX</span></span>

### <span data-ttu-id="e29f5-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e29f5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId] <String> -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>]
 [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e29f5-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="e29f5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubModuleMethod [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29f5-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e29f5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubModuleMethod [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String> -Name <String>
 [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e29f5-108">DESCRIPTION</span></span>
<span data-ttu-id="e29f5-109">Edge modülü yöntemini çağırma.</span><span class="sxs-lookup"><span data-stu-id="e29f5-109">Invoke an Edge module method.</span></span> <span data-ttu-id="e29f5-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="e29f5-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="e29f5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e29f5-111">EXAMPLES</span></span>

### <span data-ttu-id="e29f5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e29f5-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubModuleMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Name "methodName" -Payload "method-input" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="e29f5-113">Edge modülü yöntemini çağırma.</span><span class="sxs-lookup"><span data-stu-id="e29f5-113">Invoke an Edge module method.</span></span>

## <span data-ttu-id="e29f5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e29f5-114">PARAMETERS</span></span>

### <span data-ttu-id="e29f5-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="e29f5-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="e29f5-116">Bir bağlantı başarılı olana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="e29f5-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="e29f5-117">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e29f5-117">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29f5-118">-DefaultProfile</span></span>
<span data-ttu-id="e29f5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e29f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29f5-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="e29f5-120">-DeviceId</span></span>
<span data-ttu-id="e29f5-121">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="e29f5-121">Target Device Id.</span></span>

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

### <span data-ttu-id="e29f5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e29f5-122">-InputObject</span></span>
<span data-ttu-id="e29f5-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="e29f5-123">IotHub object</span></span>

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

### <span data-ttu-id="e29f5-124">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="e29f5-124">-IotHubName</span></span>
<span data-ttu-id="e29f5-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="e29f5-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e29f5-126">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="e29f5-126">-ModuleId</span></span>
<span data-ttu-id="e29f5-127">Hedef cihazın modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="e29f5-127">Target device's module id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e29f5-128">-Name</span></span>
<span data-ttu-id="e29f5-129">Bu cihaz modülünde çağrılacak yöntemin adı.</span><span class="sxs-lookup"><span data-stu-id="e29f5-129">The name of the method to invoke on this device module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f5-130">-Yük</span><span class="sxs-lookup"><span data-stu-id="e29f5-130">-Payload</span></span>
<span data-ttu-id="e29f5-131">Bu cihaz modülünde çağrılacak yöntemin yükü.</span><span class="sxs-lookup"><span data-stu-id="e29f5-131">The payload for the method to invoke on this device module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29f5-132">-ResourceGroupName</span></span>
<span data-ttu-id="e29f5-133">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="e29f5-133">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e29f5-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e29f5-134">-ResourceId</span></span>
<span data-ttu-id="e29f5-135">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e29f5-135">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e29f5-136">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="e29f5-136">-ResponseTimeOut</span></span>
<span data-ttu-id="e29f5-137">Doğrudan yöntemden bir sonuç alınana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="e29f5-137">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="e29f5-138">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e29f5-138">Default is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f5-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="e29f5-139">-Confirm</span></span>
<span data-ttu-id="e29f5-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e29f5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29f5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29f5-141">-WhatIf</span></span>
<span data-ttu-id="e29f5-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e29f5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29f5-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e29f5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29f5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29f5-144">CommonParameters</span></span>
<span data-ttu-id="e29f5-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e29f5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29f5-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29f5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29f5-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e29f5-147">INPUTS</span></span>

### <span data-ttu-id="e29f5-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="e29f5-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e29f5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e29f5-149">System.String</span></span>

## <span data-ttu-id="e29f5-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e29f5-150">OUTPUTS</span></span>

### <span data-ttu-id="e29f5-151">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscses Todevicemethodresult</span><span class="sxs-lookup"><span data-stu-id="e29f5-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="e29f5-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e29f5-152">NOTES</span></span>

## <span data-ttu-id="e29f5-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e29f5-153">RELATED LINKS</span></span>
