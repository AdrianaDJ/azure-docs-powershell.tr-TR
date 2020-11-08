---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107895"
---
# <span data-ttu-id="567db-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="567db-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="567db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="567db-102">SYNOPSIS</span></span>
<span data-ttu-id="567db-103">Bir abonelikten veya bir yönetim grubundan şeması atamasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="567db-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="567db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="567db-104">SYNTAX</span></span>

### <span data-ttu-id="567db-105">BySubscriptionAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="567db-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567db-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="567db-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="567db-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="567db-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="567db-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="567db-108">DESCRIPTION</span></span>
<span data-ttu-id="567db-109">Aboneliğe atanmış bir şeması öğesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="567db-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="567db-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="567db-110">EXAMPLES</span></span>

### <span data-ttu-id="567db-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="567db-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="567db-112">Belirtilen abonelikteki ad ile belirtilen şeması atamasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="567db-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="567db-113">Cmdlet, komutu yürütmeden önce onay isteyecek.</span><span class="sxs-lookup"><span data-stu-id="567db-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="567db-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="567db-114">PARAMETERS</span></span>

### <span data-ttu-id="567db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567db-115">-DefaultProfile</span></span>
<span data-ttu-id="567db-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="567db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="567db-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="567db-117">-InputObject</span></span>
<span data-ttu-id="567db-118">Blueprint atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="567db-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567db-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="567db-119">-ManagementGroupId</span></span>
<span data-ttu-id="567db-120">Blueprint atamasının kaydedildiği yönetim grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="567db-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567db-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="567db-121">-Name</span></span>
<span data-ttu-id="567db-122">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="567db-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="567db-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="567db-123">-PassThru</span></span>
<span data-ttu-id="567db-124">Ayarlandığında, cmdlet kaldırılmış mavi yazdırma atamasını temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="567db-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="567db-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="567db-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="567db-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="567db-126">-SubscriptionId</span></span>
<span data-ttu-id="567db-127">Abonelik kimliği şeması ataması dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="567db-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="567db-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="567db-128">-Confirm</span></span>
<span data-ttu-id="567db-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="567db-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="567db-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="567db-130">-WhatIf</span></span>
<span data-ttu-id="567db-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="567db-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="567db-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="567db-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="567db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567db-133">CommonParameters</span></span>
<span data-ttu-id="567db-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="567db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567db-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="567db-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567db-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="567db-136">INPUTS</span></span>

### <span data-ttu-id="567db-137">System. String</span><span class="sxs-lookup"><span data-stu-id="567db-137">System.String</span></span>

### <span data-ttu-id="567db-138">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="567db-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="567db-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="567db-139">OUTPUTS</span></span>

### <span data-ttu-id="567db-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="567db-140">System.Object</span></span>
## <span data-ttu-id="567db-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="567db-141">NOTES</span></span>

## <span data-ttu-id="567db-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="567db-142">RELATED LINKS</span></span>
