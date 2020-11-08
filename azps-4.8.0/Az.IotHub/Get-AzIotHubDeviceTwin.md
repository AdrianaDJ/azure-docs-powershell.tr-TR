---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267446"
---
# <span data-ttu-id="9332a-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="9332a-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="9332a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9332a-102">SYNOPSIS</span></span>
<span data-ttu-id="9332a-103">Bir cihaz ikili alır.</span><span class="sxs-lookup"><span data-stu-id="9332a-103">Gets a device twin.</span></span>

## <span data-ttu-id="9332a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9332a-104">SYNTAX</span></span>

### <span data-ttu-id="9332a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9332a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9332a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9332a-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9332a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9332a-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9332a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9332a-108">DESCRIPTION</span></span>
<span data-ttu-id="9332a-109">Bir cihaz ikili alır.</span><span class="sxs-lookup"><span data-stu-id="9332a-109">Gets a device twin.</span></span> <span data-ttu-id="9332a-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="9332a-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="9332a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9332a-111">EXAMPLES</span></span>

### <span data-ttu-id="9332a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9332a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="9332a-113">İkili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9332a-113">Returns the device twin object.</span></span>

## <span data-ttu-id="9332a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9332a-114">PARAMETERS</span></span>

### <span data-ttu-id="9332a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9332a-115">-DefaultProfile</span></span>
<span data-ttu-id="9332a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9332a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9332a-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="9332a-117">-DeviceId</span></span>
<span data-ttu-id="9332a-118">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="9332a-118">Target Device Id.</span></span>

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

### <span data-ttu-id="9332a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9332a-119">-InputObject</span></span>
<span data-ttu-id="9332a-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="9332a-120">IotHub object</span></span>

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

### <span data-ttu-id="9332a-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="9332a-121">-IotHubName</span></span>
<span data-ttu-id="9332a-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="9332a-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9332a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9332a-123">-ResourceGroupName</span></span>
<span data-ttu-id="9332a-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9332a-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9332a-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9332a-125">-ResourceId</span></span>
<span data-ttu-id="9332a-126">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9332a-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9332a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9332a-127">CommonParameters</span></span>
<span data-ttu-id="9332a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9332a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9332a-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9332a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9332a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9332a-130">INPUTS</span></span>

### <span data-ttu-id="9332a-131">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="9332a-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9332a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9332a-132">System.String</span></span>

## <span data-ttu-id="9332a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9332a-133">OUTPUTS</span></span>

### <span data-ttu-id="9332a-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etwın</span><span class="sxs-lookup"><span data-stu-id="9332a-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="9332a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9332a-135">NOTES</span></span>

## <span data-ttu-id="9332a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9332a-136">RELATED LINKS</span></span>
