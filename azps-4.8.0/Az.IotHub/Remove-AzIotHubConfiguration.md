---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubConfiguration.md
ms.openlocfilehash: 0b87bece7bca0ea3f534746dd20a163f69f21262
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108241"
---
# <span data-ttu-id="2d480-101">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d480-101">Remove-AzIotHubConfiguration</span></span>

## <span data-ttu-id="2d480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d480-102">SYNOPSIS</span></span>
<span data-ttu-id="2d480-103">IoT cihazı yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="2d480-103">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="2d480-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d480-104">SYNTAX</span></span>

### <span data-ttu-id="2d480-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d480-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d480-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2d480-106">InputObjectSet</span></span>
```
Remove-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d480-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2d480-107">ResourceIdSet</span></span>
```
Remove-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d480-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d480-108">DESCRIPTION</span></span>
<span data-ttu-id="2d480-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="2d480-109">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="2d480-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d480-110">EXAMPLES</span></span>

### <span data-ttu-id="2d480-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d480-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="2d480-112">IoT cihazı yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="2d480-112">Delete an IoT device configuration.</span></span>

## <span data-ttu-id="2d480-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d480-113">PARAMETERS</span></span>

### <span data-ttu-id="2d480-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d480-114">-DefaultProfile</span></span>
<span data-ttu-id="2d480-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d480-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d480-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d480-116">-InputObject</span></span>
<span data-ttu-id="2d480-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="2d480-117">IotHub object</span></span>

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

### <span data-ttu-id="2d480-118">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="2d480-118">-IotHubName</span></span>
<span data-ttu-id="2d480-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2d480-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2d480-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d480-120">-Name</span></span>
<span data-ttu-id="2d480-121">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="2d480-121">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="2d480-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2d480-122">-PassThru</span></span>
<span data-ttu-id="2d480-123">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2d480-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="2d480-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2d480-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d480-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d480-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d480-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2d480-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2d480-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2d480-127">-ResourceId</span></span>
<span data-ttu-id="2d480-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2d480-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2d480-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d480-129">-Confirm</span></span>
<span data-ttu-id="2d480-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d480-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d480-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d480-131">-WhatIf</span></span>
<span data-ttu-id="2d480-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d480-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d480-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d480-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d480-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d480-134">CommonParameters</span></span>
<span data-ttu-id="2d480-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d480-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d480-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d480-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d480-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d480-137">INPUTS</span></span>

### <span data-ttu-id="2d480-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="2d480-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2d480-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2d480-139">System.String</span></span>

## <span data-ttu-id="2d480-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d480-140">OUTPUTS</span></span>

### <span data-ttu-id="2d480-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d480-141">System.Boolean</span></span>

## <span data-ttu-id="2d480-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d480-142">NOTES</span></span>

## <span data-ttu-id="2d480-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d480-143">RELATED LINKS</span></span>
