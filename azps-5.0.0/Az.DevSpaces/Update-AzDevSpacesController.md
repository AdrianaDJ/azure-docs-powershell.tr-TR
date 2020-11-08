---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275560"
---
# <span data-ttu-id="862e3-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="862e3-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="862e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="862e3-102">SYNOPSIS</span></span>
<span data-ttu-id="862e3-103">Etiket eklemek için DevSpaces denetleyicisini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="862e3-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="862e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="862e3-104">SYNTAX</span></span>

### <span data-ttu-id="862e3-105">DevSpacesControllerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="862e3-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862e3-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="862e3-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="862e3-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="862e3-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="862e3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="862e3-108">DESCRIPTION</span></span>
<span data-ttu-id="862e3-109">Etiket eklemek için DevSpaces denetleyicisini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="862e3-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="862e3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="862e3-110">EXAMPLES</span></span>

### <span data-ttu-id="862e3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="862e3-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="862e3-112">Bir DevSpaces denetleyicisini etiketleme.</span><span class="sxs-lookup"><span data-stu-id="862e3-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="862e3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="862e3-113">PARAMETERS</span></span>

### <span data-ttu-id="862e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="862e3-114">-DefaultProfile</span></span>
<span data-ttu-id="862e3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="862e3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="862e3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="862e3-116">-InputObject</span></span>
<span data-ttu-id="862e3-117">Normalde ardışık düzen aracılığıyla iletilen bir PSController nesnesi.</span><span class="sxs-lookup"><span data-stu-id="862e3-117">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="862e3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="862e3-118">-Name</span></span>
<span data-ttu-id="862e3-119">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="862e3-119">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="862e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="862e3-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="862e3-121">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862e3-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="862e3-122">-ResourceId</span></span>
<span data-ttu-id="862e3-123">DevSpaces kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="862e3-123">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="862e3-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="862e3-124">-Tag</span></span>
<span data-ttu-id="862e3-125">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="862e3-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="862e3-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="862e3-126">-Confirm</span></span>
<span data-ttu-id="862e3-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="862e3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="862e3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="862e3-128">-WhatIf</span></span>
<span data-ttu-id="862e3-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="862e3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="862e3-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="862e3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="862e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862e3-131">CommonParameters</span></span>
<span data-ttu-id="862e3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="862e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862e3-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862e3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862e3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="862e3-134">INPUTS</span></span>

### <span data-ttu-id="862e3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="862e3-135">System.String</span></span>

### <span data-ttu-id="862e3-136">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="862e3-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="862e3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="862e3-137">OUTPUTS</span></span>

### <span data-ttu-id="862e3-138">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="862e3-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="862e3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="862e3-139">NOTES</span></span>

## <span data-ttu-id="862e3-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="862e3-140">RELATED LINKS</span></span>
