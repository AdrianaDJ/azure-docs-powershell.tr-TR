---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280286"
---
# <span data-ttu-id="8dabc-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="8dabc-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="8dabc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dabc-102">SYNOPSIS</span></span>
<span data-ttu-id="8dabc-103">IoT Hub 'ındaki IoT cihazında bulunan bir IoT cihazı modülü veya liste modüllerinin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="8dabc-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="8dabc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8dabc-104">SYNTAX</span></span>

### <span data-ttu-id="8dabc-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8dabc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dabc-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="8dabc-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dabc-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="8dabc-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dabc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dabc-108">DESCRIPTION</span></span>
<span data-ttu-id="8dabc-109">IoT Hub 'ındaki IoT cihazında bulunan bir IoT cihazı modülü veya liste modüllerinin ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="8dabc-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="8dabc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8dabc-110">EXAMPLES</span></span>

### <span data-ttu-id="8dabc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8dabc-111">Example 1</span></span>
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

<span data-ttu-id="8dabc-112">IoT Hub 'ındaki bir IoT cihazı modülünün ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="8dabc-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="8dabc-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8dabc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="8dabc-114">IoT merkezinde bir IoT cihazında bulunan tüm modülleri gösterin.</span><span class="sxs-lookup"><span data-stu-id="8dabc-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="8dabc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8dabc-115">PARAMETERS</span></span>

### <span data-ttu-id="8dabc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dabc-116">-DefaultProfile</span></span>
<span data-ttu-id="8dabc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8dabc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dabc-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="8dabc-118">-DeviceId</span></span>
<span data-ttu-id="8dabc-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="8dabc-119">Target Device Id.</span></span>

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

### <span data-ttu-id="8dabc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dabc-120">-InputObject</span></span>
<span data-ttu-id="8dabc-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="8dabc-121">IotHub object</span></span>

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

### <span data-ttu-id="8dabc-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="8dabc-122">-IotHubName</span></span>
<span data-ttu-id="8dabc-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="8dabc-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8dabc-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="8dabc-124">-ModuleId</span></span>
<span data-ttu-id="8dabc-125">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="8dabc-125">Target Module Id.</span></span>

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

### <span data-ttu-id="8dabc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dabc-126">-ResourceGroupName</span></span>
<span data-ttu-id="8dabc-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8dabc-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8dabc-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8dabc-128">-ResourceId</span></span>
<span data-ttu-id="8dabc-129">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8dabc-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8dabc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dabc-130">CommonParameters</span></span>
<span data-ttu-id="8dabc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8dabc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dabc-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dabc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dabc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8dabc-133">INPUTS</span></span>

### <span data-ttu-id="8dabc-134">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="8dabc-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8dabc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8dabc-135">System.String</span></span>

## <span data-ttu-id="8dabc-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8dabc-136">OUTPUTS</span></span>

### <span data-ttu-id="8dabc-137">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModule</span><span class="sxs-lookup"><span data-stu-id="8dabc-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="8dabc-138">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModules []</span><span class="sxs-lookup"><span data-stu-id="8dabc-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="8dabc-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8dabc-139">NOTES</span></span>

## <span data-ttu-id="8dabc-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8dabc-140">RELATED LINKS</span></span>
