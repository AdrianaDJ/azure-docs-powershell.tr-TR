---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 1066c922e24f8a521ac7a52bab437812a7733021
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935820"
---
# <span data-ttu-id="8a800-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="8a800-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="8a800-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a800-102">SYNOPSIS</span></span>
<span data-ttu-id="8a800-103">IoT Hub 'da yol silme</span><span class="sxs-lookup"><span data-stu-id="8a800-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="8a800-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a800-104">SYNTAX</span></span>

### <span data-ttu-id="8a800-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a800-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a800-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="8a800-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a800-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="8a800-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a800-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a800-108">DESCRIPTION</span></span>
<span data-ttu-id="8a800-109">Son noktana bir yol silme</span><span class="sxs-lookup"><span data-stu-id="8a800-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="8a800-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a800-110">EXAMPLES</span></span>

### <span data-ttu-id="8a800-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a800-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="8a800-112">"Myiothub" IoT Hub 'ından "R1" rotasını silin.</span><span class="sxs-lookup"><span data-stu-id="8a800-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="8a800-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a800-113">PARAMETERS</span></span>

### <span data-ttu-id="8a800-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a800-114">-DefaultProfile</span></span>
<span data-ttu-id="8a800-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a800-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a800-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a800-116">-InputObject</span></span>
<span data-ttu-id="8a800-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="8a800-117">IotHub Object</span></span>

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

### <span data-ttu-id="8a800-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a800-118">-Name</span></span>
<span data-ttu-id="8a800-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="8a800-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8a800-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8a800-120">-PassThru</span></span>
<span data-ttu-id="8a800-121">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="8a800-121">Allows to return the boolean object.</span></span> <span data-ttu-id="8a800-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8a800-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8a800-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a800-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a800-124">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8a800-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8a800-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8a800-125">-ResourceId</span></span>
<span data-ttu-id="8a800-126">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8a800-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8a800-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="8a800-127">-RouteName</span></span>
<span data-ttu-id="8a800-128">Rotanın adı</span><span class="sxs-lookup"><span data-stu-id="8a800-128">Name of the Route</span></span>

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

### <span data-ttu-id="8a800-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a800-129">-Confirm</span></span>
<span data-ttu-id="8a800-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a800-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a800-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a800-131">-WhatIf</span></span>
<span data-ttu-id="8a800-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a800-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a800-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a800-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a800-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a800-134">CommonParameters</span></span>
<span data-ttu-id="8a800-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a800-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a800-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a800-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a800-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a800-137">INPUTS</span></span>

### <span data-ttu-id="8a800-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="8a800-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8a800-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8a800-139">System.String</span></span>

## <span data-ttu-id="8a800-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a800-140">OUTPUTS</span></span>

### <span data-ttu-id="8a800-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a800-141">System.Boolean</span></span>

## <span data-ttu-id="8a800-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a800-142">NOTES</span></span>

## <span data-ttu-id="8a800-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a800-143">RELATED LINKS</span></span>
