---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: 5422b43019b7b667ba7ea787663e91e2b6beb118
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320354"
---
# <span data-ttu-id="30792-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="30792-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="30792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30792-102">SYNOPSIS</span></span>
<span data-ttu-id="30792-103">Sağlayıcı tarafında müşteri paylaşma abonelikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="30792-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="30792-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30792-104">SYNTAX</span></span>

### <span data-ttu-id="30792-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30792-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30792-106">Byprovidersharesubscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="30792-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30792-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30792-107">DESCRIPTION</span></span>
<span data-ttu-id="30792-108">**Get-AzDataShareProviderSubscription** cmdlet 'i sağlayıcı tarafında tüketici paylaşma abonelikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="30792-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="30792-109">Paylaşım alt öğesi kimliği belirtirseniz, bu cmdlet paylaşım aboneliği hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="30792-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="30792-110">Paylaşım aboneliği kimliğini belirtmezseniz, bu cmdlet, paylaşım ile ilişkili olan tüm tüketici paylaşımı abonelikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="30792-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="30792-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30792-111">EXAMPLES</span></span>

### <span data-ttu-id="30792-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30792-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="30792-113">Bu komut, veri paylaşımı hesap WikiAds 'de paylaşım AdsShare ile ilişkilendirilmiş tüketici paylaşımı aboneliği hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="30792-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="30792-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30792-114">PARAMETERS</span></span>

### <span data-ttu-id="30792-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="30792-115">-AccountName</span></span>
<span data-ttu-id="30792-116">Azure DataShare hesap adı.</span><span class="sxs-lookup"><span data-stu-id="30792-116">Azure DataShare Account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30792-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30792-117">-DefaultProfile</span></span>
<span data-ttu-id="30792-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30792-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30792-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30792-119">-ResourceGroupName</span></span>
<span data-ttu-id="30792-120">Azure DataShare hesabının kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="30792-120">The resource group of the Azure DataShare Account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30792-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="30792-121">-ResourceId</span></span>
<span data-ttu-id="30792-122">Paylaşımın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="30792-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30792-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="30792-123">-ShareName</span></span>
<span data-ttu-id="30792-124">Azure DataShare adı.</span><span class="sxs-lookup"><span data-stu-id="30792-124">Azure DataShare name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30792-125">-Sharesubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="30792-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="30792-126">Tüketici paylaşımı aboneliği kimliği</span><span class="sxs-lookup"><span data-stu-id="30792-126">The id of consumer share subscription</span></span>

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

### <span data-ttu-id="30792-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30792-127">CommonParameters</span></span>
<span data-ttu-id="30792-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30792-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30792-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30792-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30792-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30792-130">INPUTS</span></span>

### <span data-ttu-id="30792-131">System. String</span><span class="sxs-lookup"><span data-stu-id="30792-131">System.String</span></span>

## <span data-ttu-id="30792-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30792-132">OUTPUTS</span></span>

### <span data-ttu-id="30792-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="30792-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="30792-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30792-134">NOTES</span></span>

## <span data-ttu-id="30792-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30792-135">RELATED LINKS</span></span>
