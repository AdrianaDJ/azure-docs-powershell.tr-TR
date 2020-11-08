---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279297"
---
# <span data-ttu-id="a8759-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="a8759-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="a8759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8759-102">SYNOPSIS</span></span>
<span data-ttu-id="a8759-103">Yeni diğer ad ve abonelik oluşturur</span><span class="sxs-lookup"><span data-stu-id="a8759-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="a8759-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8759-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8759-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8759-105">DESCRIPTION</span></span>
<span data-ttu-id="a8759-106">**New-AzSubscriptionAlias** cmdlet 'i yeni diğer ad ve abonelik oluşturur</span><span class="sxs-lookup"><span data-stu-id="a8759-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="a8759-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8759-107">EXAMPLES</span></span>

### <span data-ttu-id="a8759-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8759-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="a8759-109">Yeni diğer ad ve abonelik oluşturur</span><span class="sxs-lookup"><span data-stu-id="a8759-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="a8759-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8759-110">PARAMETERS</span></span>

### <span data-ttu-id="a8759-111">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="a8759-111">-AliasName</span></span>
<span data-ttu-id="a8759-112">Abonelik için diğer ad</span><span class="sxs-lookup"><span data-stu-id="a8759-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="a8759-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="a8759-113">-AsJob</span></span>
<span data-ttu-id="a8759-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a8759-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8759-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="a8759-115">-BillingScope</span></span>
<span data-ttu-id="a8759-116">Faturalandırma kapsamı</span><span class="sxs-lookup"><span data-stu-id="a8759-116">Billing Scope</span></span>

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

### <span data-ttu-id="a8759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8759-117">-DefaultProfile</span></span>
<span data-ttu-id="a8759-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8759-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8759-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="a8759-119">-ResellerId</span></span>
<span data-ttu-id="a8759-120">Satıcı kimliği</span><span class="sxs-lookup"><span data-stu-id="a8759-120">Reseller Id</span></span>

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

### <span data-ttu-id="a8759-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a8759-121">-SubscriptionId</span></span>
<span data-ttu-id="a8759-122">Var olan abonelik kimliği</span><span class="sxs-lookup"><span data-stu-id="a8759-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="a8759-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a8759-123">-SubscriptionName</span></span>
<span data-ttu-id="a8759-124">Aboneliğin adı</span><span class="sxs-lookup"><span data-stu-id="a8759-124">Name of the subscription</span></span>

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

### <span data-ttu-id="a8759-125">-İş yükü</span><span class="sxs-lookup"><span data-stu-id="a8759-125">-Workload</span></span>
<span data-ttu-id="a8759-126">Iş yükü türü</span><span class="sxs-lookup"><span data-stu-id="a8759-126">Type of Workload</span></span>

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

### <span data-ttu-id="a8759-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8759-127">-Confirm</span></span>
<span data-ttu-id="a8759-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8759-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8759-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8759-129">-WhatIf</span></span>
<span data-ttu-id="a8759-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8759-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8759-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8759-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8759-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8759-132">CommonParameters</span></span>
<span data-ttu-id="a8759-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8759-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8759-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a8759-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8759-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8759-135">INPUTS</span></span>

### <span data-ttu-id="a8759-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a8759-136">None</span></span>

## <span data-ttu-id="a8759-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8759-137">OUTPUTS</span></span>

### <span data-ttu-id="a8759-138">Microsoft. Azure. Commands. Subscription. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="a8759-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a8759-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8759-139">NOTES</span></span>

## <span data-ttu-id="a8759-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8759-140">RELATED LINKS</span></span>
