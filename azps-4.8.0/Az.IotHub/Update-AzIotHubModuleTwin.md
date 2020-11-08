---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108233"
---
# <span data-ttu-id="a0298-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a0298-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="a0298-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0298-102">SYNOPSIS</span></span>
<span data-ttu-id="a0298-103">IoT cihaz modülü ikili etiket ve istenen özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0298-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="a0298-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0298-104">SYNTAX</span></span>

### <span data-ttu-id="a0298-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0298-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0298-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="a0298-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0298-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a0298-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0298-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0298-108">DESCRIPTION</span></span>
<span data-ttu-id="a0298-109">Bir cihaz ikili.</span><span class="sxs-lookup"><span data-stu-id="a0298-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="a0298-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="a0298-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="a0298-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0298-111">EXAMPLES</span></span>

### <span data-ttu-id="a0298-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0298-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="a0298-113">Güncelleştirilmiş cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0298-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="a0298-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a0298-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="a0298-115">Güncelleştirilmiş özellikleri olan cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0298-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="a0298-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a0298-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="a0298-117">Güncelleştirilmiş Etiketler özelliğine sahip cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0298-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="a0298-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="a0298-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="a0298-119">Değiştirilen cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0298-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="a0298-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0298-120">PARAMETERS</span></span>

### <span data-ttu-id="a0298-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0298-121">-DefaultProfile</span></span>
<span data-ttu-id="a0298-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0298-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0298-123">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="a0298-123">-Desired</span></span>
<span data-ttu-id="a0298-124">İstenen özelliği modül ikili.</span><span class="sxs-lookup"><span data-stu-id="a0298-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="a0298-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="a0298-125">-DeviceId</span></span>
<span data-ttu-id="a0298-126">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="a0298-126">Target Device Id.</span></span>

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

### <span data-ttu-id="a0298-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0298-127">-InputObject</span></span>
<span data-ttu-id="a0298-128">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0298-128">IotHub object</span></span>

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

### <span data-ttu-id="a0298-129">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="a0298-129">-IotHubName</span></span>
<span data-ttu-id="a0298-130">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="a0298-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a0298-131">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="a0298-131">-ModuleId</span></span>
<span data-ttu-id="a0298-132">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="a0298-132">Target Module Id.</span></span>

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

### <span data-ttu-id="a0298-133">-Kısmi</span><span class="sxs-lookup"><span data-stu-id="a0298-133">-Partial</span></span>
<span data-ttu-id="a0298-134">Bir modül ikili etiket ve istenen özelliklerinin yalnızca kısmen güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a0298-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="a0298-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0298-135">-ResourceGroupName</span></span>
<span data-ttu-id="a0298-136">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a0298-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a0298-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0298-137">-ResourceId</span></span>
<span data-ttu-id="a0298-138">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a0298-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a0298-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a0298-139">-Tag</span></span>
<span data-ttu-id="a0298-140">Bir modül ikili etiket özelliğini ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="a0298-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="a0298-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0298-141">-Confirm</span></span>
<span data-ttu-id="a0298-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0298-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0298-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0298-143">-WhatIf</span></span>
<span data-ttu-id="a0298-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0298-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0298-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0298-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0298-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0298-146">CommonParameters</span></span>
<span data-ttu-id="a0298-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0298-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0298-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0298-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0298-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0298-149">INPUTS</span></span>

### <span data-ttu-id="a0298-150">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="a0298-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a0298-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a0298-151">System.String</span></span>

## <span data-ttu-id="a0298-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0298-152">OUTPUTS</span></span>

### <span data-ttu-id="a0298-153">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a0298-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="a0298-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0298-154">NOTES</span></span>

## <span data-ttu-id="a0298-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0298-155">RELATED LINKS</span></span>
