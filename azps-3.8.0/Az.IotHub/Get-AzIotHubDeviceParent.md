---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098477"
---
# <span data-ttu-id="7917f-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="7917f-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="7917f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7917f-102">SYNOPSIS</span></span>
<span data-ttu-id="7917f-103">Belirtilen cihazın üst aygıtını edinin.</span><span class="sxs-lookup"><span data-stu-id="7917f-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="7917f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7917f-104">SYNTAX</span></span>

### <span data-ttu-id="7917f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7917f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7917f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="7917f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7917f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7917f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7917f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7917f-108">DESCRIPTION</span></span>
<span data-ttu-id="7917f-109">Belirtilen uç olmayan cihazın üst aygıtını edinin.</span><span class="sxs-lookup"><span data-stu-id="7917f-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7917f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7917f-110">EXAMPLES</span></span>

### <span data-ttu-id="7917f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7917f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="7917f-112">Belirtilen uç olmayan cihazın üst aygıtını edinin.</span><span class="sxs-lookup"><span data-stu-id="7917f-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="7917f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7917f-113">PARAMETERS</span></span>

### <span data-ttu-id="7917f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7917f-114">-DefaultProfile</span></span>
<span data-ttu-id="7917f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7917f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7917f-116">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="7917f-116">-DeviceId</span></span>
<span data-ttu-id="7917f-117">Uç olmayan cihazın kimliği.</span><span class="sxs-lookup"><span data-stu-id="7917f-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="7917f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7917f-118">-InputObject</span></span>
<span data-ttu-id="7917f-119">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="7917f-119">IotHub object</span></span>

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

### <span data-ttu-id="7917f-120">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="7917f-120">-IotHubName</span></span>
<span data-ttu-id="7917f-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="7917f-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7917f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7917f-122">-ResourceGroupName</span></span>
<span data-ttu-id="7917f-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7917f-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7917f-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7917f-124">-ResourceId</span></span>
<span data-ttu-id="7917f-125">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7917f-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7917f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7917f-126">CommonParameters</span></span>
<span data-ttu-id="7917f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7917f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7917f-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7917f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7917f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7917f-129">INPUTS</span></span>

### <span data-ttu-id="7917f-130">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="7917f-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7917f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7917f-131">System.String</span></span>

## <span data-ttu-id="7917f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7917f-132">OUTPUTS</span></span>

### <span data-ttu-id="7917f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="7917f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="7917f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7917f-134">NOTES</span></span>

## <span data-ttu-id="7917f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7917f-135">RELATED LINKS</span></span>
