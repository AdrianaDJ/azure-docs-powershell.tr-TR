---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubRoute.md
ms.openlocfilehash: 9af711bd449bc8c69808f30dc99ceea806dee00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594028"
---
# <span data-ttu-id="278eb-101">Remove-AzureRmIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="278eb-101">Remove-AzureRmIotHubRoute</span></span>

## <span data-ttu-id="278eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="278eb-102">SYNOPSIS</span></span>
<span data-ttu-id="278eb-103">IoT Hub 'da yol silme</span><span class="sxs-lookup"><span data-stu-id="278eb-103">Delete a route in IoT Hub</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="278eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="278eb-104">SYNTAX</span></span>

### <span data-ttu-id="278eb-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="278eb-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278eb-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="278eb-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="278eb-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="278eb-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="278eb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="278eb-108">DESCRIPTION</span></span>
<span data-ttu-id="278eb-109">Son noktana bir yol silme</span><span class="sxs-lookup"><span data-stu-id="278eb-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="278eb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="278eb-110">EXAMPLES</span></span>

### <span data-ttu-id="278eb-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="278eb-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="278eb-112">"Myiothub" IoT Hub 'ından "R1" rotasını silin.</span><span class="sxs-lookup"><span data-stu-id="278eb-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="278eb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="278eb-113">PARAMETERS</span></span>

### <span data-ttu-id="278eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="278eb-114">-DefaultProfile</span></span>
<span data-ttu-id="278eb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="278eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="278eb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="278eb-116">-InputObject</span></span>
<span data-ttu-id="278eb-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="278eb-117">IotHub Object</span></span>

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

### <span data-ttu-id="278eb-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="278eb-118">-Name</span></span>
<span data-ttu-id="278eb-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="278eb-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="278eb-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="278eb-120">-PassThru</span></span>
<span data-ttu-id="278eb-121">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="278eb-121">Allows to return the boolean object.</span></span> <span data-ttu-id="278eb-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="278eb-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="278eb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="278eb-123">-ResourceGroupName</span></span>
<span data-ttu-id="278eb-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="278eb-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="278eb-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="278eb-125">-ResourceId</span></span>
<span data-ttu-id="278eb-126">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="278eb-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="278eb-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="278eb-127">-RouteName</span></span>
<span data-ttu-id="278eb-128">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="278eb-128">Name of the Route</span></span>

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

### <span data-ttu-id="278eb-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="278eb-129">-Confirm</span></span>
<span data-ttu-id="278eb-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="278eb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="278eb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="278eb-131">-WhatIf</span></span>
<span data-ttu-id="278eb-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="278eb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="278eb-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="278eb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="278eb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="278eb-134">CommonParameters</span></span>
<span data-ttu-id="278eb-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="278eb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="278eb-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="278eb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="278eb-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="278eb-137">INPUTS</span></span>

### <span data-ttu-id="278eb-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="278eb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="278eb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="278eb-139">System.String</span></span>

## <span data-ttu-id="278eb-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="278eb-140">OUTPUTS</span></span>

### <span data-ttu-id="278eb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="278eb-141">System.Boolean</span></span>

## <span data-ttu-id="278eb-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="278eb-142">NOTES</span></span>

## <span data-ttu-id="278eb-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="278eb-143">RELATED LINKS</span></span>
