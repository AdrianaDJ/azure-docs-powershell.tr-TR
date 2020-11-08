---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275328"
---
# <span data-ttu-id="87847-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="87847-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="87847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87847-102">SYNOPSIS</span></span>
<span data-ttu-id="87847-103">IoT Hub cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="87847-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="87847-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87847-104">SYNTAX</span></span>

### <span data-ttu-id="87847-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="87847-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87847-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="87847-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87847-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="87847-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87847-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="87847-108">DESCRIPTION</span></span>
<span data-ttu-id="87847-109">Bir IoT Hub 'ından tüm cihazları veya belirli bir cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="87847-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="87847-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87847-110">EXAMPLES</span></span>

### <span data-ttu-id="87847-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="87847-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="87847-112">Tüm IoT Hub aygıtlarını silin.</span><span class="sxs-lookup"><span data-stu-id="87847-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="87847-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="87847-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="87847-114">IoT Hub cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="87847-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="87847-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87847-115">PARAMETERS</span></span>

### <span data-ttu-id="87847-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87847-116">-DefaultProfile</span></span>
<span data-ttu-id="87847-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="87847-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87847-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="87847-118">-DeviceId</span></span>
<span data-ttu-id="87847-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="87847-119">Target Device Id.</span></span>

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

### <span data-ttu-id="87847-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87847-120">-InputObject</span></span>
<span data-ttu-id="87847-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="87847-121">IotHub object</span></span>

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

### <span data-ttu-id="87847-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="87847-122">-IotHubName</span></span>
<span data-ttu-id="87847-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="87847-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="87847-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="87847-124">-PassThru</span></span>
<span data-ttu-id="87847-125">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="87847-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="87847-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="87847-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87847-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87847-127">-ResourceGroupName</span></span>
<span data-ttu-id="87847-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="87847-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="87847-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="87847-129">-ResourceId</span></span>
<span data-ttu-id="87847-130">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="87847-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="87847-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="87847-131">-Confirm</span></span>
<span data-ttu-id="87847-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87847-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87847-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87847-133">-WhatIf</span></span>
<span data-ttu-id="87847-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87847-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87847-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87847-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87847-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87847-136">CommonParameters</span></span>
<span data-ttu-id="87847-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87847-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87847-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87847-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87847-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87847-139">INPUTS</span></span>

### <span data-ttu-id="87847-140">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="87847-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="87847-141">System. String</span><span class="sxs-lookup"><span data-stu-id="87847-141">System.String</span></span>

## <span data-ttu-id="87847-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87847-142">OUTPUTS</span></span>

### <span data-ttu-id="87847-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87847-143">System.Boolean</span></span>

## <span data-ttu-id="87847-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87847-144">NOTES</span></span>

## <span data-ttu-id="87847-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87847-145">RELATED LINKS</span></span>
