---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096629"
---
# <span data-ttu-id="3fead-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="3fead-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="3fead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fead-102">SYNOPSIS</span></span>
<span data-ttu-id="3fead-103">Bir cihaz ikili etiket ve istenen özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3fead-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="3fead-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fead-104">SYNTAX</span></span>

### <span data-ttu-id="3fead-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3fead-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fead-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="3fead-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fead-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3fead-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fead-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fead-108">DESCRIPTION</span></span>
<span data-ttu-id="3fead-109">Bir cihaz ikili.</span><span class="sxs-lookup"><span data-stu-id="3fead-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="3fead-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="3fead-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="3fead-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fead-111">EXAMPLES</span></span>

### <span data-ttu-id="3fead-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3fead-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="3fead-113">Güncelleştirilmiş cihaz ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fead-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="3fead-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3fead-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="3fead-115">Güncelleştirilmiş özellikleri olan cihaz ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fead-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="3fead-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3fead-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="3fead-117">Güncelleştirilmiş Etiketler özelliğine sahip cihaz ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fead-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="3fead-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3fead-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="3fead-119">Değiştirilen cihaz ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3fead-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="3fead-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fead-120">PARAMETERS</span></span>

### <span data-ttu-id="3fead-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fead-121">-DefaultProfile</span></span>
<span data-ttu-id="3fead-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fead-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fead-123">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="3fead-123">-Desired</span></span>
<span data-ttu-id="3fead-124">Bir cihaz ikili istenen özelliği ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3fead-124">Add or update the desired property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fead-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3fead-125">-DeviceId</span></span>
<span data-ttu-id="3fead-126">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="3fead-126">Target Device Id.</span></span>

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

### <span data-ttu-id="3fead-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fead-127">-InputObject</span></span>
<span data-ttu-id="3fead-128">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="3fead-128">IotHub object</span></span>

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

### <span data-ttu-id="3fead-129">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="3fead-129">-IotHubName</span></span>
<span data-ttu-id="3fead-130">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="3fead-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3fead-131">-Kısmi</span><span class="sxs-lookup"><span data-stu-id="3fead-131">-Partial</span></span>
<span data-ttu-id="3fead-132">Bir cihaz ikili etiket ve istediğiniz özelliklerinin yalnızca kısmen güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3fead-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fead-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fead-133">-ResourceGroupName</span></span>
<span data-ttu-id="3fead-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3fead-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3fead-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3fead-135">-ResourceId</span></span>
<span data-ttu-id="3fead-136">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3fead-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3fead-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3fead-137">-Tag</span></span>
<span data-ttu-id="3fead-138">Bir cihaz ikili etiket özelliğini ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3fead-138">Add or update the tags property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fead-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="3fead-139">-Confirm</span></span>
<span data-ttu-id="3fead-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3fead-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fead-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fead-141">-WhatIf</span></span>
<span data-ttu-id="3fead-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3fead-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fead-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3fead-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fead-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fead-144">CommonParameters</span></span>
<span data-ttu-id="3fead-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fead-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fead-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fead-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fead-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fead-147">INPUTS</span></span>

### <span data-ttu-id="3fead-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="3fead-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3fead-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3fead-149">System.String</span></span>

## <span data-ttu-id="3fead-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fead-150">OUTPUTS</span></span>

### <span data-ttu-id="3fead-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3fead-151">System.String</span></span>

## <span data-ttu-id="3fead-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fead-152">NOTES</span></span>

## <span data-ttu-id="3fead-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fead-153">RELATED LINKS</span></span>
