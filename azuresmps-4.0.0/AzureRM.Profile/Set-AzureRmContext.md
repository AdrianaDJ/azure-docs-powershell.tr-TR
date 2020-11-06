---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571902"
---
# <span data-ttu-id="07616-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="07616-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="07616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07616-102">SYNOPSIS</span></span>
<span data-ttu-id="07616-103">Cmdlet 'lerin geçerli oturumda kullanması için kiracı, abonelik ve ortamı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07616-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="07616-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07616-104">SYNTAX</span></span>

### <span data-ttu-id="07616-105">SubscriptionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07616-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07616-106">Dan</span><span class="sxs-lookup"><span data-stu-id="07616-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07616-107">Olduğunda</span><span class="sxs-lookup"><span data-stu-id="07616-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07616-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="07616-108">DESCRIPTION</span></span>
<span data-ttu-id="07616-109">Set-AzureRmContext cmdlet, geçerli oturumda çalıştırdığınız cmdlet 'lerin kimlik doğrulama bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07616-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="07616-110">Bağlam kiracı, abonelik ve ortam bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="07616-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="07616-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07616-111">EXAMPLES</span></span>

### <span data-ttu-id="07616-112">Örnek 1: abonelik bağlamını ayarlama</span><span class="sxs-lookup"><span data-stu-id="07616-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="07616-113">Bu komut, bağlamı belirtilen aboneliği kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="07616-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="07616-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07616-114">PARAMETERS</span></span>

### <span data-ttu-id="07616-115">-Context</span><span class="sxs-lookup"><span data-stu-id="07616-115">-Context</span></span>
<span data-ttu-id="07616-116">Geçerli oturumun bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07616-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07616-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="07616-117">-SubscriptionId</span></span>
<span data-ttu-id="07616-118">Bu cmdlet 'in geçerli oturum için ayarladığı içeriğin abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="07616-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07616-119">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="07616-119">-SubscriptionName</span></span>
<span data-ttu-id="07616-120">Bu cmdlet 'in geçerli oturum için ayarladığı içeriğin abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07616-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07616-121">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="07616-121">-TenantId</span></span>
<span data-ttu-id="07616-122">Bu cmdlet 'in geçerli oturum için ayarladığı bağlamın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="07616-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07616-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="07616-123">-Confirm</span></span>
<span data-ttu-id="07616-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07616-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07616-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07616-125">-WhatIf</span></span>
<span data-ttu-id="07616-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07616-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07616-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07616-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07616-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07616-128">CommonParameters</span></span>
<span data-ttu-id="07616-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07616-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07616-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07616-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07616-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07616-131">INPUTS</span></span>

## <span data-ttu-id="07616-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07616-132">OUTPUTS</span></span>

### <span data-ttu-id="07616-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="07616-133">PSAzureContext</span></span>

## <span data-ttu-id="07616-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07616-134">NOTES</span></span>

## <span data-ttu-id="07616-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07616-135">RELATED LINKS</span></span>

[<span data-ttu-id="07616-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="07616-136">Get-AzureRMContext</span></span>]()

