---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: a52ae3b59cc7cbf99bf7f4751a36f271bc9610de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759222"
---
# <span data-ttu-id="dd98b-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="dd98b-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="dd98b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd98b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd98b-103">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dd98b-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="dd98b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd98b-104">SYNTAX</span></span>

### <span data-ttu-id="dd98b-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd98b-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd98b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="dd98b-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd98b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd98b-107">DESCRIPTION</span></span>
<span data-ttu-id="dd98b-108">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dd98b-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="dd98b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd98b-109">EXAMPLES</span></span>

### <span data-ttu-id="dd98b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd98b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="dd98b-111">Azure Güvenlik Merkezi fiyatlandırma katmanını "standart" olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="dd98b-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="dd98b-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dd98b-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="dd98b-113">"MyService1" kaynak grubu Azure Güvenlik Merkezi fiyatlandırma katmanını "standart" olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="dd98b-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="dd98b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd98b-114">PARAMETERS</span></span>

### <span data-ttu-id="dd98b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd98b-115">-DefaultProfile</span></span>
<span data-ttu-id="dd98b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd98b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd98b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd98b-117">-InputObject</span></span>
<span data-ttu-id="dd98b-118">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dd98b-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd98b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd98b-119">-Name</span></span>
<span data-ttu-id="dd98b-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="dd98b-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd98b-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="dd98b-121">-PricingTier</span></span>
<span data-ttu-id="dd98b-122">Fiyatlandırma Katmanı.</span><span class="sxs-lookup"><span data-stu-id="dd98b-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd98b-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd98b-123">-Confirm</span></span>
<span data-ttu-id="dd98b-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd98b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd98b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd98b-125">-WhatIf</span></span>
<span data-ttu-id="dd98b-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd98b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd98b-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd98b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd98b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd98b-128">CommonParameters</span></span>
<span data-ttu-id="dd98b-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd98b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd98b-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd98b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd98b-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd98b-131">INPUTS</span></span>

### <span data-ttu-id="dd98b-132">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="dd98b-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="dd98b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd98b-133">OUTPUTS</span></span>

### <span data-ttu-id="dd98b-134">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="dd98b-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="dd98b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd98b-135">NOTES</span></span>

## <span data-ttu-id="dd98b-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd98b-136">RELATED LINKS</span></span>
