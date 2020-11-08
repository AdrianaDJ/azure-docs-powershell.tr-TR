---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275429"
---
# <span data-ttu-id="56f18-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="56f18-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="56f18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f18-102">SYNOPSIS</span></span>
<span data-ttu-id="56f18-103">Bir abonelikte işlev uygulamaları planları edinin.</span><span class="sxs-lookup"><span data-stu-id="56f18-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="56f18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56f18-104">SYNTAX</span></span>

### <span data-ttu-id="56f18-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56f18-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56f18-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="56f18-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="56f18-107">ByName</span><span class="sxs-lookup"><span data-stu-id="56f18-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="56f18-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f18-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="56f18-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="56f18-109">DESCRIPTION</span></span>
<span data-ttu-id="56f18-110">Bir abonelikte işlev uygulamaları planları edinin.</span><span class="sxs-lookup"><span data-stu-id="56f18-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="56f18-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56f18-111">EXAMPLES</span></span>

### <span data-ttu-id="56f18-112">Örnek 1: tüm işlev uygulaması planlarını alın.</span><span class="sxs-lookup"><span data-stu-id="56f18-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="56f18-113">Bu komut, tüm işlev uygulaması planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="56f18-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="56f18-114">Örnek 2: kaynak grubu adına göre işlev uygulama planlarını alın.</span><span class="sxs-lookup"><span data-stu-id="56f18-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="56f18-115">Bu komut, kaynak grubu adına göre işlev uygulama planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="56f18-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="56f18-116">Örnek 3: verilen abonelikler için işlev uygulama planları alın.</span><span class="sxs-lookup"><span data-stu-id="56f18-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="56f18-117">Bu komut, verilen abonelikler için işlev uygulama planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="56f18-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="56f18-118">Örnek 4: konuma göre işlev uygulaması planlarını alın.</span><span class="sxs-lookup"><span data-stu-id="56f18-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="56f18-119">Bu komut, App planlarını konuma göre alır.</span><span class="sxs-lookup"><span data-stu-id="56f18-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="56f18-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56f18-120">PARAMETERS</span></span>

### <span data-ttu-id="56f18-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f18-121">-DefaultProfile</span></span>
<span data-ttu-id="56f18-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56f18-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f18-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="56f18-123">-Location</span></span>
<span data-ttu-id="56f18-124">İşlev uygulaması planının konumu.</span><span class="sxs-lookup"><span data-stu-id="56f18-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="56f18-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="56f18-125">-Name</span></span>
<span data-ttu-id="56f18-126">Hizmet planı adı.</span><span class="sxs-lookup"><span data-stu-id="56f18-126">The service plan name.</span></span>

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

### <span data-ttu-id="56f18-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f18-127">-ResourceGroupName</span></span>
<span data-ttu-id="56f18-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="56f18-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="56f18-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="56f18-129">-SubscriptionId</span></span>
<span data-ttu-id="56f18-130">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="56f18-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="56f18-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f18-131">CommonParameters</span></span>
<span data-ttu-id="56f18-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56f18-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f18-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56f18-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f18-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56f18-134">INPUTS</span></span>

## <span data-ttu-id="56f18-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56f18-135">OUTPUTS</span></span>

### <span data-ttu-id="56f18-136">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan</span><span class="sxs-lookup"><span data-stu-id="56f18-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="56f18-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56f18-137">NOTES</span></span>

<span data-ttu-id="56f18-138">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="56f18-138">ALIASES</span></span>

## <span data-ttu-id="56f18-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56f18-139">RELATED LINKS</span></span>

