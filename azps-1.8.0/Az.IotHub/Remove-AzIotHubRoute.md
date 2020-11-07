---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 61cbe1ef1fc18ba9c2d6455c6cf56b4f951fdfd7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916407"
---
# <span data-ttu-id="2ec37-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="2ec37-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="2ec37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ec37-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec37-103">IoT Hub 'da yol silme</span><span class="sxs-lookup"><span data-stu-id="2ec37-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="2ec37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ec37-104">SYNTAX</span></span>

### <span data-ttu-id="2ec37-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ec37-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec37-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="2ec37-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec37-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2ec37-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec37-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ec37-108">DESCRIPTION</span></span>
<span data-ttu-id="2ec37-109">Son noktana bir yol silme</span><span class="sxs-lookup"><span data-stu-id="2ec37-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="2ec37-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ec37-110">EXAMPLES</span></span>

### <span data-ttu-id="2ec37-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ec37-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="2ec37-112">"Myiothub" IoT Hub 'ından "R1" rotasını silin.</span><span class="sxs-lookup"><span data-stu-id="2ec37-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="2ec37-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ec37-113">PARAMETERS</span></span>

### <span data-ttu-id="2ec37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec37-114">-DefaultProfile</span></span>
<span data-ttu-id="2ec37-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ec37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ec37-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ec37-116">-InputObject</span></span>
<span data-ttu-id="2ec37-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="2ec37-117">IotHub Object</span></span>

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

### <span data-ttu-id="2ec37-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ec37-118">-Name</span></span>
<span data-ttu-id="2ec37-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="2ec37-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2ec37-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2ec37-120">-PassThru</span></span>
<span data-ttu-id="2ec37-121">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ec37-121">Allows to return the boolean object.</span></span> <span data-ttu-id="2ec37-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="2ec37-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2ec37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec37-123">-ResourceGroupName</span></span>
<span data-ttu-id="2ec37-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2ec37-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ec37-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ec37-125">-ResourceId</span></span>
<span data-ttu-id="2ec37-126">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2ec37-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2ec37-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="2ec37-127">-RouteName</span></span>
<span data-ttu-id="2ec37-128">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="2ec37-128">Name of the Route</span></span>

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

### <span data-ttu-id="2ec37-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ec37-129">-Confirm</span></span>
<span data-ttu-id="2ec37-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ec37-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec37-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec37-131">-WhatIf</span></span>
<span data-ttu-id="2ec37-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ec37-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec37-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ec37-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec37-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec37-134">CommonParameters</span></span>
<span data-ttu-id="2ec37-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ec37-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec37-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec37-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec37-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ec37-137">INPUTS</span></span>

### <span data-ttu-id="2ec37-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="2ec37-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2ec37-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec37-139">System.String</span></span>

## <span data-ttu-id="2ec37-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ec37-140">OUTPUTS</span></span>

### <span data-ttu-id="2ec37-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ec37-141">System.Boolean</span></span>

## <span data-ttu-id="2ec37-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ec37-142">NOTES</span></span>

## <span data-ttu-id="2ec37-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ec37-143">RELATED LINKS</span></span>
