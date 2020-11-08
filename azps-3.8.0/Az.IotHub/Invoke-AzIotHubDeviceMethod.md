---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103816"
---
# <span data-ttu-id="f935a-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="f935a-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="f935a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f935a-102">SYNOPSIS</span></span>
<span data-ttu-id="f935a-103">Bir cihazda doğrudan yöntem çağırma.</span><span class="sxs-lookup"><span data-stu-id="f935a-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="f935a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f935a-104">SYNTAX</span></span>

### <span data-ttu-id="f935a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f935a-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f935a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="f935a-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f935a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="f935a-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f935a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f935a-108">DESCRIPTION</span></span>
<span data-ttu-id="f935a-109">Bir cihazda doğrudan yöntem çağırma.</span><span class="sxs-lookup"><span data-stu-id="f935a-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="f935a-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="f935a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="f935a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f935a-111">EXAMPLES</span></span>

### <span data-ttu-id="f935a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f935a-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="f935a-113">Bir cihaz yöntemi çağır.</span><span class="sxs-lookup"><span data-stu-id="f935a-113">Invoke a device method.</span></span>

## <span data-ttu-id="f935a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f935a-114">PARAMETERS</span></span>

### <span data-ttu-id="f935a-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="f935a-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="f935a-116">Bir bağlantı başarılı olana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="f935a-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="f935a-117">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f935a-117">Default is 10.</span></span>

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

### <span data-ttu-id="f935a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f935a-118">-DefaultProfile</span></span>
<span data-ttu-id="f935a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f935a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f935a-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="f935a-120">-DeviceId</span></span>
<span data-ttu-id="f935a-121">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="f935a-121">Target Device Id.</span></span>

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

### <span data-ttu-id="f935a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f935a-122">-InputObject</span></span>
<span data-ttu-id="f935a-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="f935a-123">IotHub object</span></span>

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

### <span data-ttu-id="f935a-124">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="f935a-124">-IotHubName</span></span>
<span data-ttu-id="f935a-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="f935a-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f935a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f935a-126">-Name</span></span>
<span data-ttu-id="f935a-127">Bu cihazda çağrılacak yöntemin adı.</span><span class="sxs-lookup"><span data-stu-id="f935a-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="f935a-128">-Yük</span><span class="sxs-lookup"><span data-stu-id="f935a-128">-Payload</span></span>
<span data-ttu-id="f935a-129">Bu cihazda çağrılacak yöntemin yükü.</span><span class="sxs-lookup"><span data-stu-id="f935a-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="f935a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f935a-130">-ResourceGroupName</span></span>
<span data-ttu-id="f935a-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f935a-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f935a-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f935a-132">-ResourceId</span></span>
<span data-ttu-id="f935a-133">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f935a-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f935a-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="f935a-134">-ResponseTimeOut</span></span>
<span data-ttu-id="f935a-135">Doğrudan yöntemden bir sonuç alınana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="f935a-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="f935a-136">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f935a-136">Default is 10.</span></span>

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

### <span data-ttu-id="f935a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="f935a-137">-Confirm</span></span>
<span data-ttu-id="f935a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f935a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f935a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f935a-139">-WhatIf</span></span>
<span data-ttu-id="f935a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f935a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f935a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f935a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f935a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f935a-142">CommonParameters</span></span>
<span data-ttu-id="f935a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f935a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f935a-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f935a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f935a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f935a-145">INPUTS</span></span>

### <span data-ttu-id="f935a-146">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="f935a-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f935a-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f935a-147">System.String</span></span>

## <span data-ttu-id="f935a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f935a-148">OUTPUTS</span></span>

### <span data-ttu-id="f935a-149">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscses Todevicemethodresult</span><span class="sxs-lookup"><span data-stu-id="f935a-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="f935a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f935a-150">NOTES</span></span>

## <span data-ttu-id="f935a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f935a-151">RELATED LINKS</span></span>
