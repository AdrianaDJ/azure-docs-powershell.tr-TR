---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097161"
---
# <span data-ttu-id="178f3-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="178f3-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="178f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178f3-102">SYNOPSIS</span></span>
<span data-ttu-id="178f3-103">Atanmış alt cihazların virgülle ayrılmış listesini yazdırma.</span><span class="sxs-lookup"><span data-stu-id="178f3-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="178f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="178f3-104">SYNTAX</span></span>

### <span data-ttu-id="178f3-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="178f3-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="178f3-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="178f3-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="178f3-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="178f3-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="178f3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="178f3-108">DESCRIPTION</span></span>
<span data-ttu-id="178f3-109">Tüm kenarsız olmayan cihazları, tüm Edge aygıtların veya belirtilen aygıtın virgülle ayrılmış listesi olarak gösterin.</span><span class="sxs-lookup"><span data-stu-id="178f3-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="178f3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="178f3-110">EXAMPLES</span></span>

### <span data-ttu-id="178f3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="178f3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="178f3-112">Tüm atanmış kenarsız cihazları virgülle ayrılmış liste olarak gösterin.</span><span class="sxs-lookup"><span data-stu-id="178f3-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="178f3-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="178f3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="178f3-114">Tüm kenarsız olmayan cihazları tüm kenar aygıtlarının virgülle ayrılmış listesi olarak gösterin.</span><span class="sxs-lookup"><span data-stu-id="178f3-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="178f3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="178f3-115">PARAMETERS</span></span>

### <span data-ttu-id="178f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178f3-116">-DefaultProfile</span></span>
<span data-ttu-id="178f3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="178f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="178f3-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="178f3-118">-DeviceId</span></span>
<span data-ttu-id="178f3-119">Sınır aygıtının kimliği.</span><span class="sxs-lookup"><span data-stu-id="178f3-119">Id of edge device.</span></span>

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

### <span data-ttu-id="178f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="178f3-120">-InputObject</span></span>
<span data-ttu-id="178f3-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="178f3-121">IotHub object</span></span>

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

### <span data-ttu-id="178f3-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="178f3-122">-IotHubName</span></span>
<span data-ttu-id="178f3-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="178f3-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="178f3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178f3-124">-ResourceGroupName</span></span>
<span data-ttu-id="178f3-125">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="178f3-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="178f3-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="178f3-126">-ResourceId</span></span>
<span data-ttu-id="178f3-127">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="178f3-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="178f3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178f3-128">CommonParameters</span></span>
<span data-ttu-id="178f3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="178f3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178f3-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178f3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178f3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="178f3-131">INPUTS</span></span>

### <span data-ttu-id="178f3-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="178f3-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="178f3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="178f3-133">System.String</span></span>

## <span data-ttu-id="178f3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="178f3-134">OUTPUTS</span></span>

### <span data-ttu-id="178f3-135">Evicei Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="178f3-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="178f3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDçıkarma Eschildren []</span><span class="sxs-lookup"><span data-stu-id="178f3-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="178f3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="178f3-137">NOTES</span></span>

## <span data-ttu-id="178f3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="178f3-138">RELATED LINKS</span></span>
