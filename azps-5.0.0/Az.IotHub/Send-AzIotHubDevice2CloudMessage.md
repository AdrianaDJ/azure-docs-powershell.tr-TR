---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/send-aziothubdevice2cloudmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Send-AzIotHubDevice2CloudMessage.md
ms.openlocfilehash: 2445ba6a4436af1dad4b940d18c5576bdf9a5bfc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319965"
---
# <span data-ttu-id="fdbd4-101">Send-AzIotHubDevice2CloudMessage</span><span class="sxs-lookup"><span data-stu-id="fdbd4-101">Send-AzIotHubDevice2CloudMessage</span></span>

## <span data-ttu-id="fdbd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdbd4-102">SYNOPSIS</span></span>
<span data-ttu-id="fdbd4-103">Aygıttan buluta ileti gönderme.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-103">Send device-to-cloud message.</span></span>

## <span data-ttu-id="fdbd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdbd4-104">SYNTAX</span></span>

### <span data-ttu-id="fdbd4-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fdbd4-105">ResourceSet (Default)</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -Message <String> [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdbd4-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="fdbd4-106">InputObjectSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-InputObject] <PSIotHub> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdbd4-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="fdbd4-107">ResourceIdSet</span></span>
```
Send-AzIotHubDevice2CloudMessage [-ResourceId] <String> -DeviceId <String> -Message <String>
 [-TransportType <PSTransportType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fdbd4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdbd4-108">DESCRIPTION</span></span>
<span data-ttu-id="fdbd4-109">Komut, uygulama ve sistem özellikleriyle ileti gönderilmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-109">The command supports sending messages with application and system properties.</span></span>

## <span data-ttu-id="fdbd4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdbd4-110">EXAMPLES</span></span>

### <span data-ttu-id="fdbd4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fdbd4-111">Example 1</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS"
```

<span data-ttu-id="fdbd4-112">Varsayılan aktarım türünü kullanarak bulut iletisine cihaz gönderiliyor.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-112">Sending device to cloud message using default transport type.</span></span>

### <span data-ttu-id="fdbd4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fdbd4-113">Example 2</span></span>
```powershell
PS C:\> Send-AzIotHubDevice2CloudMessage -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Message "Ping from PS" -TransportType Mqtt
```

<span data-ttu-id="fdbd4-114">Bir MQTT cihazı bulut iletisine gönderiliyor.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-114">Sending an mqtt device to cloud message.</span></span>

## <span data-ttu-id="fdbd4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdbd4-115">PARAMETERS</span></span>

### <span data-ttu-id="fdbd4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdbd4-116">-DefaultProfile</span></span>
<span data-ttu-id="fdbd4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdbd4-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="fdbd4-118">-DeviceId</span></span>
<span data-ttu-id="fdbd4-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-119">Target Device Id.</span></span>

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

### <span data-ttu-id="fdbd4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdbd4-120">-InputObject</span></span>
<span data-ttu-id="fdbd4-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="fdbd4-121">IotHub object</span></span>

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

### <span data-ttu-id="fdbd4-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="fdbd4-122">-IotHubName</span></span>
<span data-ttu-id="fdbd4-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="fdbd4-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fdbd4-124">-İleti</span><span class="sxs-lookup"><span data-stu-id="fdbd4-124">-Message</span></span>
<span data-ttu-id="fdbd4-125">IoT Hub 'ına gönderilecek ileti gövdesi.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-125">Message body to send to IoT Hub.</span></span>

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

### <span data-ttu-id="fdbd4-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fdbd4-126">-PassThru</span></span>
<span data-ttu-id="fdbd4-127">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-127">Allows to return the boolean object.</span></span> <span data-ttu-id="fdbd4-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fdbd4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdbd4-129">-ResourceGroupName</span></span>
<span data-ttu-id="fdbd4-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="fdbd4-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fdbd4-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fdbd4-131">-ResourceId</span></span>
<span data-ttu-id="fdbd4-132">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fdbd4-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fdbd4-133">-TransportType</span><span class="sxs-lookup"><span data-stu-id="fdbd4-133">-TransportType</span></span>
<span data-ttu-id="fdbd4-134">Kullanılacak taşıma türü.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-134">Transport type to use.</span></span>
<span data-ttu-id="fdbd4-135">Varsayılan AMQP.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-135">Default is Amqp.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSTransportType
Parameter Sets: (All)
Aliases:
Accepted values: Amqp, Http1, Amqp_WebSocket_Only, Amqp_Tcp_Only, Mqtt, Mqtt_WebSocket_Only, Mqtt_Tcp_Only

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdbd4-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdbd4-136">-Confirm</span></span>
<span data-ttu-id="fdbd4-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdbd4-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdbd4-138">-WhatIf</span></span>
<span data-ttu-id="fdbd4-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdbd4-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdbd4-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdbd4-141">CommonParameters</span></span>
<span data-ttu-id="fdbd4-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdbd4-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdbd4-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdbd4-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdbd4-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdbd4-144">INPUTS</span></span>

### <span data-ttu-id="fdbd4-145">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="fdbd4-145">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fdbd4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fdbd4-146">System.String</span></span>

## <span data-ttu-id="fdbd4-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdbd4-147">OUTPUTS</span></span>

### <span data-ttu-id="fdbd4-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdbd4-148">System.Boolean</span></span>

## <span data-ttu-id="fdbd4-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdbd4-149">NOTES</span></span>

## <span data-ttu-id="fdbd4-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdbd4-150">RELATED LINKS</span></span>
