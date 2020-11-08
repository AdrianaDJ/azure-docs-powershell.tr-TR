---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscription/new-azssubscription
schema: 2.0.0
ms.openlocfilehash: ef8ee9ce81e8ba656a43330ac564c147bcd5d615
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105175"
---
# <span data-ttu-id="b501e-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="b501e-101">New-AzsSubscription</span></span>

## <span data-ttu-id="b501e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b501e-102">SYNOPSIS</span></span>
<span data-ttu-id="b501e-103">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b501e-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="b501e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b501e-104">SYNTAX</span></span>

```
New-AzsSubscription -OfferId <String> [-SubscriptionId <String>] [-DisplayName <String>] [-Id <String>]
 [-State <SubscriptionState>] [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b501e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b501e-105">DESCRIPTION</span></span>
<span data-ttu-id="b501e-106">Abonelik oluşturma veya güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="b501e-106">Create or updates a subscription.</span></span>

## <span data-ttu-id="b501e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b501e-107">EXAMPLES</span></span>

### <span data-ttu-id="b501e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b501e-108">Example 1</span></span>
```powershell
PS C:\> New-AzsSubscription -OfferId '/delegatedProviders/default/offers/testoffer' -DisplayName 'testsubscription' | fl *

DisplayName    : testsubscription
Id             : /subscriptions/7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
OfferId        : /delegatedProviders/default/offers/testoffer
State          : Enabled
SubscriptionId : 7b9d25c5-52ea-4940-8c6a-fe6749ab2e97
TenantId       : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="b501e-109">Abonelik oluşturma.</span><span class="sxs-lookup"><span data-stu-id="b501e-109">Create a subscription.</span></span>

## <span data-ttu-id="b501e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b501e-110">PARAMETERS</span></span>

### <span data-ttu-id="b501e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b501e-111">-DefaultProfile</span></span>
<span data-ttu-id="b501e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b501e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b501e-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b501e-113">-DisplayName</span></span>
<span data-ttu-id="b501e-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="b501e-114">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="b501e-115">-Id</span></span>
<span data-ttu-id="b501e-116">Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="b501e-116">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="b501e-117">-OfferId</span></span>
<span data-ttu-id="b501e-118">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="b501e-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b501e-119">-State</span></span>
<span data-ttu-id="b501e-120">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="b501e-120">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Support.SubscriptionState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b501e-121">-SubscriptionId</span></span>
<span data-ttu-id="b501e-122">Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="b501e-122">Id of the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-123">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="b501e-123">-TenantId</span></span>
<span data-ttu-id="b501e-124">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b501e-124">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b501e-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b501e-125">-Confirm</span></span>
<span data-ttu-id="b501e-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b501e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b501e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b501e-127">-WhatIf</span></span>
<span data-ttu-id="b501e-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b501e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b501e-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b501e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b501e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b501e-130">CommonParameters</span></span>
<span data-ttu-id="b501e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b501e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b501e-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b501e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b501e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b501e-133">INPUTS</span></span>

## <span data-ttu-id="b501e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b501e-134">OUTPUTS</span></span>

### <span data-ttu-id="b501e-135">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. Api20151101. ısubscription</span><span class="sxs-lookup"><span data-stu-id="b501e-135">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.ISubscription</span></span>



## <span data-ttu-id="b501e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b501e-136">NOTES</span></span>

## <span data-ttu-id="b501e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b501e-137">RELATED LINKS</span></span>

