---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274917"
---
# <span data-ttu-id="a691e-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="a691e-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="a691e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a691e-102">SYNOPSIS</span></span>
<span data-ttu-id="a691e-103">Bir IoT Hub 'ı kullanarak SQL gibi güçlü bir dil kullanın.</span><span class="sxs-lookup"><span data-stu-id="a691e-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="a691e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a691e-104">SYNTAX</span></span>

### <span data-ttu-id="a691e-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a691e-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a691e-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a691e-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a691e-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a691e-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a691e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a691e-108">DESCRIPTION</span></span>
<span data-ttu-id="a691e-109">Cihaz ve modül TWINS, işler ve ileti yönlendirme hakkında bilgi almak için, üstün bir SQL gibi güçlü bir dil kullanarak bir IoT Hub 'ı sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="a691e-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="a691e-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languageDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="a691e-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="a691e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a691e-111">EXAMPLES</span></span>

### <span data-ttu-id="a691e-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a691e-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="a691e-113">Bir Azure IoT Hub 'ındaki tüm cihaz ikili verilerini sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="a691e-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="a691e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a691e-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="a691e-115">Hedef aygıttaki verileri ikili.</span><span class="sxs-lookup"><span data-stu-id="a691e-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="a691e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a691e-116">PARAMETERS</span></span>

### <span data-ttu-id="a691e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a691e-117">-DefaultProfile</span></span>
<span data-ttu-id="a691e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a691e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a691e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a691e-119">-InputObject</span></span>
<span data-ttu-id="a691e-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a691e-120">IotHub object</span></span>

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

### <span data-ttu-id="a691e-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="a691e-121">-IotHubName</span></span>
<span data-ttu-id="a691e-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a691e-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a691e-123">-Sorgu</span><span class="sxs-lookup"><span data-stu-id="a691e-123">-Query</span></span>
<span data-ttu-id="a691e-124">Yürütülecek Kullanıcı sorgusu.</span><span class="sxs-lookup"><span data-stu-id="a691e-124">User query to be executed.</span></span>

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

### <span data-ttu-id="a691e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a691e-125">-ResourceGroupName</span></span>
<span data-ttu-id="a691e-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a691e-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a691e-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a691e-127">-ResourceId</span></span>
<span data-ttu-id="a691e-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a691e-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a691e-129">-Üst</span><span class="sxs-lookup"><span data-stu-id="a691e-129">-Top</span></span>
<span data-ttu-id="a691e-130">Döndürülecek en fazla öğe sayısı.</span><span class="sxs-lookup"><span data-stu-id="a691e-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="a691e-131">Varsayılan olarak, sorgunun Cap olmaz.</span><span class="sxs-lookup"><span data-stu-id="a691e-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a691e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="a691e-132">-Confirm</span></span>
<span data-ttu-id="a691e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a691e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a691e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a691e-134">-WhatIf</span></span>
<span data-ttu-id="a691e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a691e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a691e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a691e-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a691e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a691e-137">CommonParameters</span></span>
<span data-ttu-id="a691e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a691e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a691e-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a691e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a691e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a691e-140">INPUTS</span></span>

### <span data-ttu-id="a691e-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a691e-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a691e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a691e-142">System.String</span></span>

## <span data-ttu-id="a691e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a691e-143">OUTPUTS</span></span>

### <span data-ttu-id="a691e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a691e-144">System.String</span></span>

## <span data-ttu-id="a691e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a691e-145">NOTES</span></span>

## <span data-ttu-id="a691e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a691e-146">RELATED LINKS</span></span>
