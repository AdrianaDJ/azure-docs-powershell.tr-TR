---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277997"
---
# <span data-ttu-id="80a3a-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="80a3a-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="80a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="80a3a-103">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="80a3a-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="80a3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80a3a-104">SYNTAX</span></span>

### <span data-ttu-id="80a3a-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="80a3a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a3a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="80a3a-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="80a3a-107">DESCRIPTION</span></span>
<span data-ttu-id="80a3a-108">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="80a3a-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="80a3a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80a3a-109">EXAMPLES</span></span>

### <span data-ttu-id="80a3a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="80a3a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="80a3a-111">Azure Güvenlik Merkezi fiyatlandırma katmanını "standart" olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="80a3a-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="80a3a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80a3a-112">PARAMETERS</span></span>

### <span data-ttu-id="80a3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a3a-113">-DefaultProfile</span></span>
<span data-ttu-id="80a3a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80a3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80a3a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80a3a-115">-InputObject</span></span>
<span data-ttu-id="80a3a-116">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="80a3a-116">Input Object.</span></span>

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

### <span data-ttu-id="80a3a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="80a3a-117">-Name</span></span>
<span data-ttu-id="80a3a-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="80a3a-118">Resource name.</span></span>

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

### <span data-ttu-id="80a3a-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="80a3a-119">-PricingTier</span></span>
<span data-ttu-id="80a3a-120">Fiyatlandırma Katmanı.</span><span class="sxs-lookup"><span data-stu-id="80a3a-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="80a3a-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="80a3a-121">-Confirm</span></span>
<span data-ttu-id="80a3a-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="80a3a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a3a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a3a-123">-WhatIf</span></span>
<span data-ttu-id="80a3a-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="80a3a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80a3a-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="80a3a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80a3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a3a-126">CommonParameters</span></span>
<span data-ttu-id="80a3a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80a3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a3a-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="80a3a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a3a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80a3a-129">INPUTS</span></span>

### <span data-ttu-id="80a3a-130">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="80a3a-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="80a3a-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80a3a-131">OUTPUTS</span></span>

### <span data-ttu-id="80a3a-132">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="80a3a-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="80a3a-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80a3a-133">NOTES</span></span>

## <span data-ttu-id="80a3a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80a3a-134">RELATED LINKS</span></span>
