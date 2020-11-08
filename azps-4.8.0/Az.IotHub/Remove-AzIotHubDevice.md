---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267237"
---
# <span data-ttu-id="0e52c-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="0e52c-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="0e52c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e52c-102">SYNOPSIS</span></span>
<span data-ttu-id="0e52c-103">IoT Hub cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="0e52c-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="0e52c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e52c-104">SYNTAX</span></span>

### <span data-ttu-id="0e52c-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e52c-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e52c-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="0e52c-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e52c-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0e52c-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e52c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e52c-108">DESCRIPTION</span></span>
<span data-ttu-id="0e52c-109">Bir IoT Hub 'ından tüm cihazları veya belirli bir cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="0e52c-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="0e52c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e52c-110">EXAMPLES</span></span>

### <span data-ttu-id="0e52c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e52c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="0e52c-112">Tüm IoT Hub aygıtlarını silin.</span><span class="sxs-lookup"><span data-stu-id="0e52c-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="0e52c-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0e52c-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="0e52c-114">IoT Hub cihazı silme.</span><span class="sxs-lookup"><span data-stu-id="0e52c-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="0e52c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e52c-115">PARAMETERS</span></span>

### <span data-ttu-id="0e52c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e52c-116">-DefaultProfile</span></span>
<span data-ttu-id="0e52c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e52c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e52c-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="0e52c-118">-DeviceId</span></span>
<span data-ttu-id="0e52c-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="0e52c-119">Target Device Id.</span></span>

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

### <span data-ttu-id="0e52c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e52c-120">-InputObject</span></span>
<span data-ttu-id="0e52c-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="0e52c-121">IotHub object</span></span>

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

### <span data-ttu-id="0e52c-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="0e52c-122">-IotHubName</span></span>
<span data-ttu-id="0e52c-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="0e52c-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0e52c-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0e52c-124">-PassThru</span></span>
<span data-ttu-id="0e52c-125">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0e52c-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="0e52c-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0e52c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e52c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e52c-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e52c-128">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0e52c-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e52c-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0e52c-129">-ResourceId</span></span>
<span data-ttu-id="0e52c-130">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0e52c-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0e52c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e52c-131">-Confirm</span></span>
<span data-ttu-id="0e52c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e52c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e52c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e52c-133">-WhatIf</span></span>
<span data-ttu-id="0e52c-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e52c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e52c-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e52c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e52c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e52c-136">CommonParameters</span></span>
<span data-ttu-id="0e52c-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e52c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e52c-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e52c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e52c-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e52c-139">INPUTS</span></span>

### <span data-ttu-id="0e52c-140">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="0e52c-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0e52c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0e52c-141">System.String</span></span>

## <span data-ttu-id="0e52c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e52c-142">OUTPUTS</span></span>

### <span data-ttu-id="0e52c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e52c-143">System.Boolean</span></span>

## <span data-ttu-id="0e52c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e52c-144">NOTES</span></span>

## <span data-ttu-id="0e52c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e52c-145">RELATED LINKS</span></span>
