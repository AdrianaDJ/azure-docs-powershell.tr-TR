---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109042"
---
# <span data-ttu-id="884a1-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="884a1-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="884a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="884a1-102">SYNOPSIS</span></span>
<span data-ttu-id="884a1-103">IoT Hub 'ındaki IoT cihazında bulunan bir IoT cihazı modülü veya liste modüllerinin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="884a1-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="884a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="884a1-104">SYNTAX</span></span>

### <span data-ttu-id="884a1-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="884a1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884a1-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="884a1-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="884a1-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="884a1-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="884a1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="884a1-108">DESCRIPTION</span></span>
<span data-ttu-id="884a1-109">IoT Hub 'ındaki IoT cihazında bulunan bir IoT cihazı modülü veya liste modüllerinin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="884a1-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="884a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="884a1-110">EXAMPLES</span></span>

### <span data-ttu-id="884a1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="884a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="884a1-112">IoT Hub 'ındaki bir IoT cihazı modülünün ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="884a1-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="884a1-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="884a1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="884a1-114">IoT merkezinde bir IoT cihazında bulunan tüm modülleri gösterin.</span><span class="sxs-lookup"><span data-stu-id="884a1-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="884a1-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="884a1-115">PARAMETERS</span></span>

### <span data-ttu-id="884a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884a1-116">-DefaultProfile</span></span>
<span data-ttu-id="884a1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="884a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884a1-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="884a1-118">-DeviceId</span></span>
<span data-ttu-id="884a1-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="884a1-119">Target Device Id.</span></span>

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

### <span data-ttu-id="884a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="884a1-120">-InputObject</span></span>
<span data-ttu-id="884a1-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="884a1-121">IotHub object</span></span>

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

### <span data-ttu-id="884a1-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="884a1-122">-IotHubName</span></span>
<span data-ttu-id="884a1-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="884a1-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="884a1-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="884a1-124">-ModuleId</span></span>
<span data-ttu-id="884a1-125">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="884a1-125">Target Module Id.</span></span>

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

### <span data-ttu-id="884a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="884a1-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="884a1-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="884a1-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="884a1-128">-ResourceId</span></span>
<span data-ttu-id="884a1-129">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="884a1-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="884a1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884a1-130">CommonParameters</span></span>
<span data-ttu-id="884a1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="884a1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884a1-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="884a1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884a1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="884a1-133">INPUTS</span></span>

### <span data-ttu-id="884a1-134">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="884a1-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="884a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="884a1-135">System.String</span></span>

## <span data-ttu-id="884a1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="884a1-136">OUTPUTS</span></span>

### <span data-ttu-id="884a1-137">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModule</span><span class="sxs-lookup"><span data-stu-id="884a1-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="884a1-138">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModules []</span><span class="sxs-lookup"><span data-stu-id="884a1-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="884a1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="884a1-139">NOTES</span></span>

## <span data-ttu-id="884a1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="884a1-140">RELATED LINKS</span></span>
