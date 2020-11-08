---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280289"
---
# <span data-ttu-id="6ae89-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="6ae89-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="6ae89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ae89-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae89-103">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="6ae89-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ae89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ae89-104">SYNTAX</span></span>

### <span data-ttu-id="6ae89-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ae89-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae89-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="6ae89-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ae89-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="6ae89-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ae89-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ae89-108">DESCRIPTION</span></span>
<span data-ttu-id="6ae89-109">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="6ae89-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ae89-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ae89-110">EXAMPLES</span></span>

### <span data-ttu-id="6ae89-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ae89-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="6ae89-112">Cihazın dağıtılmış izleme ayarlarını alın.</span><span class="sxs-lookup"><span data-stu-id="6ae89-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="6ae89-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ae89-113">PARAMETERS</span></span>

### <span data-ttu-id="6ae89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae89-114">-DefaultProfile</span></span>
<span data-ttu-id="6ae89-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ae89-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ae89-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="6ae89-116">-DeviceId</span></span>
<span data-ttu-id="6ae89-117">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ae89-117">Target Device Id.</span></span>

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

### <span data-ttu-id="6ae89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ae89-118">-InputObject</span></span>
<span data-ttu-id="6ae89-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ae89-119">IotHub object</span></span>

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

### <span data-ttu-id="6ae89-120">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="6ae89-120">-IotHubName</span></span>
<span data-ttu-id="6ae89-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="6ae89-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6ae89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae89-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ae89-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6ae89-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ae89-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ae89-124">-ResourceId</span></span>
<span data-ttu-id="6ae89-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6ae89-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6ae89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae89-126">CommonParameters</span></span>
<span data-ttu-id="6ae89-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ae89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae89-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae89-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae89-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ae89-129">INPUTS</span></span>

### <span data-ttu-id="6ae89-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="6ae89-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6ae89-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae89-131">System.String</span></span>

## <span data-ttu-id="6ae89-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ae89-132">OUTPUTS</span></span>

### <span data-ttu-id="6ae89-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Etyarış</span><span class="sxs-lookup"><span data-stu-id="6ae89-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="6ae89-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ae89-134">NOTES</span></span>

## <span data-ttu-id="6ae89-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ae89-135">RELATED LINKS</span></span>
