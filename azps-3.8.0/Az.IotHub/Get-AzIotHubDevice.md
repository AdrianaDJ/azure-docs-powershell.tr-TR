---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097375"
---
# <span data-ttu-id="5e540-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="5e540-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="5e540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e540-102">SYNOPSIS</span></span>
<span data-ttu-id="5e540-103">Tüm cihazları veya Azure IoT Hub 'ındaki belirli bir cihazı listeler.</span><span class="sxs-lookup"><span data-stu-id="5e540-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="5e540-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e540-104">SYNTAX</span></span>

### <span data-ttu-id="5e540-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e540-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e540-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="5e540-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e540-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="5e540-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e540-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e540-108">DESCRIPTION</span></span>
<span data-ttu-id="5e540-109">IoT Hub aygıtının ayrıntılarını alın veya bir IoT Hub 'ındaki tüm cihazları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="5e540-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="5e540-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e540-110">EXAMPLES</span></span>

### <span data-ttu-id="5e540-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5e540-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="5e540-112">IoT Hub 'ındaki tüm cihazları gösterin.</span><span class="sxs-lookup"><span data-stu-id="5e540-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="5e540-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5e540-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="5e540-114">IoT Hub cihazının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="5e540-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="5e540-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e540-115">PARAMETERS</span></span>

### <span data-ttu-id="5e540-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e540-116">-DefaultProfile</span></span>
<span data-ttu-id="5e540-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e540-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e540-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="5e540-118">-DeviceId</span></span>
<span data-ttu-id="5e540-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="5e540-119">Target Device Id.</span></span>

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

### <span data-ttu-id="5e540-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e540-120">-InputObject</span></span>
<span data-ttu-id="5e540-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="5e540-121">IotHub object</span></span>

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

### <span data-ttu-id="5e540-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="5e540-122">-IotHubName</span></span>
<span data-ttu-id="5e540-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="5e540-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5e540-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e540-124">-ResourceGroupName</span></span>
<span data-ttu-id="5e540-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5e540-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5e540-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5e540-126">-ResourceId</span></span>
<span data-ttu-id="5e540-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5e540-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5e540-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e540-128">CommonParameters</span></span>
<span data-ttu-id="5e540-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e540-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e540-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e540-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e540-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e540-131">INPUTS</span></span>

### <span data-ttu-id="5e540-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="5e540-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5e540-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5e540-133">System.String</span></span>

## <span data-ttu-id="5e540-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e540-134">OUTPUTS</span></span>

### <span data-ttu-id="5e540-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="5e540-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="5e540-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevıces []</span><span class="sxs-lookup"><span data-stu-id="5e540-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="5e540-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e540-137">NOTES</span></span>

## <span data-ttu-id="5e540-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e540-138">RELATED LINKS</span></span>