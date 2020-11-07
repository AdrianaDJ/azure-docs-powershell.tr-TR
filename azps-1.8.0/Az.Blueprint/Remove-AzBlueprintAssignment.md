---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761434"
---
# <span data-ttu-id="99fa8-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="99fa8-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="99fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="99fa8-103">Bir abonelikten bir şeması kaldırın.</span><span class="sxs-lookup"><span data-stu-id="99fa8-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="99fa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99fa8-104">SYNTAX</span></span>

### <span data-ttu-id="99fa8-105">DeleteBlueprintAssignmentByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="99fa8-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99fa8-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="99fa8-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99fa8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99fa8-107">DESCRIPTION</span></span>
<span data-ttu-id="99fa8-108">Aboneliğe atanmış bir şeması öğesini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="99fa8-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="99fa8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99fa8-109">EXAMPLES</span></span>

### <span data-ttu-id="99fa8-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99fa8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="99fa8-111">Belirtilen abonelikteki ad ile belirtilen şeması atamasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="99fa8-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="99fa8-112">Cmdlet, komutu yürütmeden önce onay isteyecek.</span><span class="sxs-lookup"><span data-stu-id="99fa8-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="99fa8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99fa8-113">PARAMETERS</span></span>

### <span data-ttu-id="99fa8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fa8-114">-DefaultProfile</span></span>
<span data-ttu-id="99fa8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99fa8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99fa8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99fa8-116">-InputObject</span></span>
<span data-ttu-id="99fa8-117">Blueprint atama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="99fa8-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99fa8-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="99fa8-118">-Name</span></span>
<span data-ttu-id="99fa8-119">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="99fa8-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fa8-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="99fa8-120">-PassThru</span></span>
<span data-ttu-id="99fa8-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="99fa8-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="99fa8-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="99fa8-122">-SubscriptionId</span></span>
<span data-ttu-id="99fa8-123">Abonelik kimliği şeması ataması dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="99fa8-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fa8-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="99fa8-124">-Confirm</span></span>
<span data-ttu-id="99fa8-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99fa8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99fa8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99fa8-126">-WhatIf</span></span>
<span data-ttu-id="99fa8-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99fa8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99fa8-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99fa8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99fa8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fa8-129">CommonParameters</span></span>
<span data-ttu-id="99fa8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99fa8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fa8-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fa8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fa8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99fa8-132">INPUTS</span></span>

### <span data-ttu-id="99fa8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="99fa8-133">System.String</span></span>

### <span data-ttu-id="99fa8-134">Microsoft. Azure. Commands. Blueprint. modeller. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="99fa8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="99fa8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99fa8-135">OUTPUTS</span></span>

### <span data-ttu-id="99fa8-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="99fa8-136">System.Object</span></span>
## <span data-ttu-id="99fa8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99fa8-137">NOTES</span></span>

## <span data-ttu-id="99fa8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99fa8-138">RELATED LINKS</span></span>
