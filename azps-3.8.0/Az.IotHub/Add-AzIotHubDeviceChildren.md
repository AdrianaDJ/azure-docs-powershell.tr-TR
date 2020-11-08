---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104340"
---
# <span data-ttu-id="6ce40-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="6ce40-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="6ce40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce40-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce40-103">Uç olmayan cihazları, kenar aygıtına alt öğeler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ce40-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="6ce40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ce40-104">SYNTAX</span></span>

### <span data-ttu-id="6ce40-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ce40-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ce40-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="6ce40-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce40-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="6ce40-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce40-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ce40-108">DESCRIPTION</span></span>
<span data-ttu-id="6ce40-109">Uç olmayan aygıt kimliklerinin belirtilen virgülle ayrılmış listesini belirtilen Edge aygıtının alt öğesi olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ce40-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="6ce40-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ce40-110">EXAMPLES</span></span>

### <span data-ttu-id="6ce40-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6ce40-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="6ce40-112">Uç olmayan cihazları, kenar aygıtına alt öğeler olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ce40-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="6ce40-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6ce40-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="6ce40-114">Kenar Çizgili olmayan aygıtları Edge aygıtına alt öğe olarak eklemek için, zaten başka bir Edge aygıtının alt öğesi var.</span><span class="sxs-lookup"><span data-stu-id="6ce40-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="6ce40-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ce40-115">PARAMETERS</span></span>

### <span data-ttu-id="6ce40-116">-Çocuklar</span><span class="sxs-lookup"><span data-stu-id="6ce40-116">-Children</span></span>
<span data-ttu-id="6ce40-117">Alt cihaz listesi (virgülle ayrılmış) yalnızca kenara ait olmayan cihazlar içerir.</span><span class="sxs-lookup"><span data-stu-id="6ce40-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce40-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce40-118">-DefaultProfile</span></span>
<span data-ttu-id="6ce40-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ce40-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce40-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="6ce40-120">-DeviceId</span></span>
<span data-ttu-id="6ce40-121">Sınır aygıtının kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ce40-121">Id of edge device.</span></span>

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

### <span data-ttu-id="6ce40-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6ce40-122">-Force</span></span>
<span data-ttu-id="6ce40-123">Kenar Çizgili olmayan cihazın üst aygıtının üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="6ce40-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="6ce40-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ce40-124">-InputObject</span></span>
<span data-ttu-id="6ce40-125">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ce40-125">IotHub object</span></span>

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

### <span data-ttu-id="6ce40-126">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="6ce40-126">-IotHubName</span></span>
<span data-ttu-id="6ce40-127">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="6ce40-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6ce40-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce40-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ce40-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6ce40-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ce40-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6ce40-130">-ResourceId</span></span>
<span data-ttu-id="6ce40-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6ce40-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6ce40-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ce40-132">-Confirm</span></span>
<span data-ttu-id="6ce40-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ce40-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce40-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce40-134">-WhatIf</span></span>
<span data-ttu-id="6ce40-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ce40-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce40-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ce40-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce40-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce40-137">CommonParameters</span></span>
<span data-ttu-id="6ce40-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ce40-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce40-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce40-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce40-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ce40-140">INPUTS</span></span>

### <span data-ttu-id="6ce40-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="6ce40-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6ce40-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6ce40-142">System.String</span></span>

## <span data-ttu-id="6ce40-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ce40-143">OUTPUTS</span></span>

### <span data-ttu-id="6ce40-144">Evicei Microsoft.Azure.Commands.Management.IotHub.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="6ce40-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="6ce40-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ce40-145">NOTES</span></span>

## <span data-ttu-id="6ce40-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ce40-146">RELATED LINKS</span></span>
