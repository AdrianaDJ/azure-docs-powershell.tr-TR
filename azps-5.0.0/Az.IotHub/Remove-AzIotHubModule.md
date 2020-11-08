---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277734"
---
# <span data-ttu-id="d52f7-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="d52f7-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="d52f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d52f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d52f7-103">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülleri silin.</span><span class="sxs-lookup"><span data-stu-id="d52f7-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d52f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d52f7-104">SYNTAX</span></span>

### <span data-ttu-id="d52f7-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d52f7-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d52f7-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="d52f7-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d52f7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d52f7-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d52f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d52f7-108">DESCRIPTION</span></span>
<span data-ttu-id="d52f7-109">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülleri silin.</span><span class="sxs-lookup"><span data-stu-id="d52f7-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="d52f7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d52f7-110">EXAMPLES</span></span>

### <span data-ttu-id="d52f7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d52f7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="d52f7-112">IoT cihazı modülünü silme.</span><span class="sxs-lookup"><span data-stu-id="d52f7-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="d52f7-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d52f7-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="d52f7-114">Tüm IoT cihaz modüllerini silin.</span><span class="sxs-lookup"><span data-stu-id="d52f7-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="d52f7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d52f7-115">PARAMETERS</span></span>

### <span data-ttu-id="d52f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52f7-116">-DefaultProfile</span></span>
<span data-ttu-id="d52f7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d52f7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d52f7-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="d52f7-118">-DeviceId</span></span>
<span data-ttu-id="d52f7-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="d52f7-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d52f7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d52f7-120">-InputObject</span></span>
<span data-ttu-id="d52f7-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="d52f7-121">IotHub object</span></span>

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

### <span data-ttu-id="d52f7-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="d52f7-122">-IotHubName</span></span>
<span data-ttu-id="d52f7-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="d52f7-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d52f7-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="d52f7-124">-ModuleId</span></span>
<span data-ttu-id="d52f7-125">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="d52f7-125">Target Module Id.</span></span>

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

### <span data-ttu-id="d52f7-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d52f7-126">-PassThru</span></span>
<span data-ttu-id="d52f7-127">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d52f7-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="d52f7-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d52f7-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d52f7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52f7-129">-ResourceGroupName</span></span>
<span data-ttu-id="d52f7-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d52f7-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d52f7-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d52f7-131">-ResourceId</span></span>
<span data-ttu-id="d52f7-132">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d52f7-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d52f7-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="d52f7-133">-Confirm</span></span>
<span data-ttu-id="d52f7-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d52f7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52f7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52f7-135">-WhatIf</span></span>
<span data-ttu-id="d52f7-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d52f7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d52f7-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d52f7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d52f7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52f7-138">CommonParameters</span></span>
<span data-ttu-id="d52f7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d52f7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52f7-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d52f7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52f7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d52f7-141">INPUTS</span></span>

### <span data-ttu-id="d52f7-142">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="d52f7-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d52f7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d52f7-143">System.String</span></span>

## <span data-ttu-id="d52f7-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d52f7-144">OUTPUTS</span></span>

### <span data-ttu-id="d52f7-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d52f7-145">System.Boolean</span></span>

## <span data-ttu-id="d52f7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d52f7-146">NOTES</span></span>

## <span data-ttu-id="d52f7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d52f7-147">RELATED LINKS</span></span>
