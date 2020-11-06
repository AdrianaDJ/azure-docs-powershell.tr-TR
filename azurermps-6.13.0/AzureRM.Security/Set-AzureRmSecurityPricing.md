---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590028"
---
# <span data-ttu-id="dbc82-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="dbc82-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="dbc82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc82-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc82-103">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dbc82-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc82-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbc82-104">SYNTAX</span></span>

### <span data-ttu-id="dbc82-105">SubscriptionLevelResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dbc82-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbc82-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="dbc82-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbc82-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="dbc82-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc82-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbc82-108">DESCRIPTION</span></span>
<span data-ttu-id="dbc82-109">Bir kapsamın Azure Güvenlik Merkezi katmanının fiyatlandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dbc82-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="dbc82-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbc82-110">EXAMPLES</span></span>

### <span data-ttu-id="dbc82-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dbc82-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="dbc82-112">Azure Güvenlik Merkezi fiyatlandırma katmanını "standart" olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="dbc82-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="dbc82-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dbc82-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="dbc82-114">"MyService1" kaynak grubu Azure Güvenlik Merkezi fiyatlandırma katmanını "standart" olarak ayarlar</span><span class="sxs-lookup"><span data-stu-id="dbc82-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="dbc82-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbc82-115">PARAMETERS</span></span>

### <span data-ttu-id="dbc82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc82-116">-DefaultProfile</span></span>
<span data-ttu-id="dbc82-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbc82-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbc82-118">-InputObject</span></span>
<span data-ttu-id="dbc82-119">Giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dbc82-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbc82-120">-Name</span></span>
<span data-ttu-id="dbc82-121">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="dbc82-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="dbc82-122">-PricingTier</span></span>
<span data-ttu-id="dbc82-123">Fiyatlandırma Katmanı.</span><span class="sxs-lookup"><span data-stu-id="dbc82-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc82-124">-ResourceGroupName</span></span>
<span data-ttu-id="dbc82-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dbc82-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbc82-126">-Confirm</span></span>
<span data-ttu-id="dbc82-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbc82-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc82-128">-WhatIf</span></span>
<span data-ttu-id="dbc82-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbc82-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dbc82-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbc82-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbc82-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc82-131">CommonParameters</span></span>
<span data-ttu-id="dbc82-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbc82-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc82-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc82-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc82-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbc82-134">INPUTS</span></span>

### <span data-ttu-id="dbc82-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbc82-135">System.String</span></span>
<span data-ttu-id="dbc82-136">Microsoft. Azure. Commands. Security. cmdlet. pricing. PSAddPricingInputObject</span><span class="sxs-lookup"><span data-stu-id="dbc82-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="dbc82-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbc82-137">OUTPUTS</span></span>

### <span data-ttu-id="dbc82-138">Microsoft. Azure. Commands. Security. model. pricing. Pssecurityprsosu</span><span class="sxs-lookup"><span data-stu-id="dbc82-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="dbc82-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbc82-139">NOTES</span></span>

## <span data-ttu-id="dbc82-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbc82-140">RELATED LINKS</span></span>
