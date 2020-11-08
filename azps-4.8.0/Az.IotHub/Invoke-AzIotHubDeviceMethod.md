---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdevicemethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeviceMethod.md
ms.openlocfilehash: 78247b26d2f8e6618d3999389efa509e3f8854b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109993"
---
# <span data-ttu-id="f2faf-101">Invoke-AzIotHubDeviceMethod</span><span class="sxs-lookup"><span data-stu-id="f2faf-101">Invoke-AzIotHubDeviceMethod</span></span>

## <span data-ttu-id="f2faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2faf-102">SYNOPSIS</span></span>
<span data-ttu-id="f2faf-103">Bir cihazda doğrudan yöntem çağırma.</span><span class="sxs-lookup"><span data-stu-id="f2faf-103">Invoke a direct method on a device.</span></span>

## <span data-ttu-id="f2faf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2faf-104">SYNTAX</span></span>

### <span data-ttu-id="f2faf-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2faf-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -Name <String> [-Payload <String>] [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2faf-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="f2faf-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-InputObject] <PSIotHub> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2faf-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="f2faf-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeviceMethod [-ResourceId] <String> [-DeviceId] <String> -Name <String> [-Payload <String>]
 [-ResponseTimeOut <Int32>] [-ConnectionTimeOut <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2faf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2faf-108">DESCRIPTION</span></span>
<span data-ttu-id="f2faf-109">Bir cihazda doğrudan yöntem çağırma.</span><span class="sxs-lookup"><span data-stu-id="f2faf-109">Invoke a direct method on a device.</span></span> <span data-ttu-id="f2faf-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methodsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="f2faf-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-direct-methods for more information.</span></span>

## <span data-ttu-id="f2faf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2faf-111">EXAMPLES</span></span>

### <span data-ttu-id="f2faf-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2faf-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeviceMethod -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Name "methodName" -ResponseTimeOut 20 -ConnectionTimeOut 15
```

<span data-ttu-id="f2faf-113">Bir cihaz yöntemi çağır.</span><span class="sxs-lookup"><span data-stu-id="f2faf-113">Invoke a device method.</span></span>

## <span data-ttu-id="f2faf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2faf-114">PARAMETERS</span></span>

### <span data-ttu-id="f2faf-115">-ConnectionTimeOut</span><span class="sxs-lookup"><span data-stu-id="f2faf-115">-ConnectionTimeOut</span></span>
<span data-ttu-id="f2faf-116">Bir bağlantı başarılı olana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="f2faf-116">Number of seconds to wait until a connection is successfully made.</span></span>
<span data-ttu-id="f2faf-117">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f2faf-117">Default is 10.</span></span>

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

### <span data-ttu-id="f2faf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2faf-118">-DefaultProfile</span></span>
<span data-ttu-id="f2faf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2faf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2faf-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="f2faf-120">-DeviceId</span></span>
<span data-ttu-id="f2faf-121">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="f2faf-121">Target Device Id.</span></span>

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

### <span data-ttu-id="f2faf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2faf-122">-InputObject</span></span>
<span data-ttu-id="f2faf-123">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="f2faf-123">IotHub object</span></span>

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

### <span data-ttu-id="f2faf-124">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="f2faf-124">-IotHubName</span></span>
<span data-ttu-id="f2faf-125">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="f2faf-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f2faf-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2faf-126">-Name</span></span>
<span data-ttu-id="f2faf-127">Bu cihazda çağrılacak yöntemin adı.</span><span class="sxs-lookup"><span data-stu-id="f2faf-127">The name of the method to invoke on this device.</span></span>

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

### <span data-ttu-id="f2faf-128">-Yük</span><span class="sxs-lookup"><span data-stu-id="f2faf-128">-Payload</span></span>
<span data-ttu-id="f2faf-129">Bu cihazda çağrılacak yöntemin yükü.</span><span class="sxs-lookup"><span data-stu-id="f2faf-129">The payload for the method to invoke on this device.</span></span>

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

### <span data-ttu-id="f2faf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2faf-130">-ResourceGroupName</span></span>
<span data-ttu-id="f2faf-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f2faf-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f2faf-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f2faf-132">-ResourceId</span></span>
<span data-ttu-id="f2faf-133">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f2faf-133">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f2faf-134">-ResponseTimeOut</span><span class="sxs-lookup"><span data-stu-id="f2faf-134">-ResponseTimeOut</span></span>
<span data-ttu-id="f2faf-135">Doğrudan yöntemden bir sonuç alınana kadar beklenecek saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="f2faf-135">Number of seconds to wait until a result is received from the direct method.</span></span>
<span data-ttu-id="f2faf-136">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="f2faf-136">Default is 10.</span></span>

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

### <span data-ttu-id="f2faf-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2faf-137">-Confirm</span></span>
<span data-ttu-id="f2faf-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2faf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2faf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2faf-139">-WhatIf</span></span>
<span data-ttu-id="f2faf-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2faf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2faf-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2faf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2faf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2faf-142">CommonParameters</span></span>
<span data-ttu-id="f2faf-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2faf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2faf-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2faf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2faf-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2faf-145">INPUTS</span></span>

### <span data-ttu-id="f2faf-146">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="f2faf-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f2faf-147">System. String</span><span class="sxs-lookup"><span data-stu-id="f2faf-147">System.String</span></span>

## <span data-ttu-id="f2faf-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2faf-148">OUTPUTS</span></span>

### <span data-ttu-id="f2faf-149">Microsoft. Azure. Commands. Management. IotHub. modeller. Pscses Todevicemethodresult</span><span class="sxs-lookup"><span data-stu-id="f2faf-149">Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceMethodResult</span></span>

## <span data-ttu-id="f2faf-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2faf-150">NOTES</span></span>

## <span data-ttu-id="f2faf-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2faf-151">RELATED LINKS</span></span>
