---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275000"
---
# <span data-ttu-id="2fd30-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="2fd30-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="2fd30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fd30-102">SYNOPSIS</span></span>
<span data-ttu-id="2fd30-103">DevSpaces denetleyicisini silme.</span><span class="sxs-lookup"><span data-stu-id="2fd30-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="2fd30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fd30-104">SYNTAX</span></span>

### <span data-ttu-id="2fd30-105">DevSpacesControllerNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2fd30-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd30-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2fd30-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fd30-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="2fd30-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fd30-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fd30-108">DESCRIPTION</span></span>
<span data-ttu-id="2fd30-109">DevSpaces denetleyicisini silme.</span><span class="sxs-lookup"><span data-stu-id="2fd30-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="2fd30-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fd30-110">EXAMPLES</span></span>

### <span data-ttu-id="2fd30-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2fd30-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="2fd30-112">DevSpaceControllerName adlı bir DevSpaces denetleyicisini silin.</span><span class="sxs-lookup"><span data-stu-id="2fd30-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="2fd30-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fd30-113">PARAMETERS</span></span>

### <span data-ttu-id="2fd30-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="2fd30-114">-AsJob</span></span>
<span data-ttu-id="2fd30-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2fd30-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fd30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fd30-116">-DefaultProfile</span></span>
<span data-ttu-id="2fd30-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fd30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fd30-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fd30-118">-InputObject</span></span>
<span data-ttu-id="2fd30-119">Normalde ardışık düzen aracılığıyla iletilen bir PSController nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2fd30-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="2fd30-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fd30-120">-Name</span></span>
<span data-ttu-id="2fd30-121">DevSpaces denetleyici adı.</span><span class="sxs-lookup"><span data-stu-id="2fd30-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="2fd30-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2fd30-122">-PassThru</span></span>
<span data-ttu-id="2fd30-123">Silme işlemi başarılıysa doğru verir</span><span class="sxs-lookup"><span data-stu-id="2fd30-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="2fd30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fd30-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fd30-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2fd30-125">Resource group name</span></span>

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

### <span data-ttu-id="2fd30-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2fd30-126">-ResourceId</span></span>
<span data-ttu-id="2fd30-127">DevSpaces kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2fd30-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="2fd30-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fd30-128">-Confirm</span></span>
<span data-ttu-id="2fd30-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fd30-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fd30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fd30-130">-WhatIf</span></span>
<span data-ttu-id="2fd30-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fd30-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fd30-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fd30-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fd30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fd30-133">CommonParameters</span></span>
<span data-ttu-id="2fd30-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fd30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fd30-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fd30-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fd30-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fd30-136">INPUTS</span></span>

### <span data-ttu-id="2fd30-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2fd30-137">System.String</span></span>

### <span data-ttu-id="2fd30-138">Microsoft. Azure. Commands. DevSpaces. modeller. PSController</span><span class="sxs-lookup"><span data-stu-id="2fd30-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="2fd30-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fd30-139">OUTPUTS</span></span>

### <span data-ttu-id="2fd30-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fd30-140">System.Boolean</span></span>

## <span data-ttu-id="2fd30-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fd30-141">NOTES</span></span>

## <span data-ttu-id="2fd30-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fd30-142">RELATED LINKS</span></span>
