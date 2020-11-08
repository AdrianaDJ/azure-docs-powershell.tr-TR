---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098473"
---
# <span data-ttu-id="abc15-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="abc15-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="abc15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abc15-102">SYNOPSIS</span></span>
<span data-ttu-id="abc15-103">Bir cihaz ikili alır.</span><span class="sxs-lookup"><span data-stu-id="abc15-103">Gets a device twin.</span></span>

## <span data-ttu-id="abc15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abc15-104">SYNTAX</span></span>

### <span data-ttu-id="abc15-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abc15-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abc15-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="abc15-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abc15-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="abc15-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abc15-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="abc15-108">DESCRIPTION</span></span>
<span data-ttu-id="abc15-109">Bir cihaz ikili alır.</span><span class="sxs-lookup"><span data-stu-id="abc15-109">Gets a device twin.</span></span> <span data-ttu-id="abc15-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="abc15-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="abc15-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abc15-111">EXAMPLES</span></span>

### <span data-ttu-id="abc15-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="abc15-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="abc15-113">İkili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="abc15-113">Returns the device twin object.</span></span>

## <span data-ttu-id="abc15-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abc15-114">PARAMETERS</span></span>

### <span data-ttu-id="abc15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc15-115">-DefaultProfile</span></span>
<span data-ttu-id="abc15-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abc15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc15-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="abc15-117">-DeviceId</span></span>
<span data-ttu-id="abc15-118">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="abc15-118">Target Device Id.</span></span>

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

### <span data-ttu-id="abc15-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abc15-119">-InputObject</span></span>
<span data-ttu-id="abc15-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="abc15-120">IotHub object</span></span>

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

### <span data-ttu-id="abc15-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="abc15-121">-IotHubName</span></span>
<span data-ttu-id="abc15-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="abc15-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="abc15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc15-123">-ResourceGroupName</span></span>
<span data-ttu-id="abc15-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="abc15-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="abc15-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="abc15-125">-ResourceId</span></span>
<span data-ttu-id="abc15-126">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="abc15-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="abc15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc15-127">CommonParameters</span></span>
<span data-ttu-id="abc15-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abc15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc15-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc15-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc15-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abc15-130">INPUTS</span></span>

### <span data-ttu-id="abc15-131">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="abc15-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="abc15-132">System. String</span><span class="sxs-lookup"><span data-stu-id="abc15-132">System.String</span></span>

## <span data-ttu-id="abc15-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abc15-133">OUTPUTS</span></span>

### <span data-ttu-id="abc15-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etwın</span><span class="sxs-lookup"><span data-stu-id="abc15-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="abc15-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abc15-135">NOTES</span></span>

## <span data-ttu-id="abc15-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abc15-136">RELATED LINKS</span></span>
