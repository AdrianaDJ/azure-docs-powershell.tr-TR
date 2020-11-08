---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274515"
---
# <span data-ttu-id="3ce7d-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="3ce7d-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="3ce7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ce7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce7d-103">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="3ce7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ce7d-104">SYNTAX</span></span>

### <span data-ttu-id="3ce7d-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ce7d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce7d-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="3ce7d-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ce7d-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3ce7d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce7d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ce7d-108">DESCRIPTION</span></span>
<span data-ttu-id="3ce7d-109">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="3ce7d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ce7d-110">EXAMPLES</span></span>

### <span data-ttu-id="3ce7d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3ce7d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="3ce7d-112">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="3ce7d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ce7d-113">PARAMETERS</span></span>

### <span data-ttu-id="3ce7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce7d-114">-DefaultProfile</span></span>
<span data-ttu-id="3ce7d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ce7d-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3ce7d-116">-DeviceId</span></span>
<span data-ttu-id="3ce7d-117">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-117">Target Device Id.</span></span>

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

### <span data-ttu-id="3ce7d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ce7d-118">-InputObject</span></span>
<span data-ttu-id="3ce7d-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="3ce7d-119">IotHub object</span></span>

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

### <span data-ttu-id="3ce7d-120">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="3ce7d-120">-IotHubName</span></span>
<span data-ttu-id="3ce7d-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="3ce7d-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3ce7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ce7d-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3ce7d-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3ce7d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3ce7d-124">-ResourceId</span></span>
<span data-ttu-id="3ce7d-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3ce7d-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3ce7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce7d-126">CommonParameters</span></span>
<span data-ttu-id="3ce7d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ce7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce7d-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce7d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce7d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ce7d-129">INPUTS</span></span>

### <span data-ttu-id="3ce7d-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="3ce7d-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3ce7d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3ce7d-131">System.String</span></span>

## <span data-ttu-id="3ce7d-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ce7d-132">OUTPUTS</span></span>

### <span data-ttu-id="3ce7d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etyarış</span><span class="sxs-lookup"><span data-stu-id="3ce7d-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="3ce7d-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ce7d-134">NOTES</span></span>

## <span data-ttu-id="3ce7d-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ce7d-135">RELATED LINKS</span></span>
