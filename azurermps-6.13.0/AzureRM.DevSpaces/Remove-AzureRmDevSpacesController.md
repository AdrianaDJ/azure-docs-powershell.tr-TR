---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764135"
---
# <span data-ttu-id="cd9fd-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="cd9fd-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="cd9fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9fd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9fd-103">DevSpaces denetleyicisini silme.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd9fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd9fd-104">SYNTAX</span></span>

### <span data-ttu-id="cd9fd-105">DevSpacesControllerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cd9fd-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9fd-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cd9fd-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9fd-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="cd9fd-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9fd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd9fd-108">DESCRIPTION</span></span>
<span data-ttu-id="cd9fd-109">DevSpaces denetleyicisini silme.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="cd9fd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd9fd-110">EXAMPLES</span></span>

### <span data-ttu-id="cd9fd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd9fd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="cd9fd-112">DevSpaceControllerName adlı bir DevSpaces denetleyicisini silin.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="cd9fd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd9fd-113">PARAMETERS</span></span>

### <span data-ttu-id="cd9fd-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="cd9fd-114">-AsJob</span></span>
<span data-ttu-id="cd9fd-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cd9fd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9fd-116">-DefaultProfile</span></span>
<span data-ttu-id="cd9fd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9fd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd9fd-118">-InputObject</span></span>
<span data-ttu-id="cd9fd-119">Normalde ardışık düzen aracılığıyla iletilen bir PSController nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cd9fd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd9fd-120">-Name</span></span>
<span data-ttu-id="cd9fd-121">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="cd9fd-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cd9fd-122">-PassThru</span></span>
<span data-ttu-id="cd9fd-123">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="cd9fd-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="cd9fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd9fd-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cd9fd-125">Resource group name</span></span>

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

### <span data-ttu-id="cd9fd-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cd9fd-126">-ResourceId</span></span>
<span data-ttu-id="cd9fd-127">DevSpaces kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="cd9fd-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="cd9fd-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd9fd-128">-Confirm</span></span>
<span data-ttu-id="cd9fd-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9fd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9fd-130">-WhatIf</span></span>
<span data-ttu-id="cd9fd-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9fd-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9fd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9fd-133">CommonParameters</span></span>
<span data-ttu-id="cd9fd-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd9fd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9fd-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd9fd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9fd-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd9fd-136">INPUTS</span></span>

### <span data-ttu-id="cd9fd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9fd-137">System.String</span></span>

### <span data-ttu-id="cd9fd-138">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="cd9fd-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="cd9fd-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd9fd-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cd9fd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd9fd-140">OUTPUTS</span></span>

### <span data-ttu-id="cd9fd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd9fd-141">System.Boolean</span></span>

## <span data-ttu-id="cd9fd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd9fd-142">NOTES</span></span>

## <span data-ttu-id="cd9fd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd9fd-143">RELATED LINKS</span></span>
