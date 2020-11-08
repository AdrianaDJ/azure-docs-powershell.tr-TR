---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280248"
---
# <span data-ttu-id="13109-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="13109-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="13109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13109-102">SYNOPSIS</span></span>
<span data-ttu-id="13109-103">Belirtilen cihazın üst aygıtını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="13109-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="13109-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13109-104">SYNTAX</span></span>

### <span data-ttu-id="13109-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13109-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13109-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="13109-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13109-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="13109-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13109-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13109-108">DESCRIPTION</span></span>
<span data-ttu-id="13109-109">Belirtilen uç olmayan cihazın üst aygıtını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="13109-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="13109-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13109-110">EXAMPLES</span></span>

### <span data-ttu-id="13109-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="13109-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="13109-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13109-112">PARAMETERS</span></span>

### <span data-ttu-id="13109-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13109-113">-DefaultProfile</span></span>
<span data-ttu-id="13109-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13109-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13109-115">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="13109-115">-DeviceId</span></span>
<span data-ttu-id="13109-116">Uç olmayan cihazın kimliği.</span><span class="sxs-lookup"><span data-stu-id="13109-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="13109-117">-Force</span><span class="sxs-lookup"><span data-stu-id="13109-117">-Force</span></span>
<span data-ttu-id="13109-118">Kenar Çizgili olmayan cihazın üst aygıtının üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="13109-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="13109-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13109-119">-InputObject</span></span>
<span data-ttu-id="13109-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="13109-120">IotHub object</span></span>

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

### <span data-ttu-id="13109-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="13109-121">-IotHubName</span></span>
<span data-ttu-id="13109-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="13109-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="13109-123">-Parentdeviceıd</span><span class="sxs-lookup"><span data-stu-id="13109-123">-ParentDeviceId</span></span>
<span data-ttu-id="13109-124">Sınır aygıtının kimliği.</span><span class="sxs-lookup"><span data-stu-id="13109-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13109-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13109-125">-ResourceGroupName</span></span>
<span data-ttu-id="13109-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="13109-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="13109-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="13109-127">-ResourceId</span></span>
<span data-ttu-id="13109-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="13109-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="13109-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="13109-129">-Confirm</span></span>
<span data-ttu-id="13109-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13109-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13109-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13109-131">-WhatIf</span></span>
<span data-ttu-id="13109-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="13109-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13109-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="13109-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13109-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13109-134">CommonParameters</span></span>
<span data-ttu-id="13109-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13109-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13109-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13109-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13109-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13109-137">INPUTS</span></span>

### <span data-ttu-id="13109-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="13109-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="13109-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13109-139">System.String</span></span>

## <span data-ttu-id="13109-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13109-140">OUTPUTS</span></span>

### <span data-ttu-id="13109-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevme</span><span class="sxs-lookup"><span data-stu-id="13109-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="13109-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13109-142">NOTES</span></span>

## <span data-ttu-id="13109-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13109-143">RELATED LINKS</span></span>
