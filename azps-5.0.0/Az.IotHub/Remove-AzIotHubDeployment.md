---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275329"
---
# <span data-ttu-id="4bcae-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4bcae-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="4bcae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bcae-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcae-103">IoT Edge dağıtımını silme.</span><span class="sxs-lookup"><span data-stu-id="4bcae-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="4bcae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bcae-104">SYNTAX</span></span>

### <span data-ttu-id="4bcae-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bcae-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bcae-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4bcae-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bcae-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4bcae-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bcae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bcae-108">DESCRIPTION</span></span>
<span data-ttu-id="4bcae-109"> https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoringDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="4bcae-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="4bcae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bcae-110">EXAMPLES</span></span>

### <span data-ttu-id="4bcae-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bcae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="4bcae-112">IoT Edge dağıtımını silme.</span><span class="sxs-lookup"><span data-stu-id="4bcae-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="4bcae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bcae-113">PARAMETERS</span></span>

### <span data-ttu-id="4bcae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcae-114">-DefaultProfile</span></span>
<span data-ttu-id="4bcae-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bcae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bcae-116">-InputObject</span></span>
<span data-ttu-id="4bcae-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="4bcae-117">IotHub object</span></span>

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

### <span data-ttu-id="4bcae-118">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="4bcae-118">-IotHubName</span></span>
<span data-ttu-id="4bcae-119">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="4bcae-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4bcae-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bcae-120">-Name</span></span>
<span data-ttu-id="4bcae-121">Dağıtımın tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="4bcae-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="4bcae-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4bcae-122">-PassThru</span></span>
<span data-ttu-id="4bcae-123">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4bcae-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="4bcae-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4bcae-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4bcae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bcae-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bcae-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4bcae-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4bcae-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bcae-127">-ResourceId</span></span>
<span data-ttu-id="4bcae-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4bcae-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4bcae-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bcae-129">-Confirm</span></span>
<span data-ttu-id="4bcae-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bcae-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bcae-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bcae-131">-WhatIf</span></span>
<span data-ttu-id="4bcae-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bcae-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bcae-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bcae-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bcae-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcae-134">CommonParameters</span></span>
<span data-ttu-id="4bcae-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bcae-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcae-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bcae-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcae-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bcae-137">INPUTS</span></span>

### <span data-ttu-id="4bcae-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="4bcae-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4bcae-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4bcae-139">System.String</span></span>

## <span data-ttu-id="4bcae-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bcae-140">OUTPUTS</span></span>

### <span data-ttu-id="4bcae-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4bcae-141">System.Boolean</span></span>

## <span data-ttu-id="4bcae-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bcae-142">NOTES</span></span>

## <span data-ttu-id="4bcae-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bcae-143">RELATED LINKS</span></span>
