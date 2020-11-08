---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097553"
---
# <span data-ttu-id="3cf9b-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3cf9b-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="3cf9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf9b-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf9b-103">IoT cihaz modülü ikili etiket ve istenen özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="3cf9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cf9b-104">SYNTAX</span></span>

### <span data-ttu-id="3cf9b-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3cf9b-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf9b-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="3cf9b-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cf9b-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3cf9b-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf9b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cf9b-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf9b-109">Bir cihaz ikili.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="3cf9b-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="3cf9b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cf9b-111">EXAMPLES</span></span>

### <span data-ttu-id="3cf9b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3cf9b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="3cf9b-113">Güncelleştirilmiş cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="3cf9b-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3cf9b-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="3cf9b-115">Güncelleştirilmiş özellikleri olan cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="3cf9b-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3cf9b-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="3cf9b-117">Güncelleştirilmiş Etiketler özelliğine sahip cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="3cf9b-118">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="3cf9b-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="3cf9b-119">Değiştirilen cihaz modülü ikili nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="3cf9b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cf9b-120">PARAMETERS</span></span>

### <span data-ttu-id="3cf9b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf9b-121">-DefaultProfile</span></span>
<span data-ttu-id="3cf9b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf9b-123">-İstenilen</span><span class="sxs-lookup"><span data-stu-id="3cf9b-123">-Desired</span></span>
<span data-ttu-id="3cf9b-124">İstenen özelliği modül ikili.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="3cf9b-125">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="3cf9b-125">-DeviceId</span></span>
<span data-ttu-id="3cf9b-126">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-126">Target Device Id.</span></span>

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

### <span data-ttu-id="3cf9b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cf9b-127">-InputObject</span></span>
<span data-ttu-id="3cf9b-128">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="3cf9b-128">IotHub object</span></span>

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

### <span data-ttu-id="3cf9b-129">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="3cf9b-129">-IotHubName</span></span>
<span data-ttu-id="3cf9b-130">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="3cf9b-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3cf9b-131">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="3cf9b-131">-ModuleId</span></span>
<span data-ttu-id="3cf9b-132">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-132">Target Module Id.</span></span>

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

### <span data-ttu-id="3cf9b-133">-Kısmi</span><span class="sxs-lookup"><span data-stu-id="3cf9b-133">-Partial</span></span>
<span data-ttu-id="3cf9b-134">Bir modül ikili etiket ve istenen özelliklerinin yalnızca kısmen güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="3cf9b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf9b-135">-ResourceGroupName</span></span>
<span data-ttu-id="3cf9b-136">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3cf9b-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3cf9b-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3cf9b-137">-ResourceId</span></span>
<span data-ttu-id="3cf9b-138">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3cf9b-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3cf9b-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3cf9b-139">-Tag</span></span>
<span data-ttu-id="3cf9b-140">Bir modül ikili etiket özelliğini ekleyin veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="3cf9b-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cf9b-141">-Confirm</span></span>
<span data-ttu-id="3cf9b-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cf9b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf9b-143">-WhatIf</span></span>
<span data-ttu-id="3cf9b-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cf9b-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cf9b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf9b-146">CommonParameters</span></span>
<span data-ttu-id="3cf9b-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cf9b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf9b-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf9b-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf9b-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cf9b-149">INPUTS</span></span>

### <span data-ttu-id="3cf9b-150">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="3cf9b-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3cf9b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf9b-151">System.String</span></span>

## <span data-ttu-id="3cf9b-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cf9b-152">OUTPUTS</span></span>

### <span data-ttu-id="3cf9b-153">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="3cf9b-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="3cf9b-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cf9b-154">NOTES</span></span>

## <span data-ttu-id="3cf9b-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cf9b-155">RELATED LINKS</span></span>
