---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096989"
---
# <span data-ttu-id="064c5-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="064c5-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="064c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="064c5-102">SYNOPSIS</span></span>
<span data-ttu-id="064c5-103">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülleri silin.</span><span class="sxs-lookup"><span data-stu-id="064c5-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="064c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="064c5-104">SYNTAX</span></span>

### <span data-ttu-id="064c5-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="064c5-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="064c5-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="064c5-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="064c5-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="064c5-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="064c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="064c5-108">DESCRIPTION</span></span>
<span data-ttu-id="064c5-109">Bir IoT Hub 'ındaki hedef IoT aygıtındaki modülleri silin.</span><span class="sxs-lookup"><span data-stu-id="064c5-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="064c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="064c5-110">EXAMPLES</span></span>

### <span data-ttu-id="064c5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="064c5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="064c5-112">IoT cihazı modülünü silme.</span><span class="sxs-lookup"><span data-stu-id="064c5-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="064c5-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="064c5-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="064c5-114">Tüm IoT cihaz modüllerini silin.</span><span class="sxs-lookup"><span data-stu-id="064c5-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="064c5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="064c5-115">PARAMETERS</span></span>

### <span data-ttu-id="064c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064c5-116">-DefaultProfile</span></span>
<span data-ttu-id="064c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="064c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="064c5-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="064c5-118">-DeviceId</span></span>
<span data-ttu-id="064c5-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="064c5-119">Target Device Id.</span></span>

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

### <span data-ttu-id="064c5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="064c5-120">-InputObject</span></span>
<span data-ttu-id="064c5-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="064c5-121">IotHub object</span></span>

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

### <span data-ttu-id="064c5-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="064c5-122">-IotHubName</span></span>
<span data-ttu-id="064c5-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="064c5-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="064c5-124">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="064c5-124">-ModuleId</span></span>
<span data-ttu-id="064c5-125">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="064c5-125">Target Module Id.</span></span>

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

### <span data-ttu-id="064c5-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="064c5-126">-PassThru</span></span>
<span data-ttu-id="064c5-127">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="064c5-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="064c5-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="064c5-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="064c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="064c5-130">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="064c5-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="064c5-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="064c5-131">-ResourceId</span></span>
<span data-ttu-id="064c5-132">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="064c5-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="064c5-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="064c5-133">-Confirm</span></span>
<span data-ttu-id="064c5-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="064c5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="064c5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="064c5-135">-WhatIf</span></span>
<span data-ttu-id="064c5-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="064c5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="064c5-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="064c5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="064c5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064c5-138">CommonParameters</span></span>
<span data-ttu-id="064c5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="064c5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064c5-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="064c5-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064c5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="064c5-141">INPUTS</span></span>

### <span data-ttu-id="064c5-142">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="064c5-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="064c5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="064c5-143">System.String</span></span>

## <span data-ttu-id="064c5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="064c5-144">OUTPUTS</span></span>

### <span data-ttu-id="064c5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="064c5-145">System.Boolean</span></span>

## <span data-ttu-id="064c5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="064c5-146">NOTES</span></span>

## <span data-ttu-id="064c5-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="064c5-147">RELATED LINKS</span></span>
