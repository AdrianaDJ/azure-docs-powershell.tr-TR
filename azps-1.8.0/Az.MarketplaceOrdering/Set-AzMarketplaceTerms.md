---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: 1cea045bd9b663e542bb435003df79f153542a75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915775"
---
# <span data-ttu-id="b8929-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="b8929-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="b8929-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8929-102">SYNOPSIS</span></span>
<span data-ttu-id="b8929-103">Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="b8929-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="b8929-104">Sözleşme şartlarını almak için lütfen Get-AzMarketplaceTerms kullanın.</span><span class="sxs-lookup"><span data-stu-id="b8929-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="b8929-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8929-105">SYNTAX</span></span>

### <span data-ttu-id="b8929-106">AgreementAcceptParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b8929-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8929-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8929-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8929-108">Inputobjectacceptparameterset</span><span class="sxs-lookup"><span data-stu-id="b8929-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8929-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8929-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8929-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8929-110">DESCRIPTION</span></span>
<span data-ttu-id="b8929-111">**Set-AzMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar nesnesini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b8929-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="b8929-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8929-112">EXAMPLES</span></span>

### <span data-ttu-id="b8929-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b8929-113">Example 1</span></span>
<span data-ttu-id="b8929-114">Market yayımcısı sözleşmesini alın</span><span class="sxs-lookup"><span data-stu-id="b8929-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="b8929-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b8929-115">Example 2</span></span>
<span data-ttu-id="b8929-116">Yayımcı sözleşmesini ' kabul et ' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b8929-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="b8929-117">' Get-AzMarketplaceTerms ' cmdlet 'ini ' terms ' parametresinin değerini alın</span><span class="sxs-lookup"><span data-stu-id="b8929-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="b8929-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8929-118">PARAMETERS</span></span>

### <span data-ttu-id="b8929-119">-Kabul et</span><span class="sxs-lookup"><span data-stu-id="b8929-119">-Accept</span></span>
<span data-ttu-id="b8929-120">Yasal koşulları kabul etmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="b8929-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8929-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8929-121">-DefaultProfile</span></span>
<span data-ttu-id="b8929-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8929-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8929-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8929-123">-InputObject</span></span>
<span data-ttu-id="b8929-124">Get-AzMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b8929-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="b8929-125">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="b8929-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8929-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8929-126">-Name</span></span>
<span data-ttu-id="b8929-127">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="b8929-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b8929-128">-Ürün</span><span class="sxs-lookup"><span data-stu-id="b8929-128">-Product</span></span>
<span data-ttu-id="b8929-129">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="b8929-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b8929-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b8929-130">-Publisher</span></span>
<span data-ttu-id="b8929-131">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="b8929-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="b8929-132">-Red</span><span class="sxs-lookup"><span data-stu-id="b8929-132">-Reject</span></span>
<span data-ttu-id="b8929-133">Yasal şartları reddetmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="b8929-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8929-134">-Terimler</span><span class="sxs-lookup"><span data-stu-id="b8929-134">-Terms</span></span>
<span data-ttu-id="b8929-135">Get-AzMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b8929-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="b8929-136">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="b8929-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="b8929-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="b8929-137">-Confirm</span></span>
<span data-ttu-id="b8929-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b8929-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8929-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8929-139">-WhatIf</span></span>
<span data-ttu-id="b8929-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b8929-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8929-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b8929-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8929-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8929-142">CommonParameters</span></span>
<span data-ttu-id="b8929-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b8929-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8929-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8929-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8929-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b8929-145">INPUTS</span></span>

### <span data-ttu-id="b8929-146">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="b8929-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="b8929-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b8929-147">OUTPUTS</span></span>

### <span data-ttu-id="b8929-148">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="b8929-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="b8929-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b8929-149">NOTES</span></span>

## <span data-ttu-id="b8929-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b8929-150">RELATED LINKS</span></span>
