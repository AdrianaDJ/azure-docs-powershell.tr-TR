---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594643"
---
# <span data-ttu-id="19732-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="19732-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="19732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19732-102">SYNOPSIS</span></span>
<span data-ttu-id="19732-103">Verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan kimliği (adı) için koşulları kabul edin veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="19732-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="19732-104">Sözleşme şartlarını almak için lütfen Get-AzureRmMarketplaceTerms kullanın.</span><span class="sxs-lookup"><span data-stu-id="19732-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19732-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19732-105">SYNTAX</span></span>

### <span data-ttu-id="19732-106">AgreementAcceptParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19732-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19732-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19732-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19732-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="19732-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19732-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="19732-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19732-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="19732-110">DESCRIPTION</span></span>
<span data-ttu-id="19732-111">**Set-AzureRmMarketplaceTerms** cmdlet 'i, verilen Yayımcı kimliği (yayımcı), teklif kimliği (ürün) ve plan No (ad) başlığı için şartlar nesnesini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="19732-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="19732-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19732-112">EXAMPLES</span></span>

### <span data-ttu-id="19732-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19732-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="19732-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="19732-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="19732-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19732-115">PARAMETERS</span></span>

### <span data-ttu-id="19732-116">-Kabul et</span><span class="sxs-lookup"><span data-stu-id="19732-116">-Accept</span></span>
<span data-ttu-id="19732-117">Yasal koşulları kabul etmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="19732-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19732-118">-DefaultProfile</span></span>
<span data-ttu-id="19732-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19732-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19732-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19732-120">-InputObject</span></span>
<span data-ttu-id="19732-121">Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19732-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="19732-122">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="19732-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19732-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="19732-123">-Name</span></span>
<span data-ttu-id="19732-124">Dağıtılan resmin tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="19732-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-125">-Ürün</span><span class="sxs-lookup"><span data-stu-id="19732-125">-Product</span></span>
<span data-ttu-id="19732-126">Dağıtılan resmin teklif tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="19732-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="19732-127">-Publisher</span></span>
<span data-ttu-id="19732-128">Dağıtılan resmin yayımcı tanımlayıcı dizesi.</span><span class="sxs-lookup"><span data-stu-id="19732-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-129">-Red</span><span class="sxs-lookup"><span data-stu-id="19732-129">-Reject</span></span>
<span data-ttu-id="19732-130">Yasal şartları reddetmek için bunu iletin.</span><span class="sxs-lookup"><span data-stu-id="19732-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-131">-Terimler</span><span class="sxs-lookup"><span data-stu-id="19732-131">-Terms</span></span>
<span data-ttu-id="19732-132">Get-AzureRmMarketplaceTerms cmdlet 'inde döndürülen terimler nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19732-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="19732-133">Bu, kabul edilen parametre doğru olduğunda zorunlu bir parametredir.</span><span class="sxs-lookup"><span data-stu-id="19732-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19732-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="19732-134">-Confirm</span></span>
<span data-ttu-id="19732-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19732-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19732-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19732-136">-WhatIf</span></span>
<span data-ttu-id="19732-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19732-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19732-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19732-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19732-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19732-139">CommonParameters</span></span>
<span data-ttu-id="19732-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19732-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19732-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19732-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19732-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19732-142">INPUTS</span></span>

### <span data-ttu-id="19732-143">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="19732-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="19732-144">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="19732-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="19732-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19732-145">OUTPUTS</span></span>

### <span data-ttu-id="19732-146">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="19732-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="19732-147">Microsoft. Azure. Commands. Marketplacesıralanıyor. modeller. Psagreemensdems</span><span class="sxs-lookup"><span data-stu-id="19732-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="19732-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19732-148">NOTES</span></span>

## <span data-ttu-id="19732-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19732-149">RELATED LINKS</span></span>

