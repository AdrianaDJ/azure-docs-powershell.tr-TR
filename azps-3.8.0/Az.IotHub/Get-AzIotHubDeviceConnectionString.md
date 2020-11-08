---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098478"
---
# <span data-ttu-id="a75a3-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a75a3-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="a75a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a75a3-103">Bir IoT Hub 'ında hedef IoT aygıtının bağlantı dizesini edinin.</span><span class="sxs-lookup"><span data-stu-id="a75a3-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="a75a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a75a3-104">SYNTAX</span></span>

### <span data-ttu-id="a75a3-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a75a3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a75a3-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a75a3-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a75a3-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a75a3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a75a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a75a3-108">DESCRIPTION</span></span>
<span data-ttu-id="a75a3-109">Tüm aygıtların veya Azure IoT Hub 'ındaki bir hedef IoT aygıtının bağlantı dizesini listeler.</span><span class="sxs-lookup"><span data-stu-id="a75a3-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="a75a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a75a3-110">EXAMPLES</span></span>

### <span data-ttu-id="a75a3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a75a3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="a75a3-112">Bir IoT merkezinde tüm cihazlar bağlantı dizelerini gösterin.</span><span class="sxs-lookup"><span data-stu-id="a75a3-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="a75a3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a75a3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="a75a3-114">IoT aygıtının ikincil bağlantı dizesini edinin.</span><span class="sxs-lookup"><span data-stu-id="a75a3-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="a75a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a75a3-115">PARAMETERS</span></span>

### <span data-ttu-id="a75a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75a3-116">-DefaultProfile</span></span>
<span data-ttu-id="a75a3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a75a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a75a3-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="a75a3-118">-DeviceId</span></span>
<span data-ttu-id="a75a3-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="a75a3-119">Target Device Id.</span></span>

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

### <span data-ttu-id="a75a3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a75a3-120">-InputObject</span></span>
<span data-ttu-id="a75a3-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a75a3-121">IotHub object</span></span>

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

### <span data-ttu-id="a75a3-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="a75a3-122">-IotHubName</span></span>
<span data-ttu-id="a75a3-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a75a3-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a75a3-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a75a3-124">-KeyType</span></span>
<span data-ttu-id="a75a3-125">Kimlik doğrulama için paylaşılan erişim ilkesi anahtarı türü.</span><span class="sxs-lookup"><span data-stu-id="a75a3-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a75a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="a75a3-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a75a3-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a75a3-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a75a3-128">-ResourceId</span></span>
<span data-ttu-id="a75a3-129">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a75a3-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a75a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75a3-130">CommonParameters</span></span>
<span data-ttu-id="a75a3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a75a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75a3-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a75a3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75a3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a75a3-133">INPUTS</span></span>

### <span data-ttu-id="a75a3-134">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a75a3-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a75a3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a75a3-135">System.String</span></span>

## <span data-ttu-id="a75a3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a75a3-136">OUTPUTS</span></span>

### <span data-ttu-id="a75a3-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="a75a3-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="a75a3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a75a3-138">NOTES</span></span>

## <span data-ttu-id="a75a3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a75a3-139">RELATED LINKS</span></span>