---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753119"
---
# <span data-ttu-id="dd6ef-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="dd6ef-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="dd6ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6ef-103">Bir veya daha fazla şeması yazdırın.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="dd6ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd6ef-104">SYNTAX</span></span>

### <span data-ttu-id="dd6ef-105">BlueprintAssignmentsBySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd6ef-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd6ef-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="dd6ef-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd6ef-107">DESCRIPTION</span></span>
<span data-ttu-id="dd6ef-108">Bir veya daha fazla şeması yazdırın.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="dd6ef-109">Blueprint ödevleri abonelik kapsamında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="dd6ef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd6ef-110">EXAMPLES</span></span>

### <span data-ttu-id="dd6ef-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd6ef-111">Example 1</span></span>
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

<span data-ttu-id="dd6ef-112">Belirtilen abonelikteki şeması atamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="dd6ef-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dd6ef-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="dd6ef-114">Belirtilen abonelikteki belirtilen adda şeması atamasını edinin.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="dd6ef-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd6ef-115">PARAMETERS</span></span>

### <span data-ttu-id="dd6ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6ef-116">-DefaultProfile</span></span>
<span data-ttu-id="dd6ef-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6ef-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd6ef-118">-Name</span></span>
<span data-ttu-id="dd6ef-119">Blueprint atama adı.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6ef-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="dd6ef-120">-SubscriptionId</span></span>
<span data-ttu-id="dd6ef-121">Abonelik kimliği şeması ataması dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd6ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6ef-122">CommonParameters</span></span>
<span data-ttu-id="dd6ef-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd6ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6ef-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd6ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6ef-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd6ef-125">INPUTS</span></span>

### <span data-ttu-id="dd6ef-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dd6ef-126">System.String</span></span>

## <span data-ttu-id="dd6ef-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd6ef-127">OUTPUTS</span></span>

### <span data-ttu-id="dd6ef-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="dd6ef-128">System.Object</span></span>
## <span data-ttu-id="dd6ef-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd6ef-129">NOTES</span></span>

## <span data-ttu-id="dd6ef-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd6ef-130">RELATED LINKS</span></span>
