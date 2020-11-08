---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108473"
---
# <span data-ttu-id="b9640-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="b9640-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="b9640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9640-102">SYNOPSIS</span></span>
<span data-ttu-id="b9640-103">Bir veya daha fazla şeması yazdırın.</span><span class="sxs-lookup"><span data-stu-id="b9640-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="b9640-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9640-104">SYNTAX</span></span>

### <span data-ttu-id="b9640-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9640-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9640-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="b9640-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9640-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="b9640-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9640-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="b9640-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9640-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9640-109">DESCRIPTION</span></span>
<span data-ttu-id="b9640-110">Bir veya daha fazla şeması yazdırın.</span><span class="sxs-lookup"><span data-stu-id="b9640-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="b9640-111">Blueprint ödevleri abonelik kapsamında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b9640-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="b9640-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9640-112">EXAMPLES</span></span>

### <span data-ttu-id="b9640-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9640-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="b9640-114">Belirtilen abonelikteki şeması atamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="b9640-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="b9640-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b9640-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="b9640-116">Belirtilen abonelikteki belirtilen adda şeması atamasını edinin.</span><span class="sxs-lookup"><span data-stu-id="b9640-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="b9640-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b9640-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="b9640-118">Belirtilen yönetim grubundaki şeması atamalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="b9640-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="b9640-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="b9640-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="b9640-120">Belirtilen yönetim grubundaki belirtilen adla şeması atamasını edinin.</span><span class="sxs-lookup"><span data-stu-id="b9640-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="b9640-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9640-121">PARAMETERS</span></span>

### <span data-ttu-id="b9640-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9640-122">-DefaultProfile</span></span>
<span data-ttu-id="b9640-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9640-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9640-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b9640-124">-ManagementGroupId</span></span>
<span data-ttu-id="b9640-125">Blueprint atamasının kaydedildiği yönetim grubunun KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b9640-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9640-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9640-126">-Name</span></span>
<span data-ttu-id="b9640-127">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="b9640-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9640-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b9640-128">-SubscriptionId</span></span>
<span data-ttu-id="b9640-129">Abonelik kimliği şeması ataması dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="b9640-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9640-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9640-130">CommonParameters</span></span>
<span data-ttu-id="b9640-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9640-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9640-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b9640-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9640-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9640-133">INPUTS</span></span>

### <span data-ttu-id="b9640-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b9640-134">System.String</span></span>

## <span data-ttu-id="b9640-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9640-135">OUTPUTS</span></span>

### <span data-ttu-id="b9640-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="b9640-136">System.Object</span></span>
## <span data-ttu-id="b9640-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9640-137">NOTES</span></span>

## <span data-ttu-id="b9640-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9640-138">RELATED LINKS</span></span>
