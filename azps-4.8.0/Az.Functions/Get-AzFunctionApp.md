---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268250"
---
# <span data-ttu-id="2e261-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="2e261-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="2e261-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e261-102">SYNOPSIS</span></span>
<span data-ttu-id="2e261-103">Bir abonelikteki işlev uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2e261-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="2e261-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e261-104">SYNTAX</span></span>

### <span data-ttu-id="2e261-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e261-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e261-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="2e261-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e261-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2e261-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2e261-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e261-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2e261-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e261-109">DESCRIPTION</span></span>
<span data-ttu-id="2e261-110">Bir abonelikteki işlev uygulamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="2e261-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="2e261-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e261-111">EXAMPLES</span></span>

### <span data-ttu-id="2e261-112">Örnek 1: tüm işlev uygulamalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="2e261-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="2e261-113">Örnek 2: ada göre işlev uygulamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="2e261-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="2e261-114">Örnek 3: kaynak grubu adına göre işlev uygulamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="2e261-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="2e261-115">Örnek 4: verilen abonelikler için işlev uygulamaları edinin.</span><span class="sxs-lookup"><span data-stu-id="2e261-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="2e261-116">Örnek 5: konuma göre işlev uygulamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="2e261-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="2e261-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e261-117">PARAMETERS</span></span>

### <span data-ttu-id="2e261-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e261-118">-DefaultProfile</span></span>
<span data-ttu-id="2e261-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e261-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e261-120">-Includeslot</span><span class="sxs-lookup"><span data-stu-id="2e261-120">-IncludeSlot</span></span>
<span data-ttu-id="2e261-121">Dağıtım yuvalarını sonuçlarda eklemeyi belirtmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e261-121">Use to specify whether to include deployment slots in results.</span></span>

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

### <span data-ttu-id="2e261-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e261-122">-Location</span></span>
<span data-ttu-id="2e261-123">İşlev uygulamasının konumu.</span><span class="sxs-lookup"><span data-stu-id="2e261-123">The location of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e261-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e261-124">-Name</span></span>
<span data-ttu-id="2e261-125">İşlev uygulamasının adı.</span><span class="sxs-lookup"><span data-stu-id="2e261-125">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e261-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e261-126">-ResourceGroupName</span></span>
<span data-ttu-id="2e261-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2e261-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e261-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2e261-128">-SubscriptionId</span></span>
<span data-ttu-id="2e261-129">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="2e261-129">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e261-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e261-130">CommonParameters</span></span>
<span data-ttu-id="2e261-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e261-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e261-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e261-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e261-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e261-133">INPUTS</span></span>

## <span data-ttu-id="2e261-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e261-134">OUTPUTS</span></span>

### <span data-ttu-id="2e261-135">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="2e261-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="2e261-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e261-136">NOTES</span></span>

<span data-ttu-id="2e261-137">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="2e261-137">ALIASES</span></span>

## <span data-ttu-id="2e261-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e261-138">RELATED LINKS</span></span>

