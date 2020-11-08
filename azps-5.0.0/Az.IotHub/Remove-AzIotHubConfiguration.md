---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275334"
---
# <span data-ttu-id="5589a-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="5589a-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="5589a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5589a-102">SYNOPSIS</span></span>
<span data-ttu-id="5589a-103">IoT cihazı yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="5589a-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="5589a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5589a-104">SYNTAX</span></span>

### <span data-ttu-id="5589a-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5589a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5589a-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="5589a-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5589a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="5589a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5589a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5589a-108">DESCRIPTION</span></span>
<span data-ttu-id="5589a-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="5589a-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="5589a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5589a-110">EXAMPLES</span></span>

### <span data-ttu-id="5589a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5589a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="5589a-112">IoT cihazı yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="5589a-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="5589a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5589a-113">PARAMETERS</span></span>

### <span data-ttu-id="5589a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5589a-114">-DefaultProfile</span></span>
<span data-ttu-id="5589a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5589a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5589a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5589a-116">-InputObject</span></span>
<span data-ttu-id="5589a-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="5589a-117">IotHub object</span></span>

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

### <span data-ttu-id="5589a-118">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="5589a-118">-IotHubName</span></span>
<span data-ttu-id="5589a-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="5589a-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5589a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5589a-120">-Name</span></span>
<span data-ttu-id="5589a-121">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="5589a-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="5589a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5589a-122">-PassThru</span></span>
<span data-ttu-id="5589a-123">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="5589a-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="5589a-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5589a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5589a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5589a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5589a-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="5589a-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5589a-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5589a-127">-ResourceId</span></span>
<span data-ttu-id="5589a-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="5589a-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5589a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5589a-129">-Confirm</span></span>
<span data-ttu-id="5589a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5589a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5589a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5589a-131">-WhatIf</span></span>
<span data-ttu-id="5589a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5589a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5589a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5589a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5589a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5589a-134">CommonParameters</span></span>
<span data-ttu-id="5589a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5589a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5589a-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5589a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5589a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5589a-137">INPUTS</span></span>

### <span data-ttu-id="5589a-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="5589a-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5589a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5589a-139">System.String</span></span>

## <span data-ttu-id="5589a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5589a-140">OUTPUTS</span></span>

### <span data-ttu-id="5589a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5589a-141">System.Boolean</span></span>

## <span data-ttu-id="5589a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5589a-142">NOTES</span></span>

## <span data-ttu-id="5589a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5589a-143">RELATED LINKS</span></span>
