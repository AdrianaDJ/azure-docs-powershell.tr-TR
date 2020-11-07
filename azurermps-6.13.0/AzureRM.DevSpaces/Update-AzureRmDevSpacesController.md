---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764132"
---
# <span data-ttu-id="bfc2e-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="bfc2e-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="bfc2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc2e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc2e-103">Etiket eklemek için DevSpaces denetleyicisini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfc2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bfc2e-104">SYNTAX</span></span>

### <span data-ttu-id="bfc2e-105">DevSpacesControllerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc2e-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bfc2e-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfc2e-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="bfc2e-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfc2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bfc2e-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc2e-109">Etiket eklemek için DevSpaces denetleyicisini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="bfc2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bfc2e-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc2e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bfc2e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="bfc2e-112">Bir DevSpaces contoller.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="bfc2e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bfc2e-113">PARAMETERS</span></span>

### <span data-ttu-id="bfc2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc2e-114">-DefaultProfile</span></span>
<span data-ttu-id="bfc2e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc2e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfc2e-116">-InputObject</span></span>
<span data-ttu-id="bfc2e-117">Normalde ardışık düzen aracılığıyla iletilen bir PSController nesnesi.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="bfc2e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="bfc2e-118">-Name</span></span>
<span data-ttu-id="bfc2e-119">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="bfc2e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc2e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bfc2e-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bfc2e-121">Resource group name</span></span>

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

### <span data-ttu-id="bfc2e-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bfc2e-122">-ResourceId</span></span>
<span data-ttu-id="bfc2e-123">DevSpaces kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bfc2e-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="bfc2e-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bfc2e-124">-Tag</span></span>
<span data-ttu-id="bfc2e-125">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="bfc2e-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bfc2e-126">-Confirm</span></span>
<span data-ttu-id="bfc2e-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc2e-128">-WhatIf</span></span>
<span data-ttu-id="bfc2e-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc2e-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc2e-131">CommonParameters</span></span>
<span data-ttu-id="bfc2e-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bfc2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc2e-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfc2e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc2e-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bfc2e-134">INPUTS</span></span>

### <span data-ttu-id="bfc2e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc2e-135">System.String</span></span>

### <span data-ttu-id="bfc2e-136">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="bfc2e-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="bfc2e-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfc2e-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bfc2e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bfc2e-138">OUTPUTS</span></span>

### <span data-ttu-id="bfc2e-139">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="bfc2e-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="bfc2e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bfc2e-140">NOTES</span></span>

## <span data-ttu-id="bfc2e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bfc2e-141">RELATED LINKS</span></span>
