---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268219"
---
# <span data-ttu-id="abf03-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="abf03-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="abf03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abf03-102">SYNOPSIS</span></span>
<span data-ttu-id="abf03-103">IoT cihaz modülü ikili.</span><span class="sxs-lookup"><span data-stu-id="abf03-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="abf03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abf03-104">SYNTAX</span></span>

### <span data-ttu-id="abf03-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="abf03-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf03-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="abf03-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf03-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="abf03-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abf03-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="abf03-108">DESCRIPTION</span></span>
<span data-ttu-id="abf03-109">IoT cihaz modülü ikili.</span><span class="sxs-lookup"><span data-stu-id="abf03-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="abf03-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="abf03-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="abf03-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abf03-111">EXAMPLES</span></span>

### <span data-ttu-id="abf03-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="abf03-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="abf03-113">İkili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="abf03-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="abf03-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abf03-114">PARAMETERS</span></span>

### <span data-ttu-id="abf03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf03-115">-DefaultProfile</span></span>
<span data-ttu-id="abf03-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abf03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf03-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="abf03-117">-DeviceId</span></span>
<span data-ttu-id="abf03-118">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="abf03-118">Target Device Id.</span></span>

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

### <span data-ttu-id="abf03-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abf03-119">-InputObject</span></span>
<span data-ttu-id="abf03-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="abf03-120">IotHub object</span></span>

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

### <span data-ttu-id="abf03-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="abf03-121">-IotHubName</span></span>
<span data-ttu-id="abf03-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="abf03-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="abf03-123">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="abf03-123">-ModuleId</span></span>
<span data-ttu-id="abf03-124">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="abf03-124">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf03-125">-ResourceGroupName</span></span>
<span data-ttu-id="abf03-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="abf03-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="abf03-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="abf03-127">-ResourceId</span></span>
<span data-ttu-id="abf03-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="abf03-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="abf03-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf03-129">CommonParameters</span></span>
<span data-ttu-id="abf03-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abf03-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf03-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf03-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf03-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abf03-132">INPUTS</span></span>

### <span data-ttu-id="abf03-133">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="abf03-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="abf03-134">System. String</span><span class="sxs-lookup"><span data-stu-id="abf03-134">System.String</span></span>

## <span data-ttu-id="abf03-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abf03-135">OUTPUTS</span></span>

### <span data-ttu-id="abf03-136">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="abf03-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="abf03-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abf03-137">NOTES</span></span>

## <span data-ttu-id="abf03-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abf03-138">RELATED LINKS</span></span>
