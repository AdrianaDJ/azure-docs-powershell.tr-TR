---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762244"
---
# <span data-ttu-id="9e9cf-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="9e9cf-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="9e9cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9cf-103">Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="9e9cf-104">Sözleşme şartlarını almak için lütfen Get-AzureRmMarketplaceTerms kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e9cf-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e9cf-105">SYNTAX</span></span>

### <span data-ttu-id="9e9cf-106">AgreementAcceptParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e9cf-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9cf-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9cf-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e9cf-108">Inputobjectacceptparameterset</span><span class="sxs-lookup"><span data-stu-id="9e9cf-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e9cf-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e9cf-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e9cf-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e9cf-110">DESCRIPTION</span></span>
<span data-ttu-id="9e9cf-111">**Set-AzureRmMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar nesnesini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="9e9cf-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e9cf-112">EXAMPLES</span></span>

### <span data-ttu-id="9e9cf-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e9cf-113">Example 1</span></span>
<span data-ttu-id="9e9cf-114">Market yayımcısı sözleşmesini alın</span><span class="sxs-lookup"><span data-stu-id="9e9cf-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="9e9cf-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9e9cf-115">Example 2</span></span>
<span data-ttu-id="9e9cf-116">Yayımcı sözleşmesini ' kabul et ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="9e9cf-117">' Get-AzureRmMarketplaceTerms ' cmdlet 'ini ' terms ' parametresinin değerini alın</span><span class="sxs-lookup"><span data-stu-id="9e9cf-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="9e9cf-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e9cf-118">PARAMETERS</span></span>

### <span data-ttu-id="9e9cf-119">-Kabul et</span><span class="sxs-lookup"><span data-stu-id="9e9cf-119">-Accept</span></span>
<span data-ttu-id="9e9cf-120">Yasal koşulları kabul etmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9cf-121">-DefaultProfile</span></span>
<span data-ttu-id="9e9cf-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e9cf-123">-InputObject</span></span>
<span data-ttu-id="9e9cf-124">Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="9e9cf-125">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e9cf-126">-Name</span></span>
<span data-ttu-id="9e9cf-127">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-128">-Ürün</span><span class="sxs-lookup"><span data-stu-id="9e9cf-128">-Product</span></span>
<span data-ttu-id="9e9cf-129">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9e9cf-130">-Publisher</span></span>
<span data-ttu-id="9e9cf-131">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-132">-Red</span><span class="sxs-lookup"><span data-stu-id="9e9cf-132">-Reject</span></span>
<span data-ttu-id="9e9cf-133">Yasal şartları reddetmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-134">-Terimler</span><span class="sxs-lookup"><span data-stu-id="9e9cf-134">-Terms</span></span>
<span data-ttu-id="9e9cf-135">Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="9e9cf-136">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9cf-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e9cf-137">-Confirm</span></span>
<span data-ttu-id="9e9cf-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e9cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e9cf-139">-WhatIf</span></span>
<span data-ttu-id="9e9cf-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e9cf-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e9cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9cf-142">CommonParameters</span></span>
<span data-ttu-id="9e9cf-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e9cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9cf-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e9cf-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9cf-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e9cf-145">INPUTS</span></span>

### <span data-ttu-id="9e9cf-146">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="9e9cf-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="9e9cf-147">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e9cf-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9e9cf-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e9cf-148">OUTPUTS</span></span>

### <span data-ttu-id="9e9cf-149">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="9e9cf-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="9e9cf-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e9cf-150">NOTES</span></span>

## <span data-ttu-id="9e9cf-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e9cf-151">RELATED LINKS</span></span>
