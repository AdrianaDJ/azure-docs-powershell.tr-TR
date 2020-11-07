---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: ba4fc6a58cd345c149e551263ddf5880f099a54e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937768"
---
# <span data-ttu-id="3a913-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3a913-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="3a913-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a913-102">SYNOPSIS</span></span>
<span data-ttu-id="3a913-103">Veri paylaşımı hesabında paylaşım aboneliği hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="3a913-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="3a913-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a913-104">SYNTAX</span></span>

### <span data-ttu-id="3a913-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a913-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a913-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3a913-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a913-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a913-107">DESCRIPTION</span></span>
<span data-ttu-id="3a913-108">**Get-AzDataShareSubscription** cmdlet 'i, veri paylaşımı hesabında paylaşma aboneliği hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3a913-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="3a913-109">Paylaşım aboneliği adı sağlanmışsa cmdlet, belirli bir paylaşım aboneliği hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="3a913-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="3a913-110">Aksi halde cmdlet, veri paylaşımı hesabında bir abonelik paylaşımı listesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3a913-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="3a913-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a913-111">EXAMPLES</span></span>

### <span data-ttu-id="3a913-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a913-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="3a913-113">Bu komut, veri paylaşımı hesap WikiAds 'de abonelik</span><span class="sxs-lookup"><span data-stu-id="3a913-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="3a913-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a913-114">PARAMETERS</span></span>

### <span data-ttu-id="3a913-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3a913-115">-AccountName</span></span>
<span data-ttu-id="3a913-116">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="3a913-116">Azure data share account name</span></span>

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

### <span data-ttu-id="3a913-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a913-117">-DefaultProfile</span></span>
<span data-ttu-id="3a913-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a913-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a913-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a913-119">-Name</span></span>
<span data-ttu-id="3a913-120">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="3a913-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a913-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a913-121">-ResourceGroupName</span></span>
<span data-ttu-id="3a913-122">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3a913-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="3a913-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a913-123">-ResourceId</span></span>
<span data-ttu-id="3a913-124">Azure veri paylaşımı aboneliğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a913-124">The resource id of the azure data share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a913-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a913-125">CommonParameters</span></span>
<span data-ttu-id="3a913-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a913-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a913-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a913-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a913-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a913-128">INPUTS</span></span>

### <span data-ttu-id="3a913-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3a913-129">System.String</span></span>

## <span data-ttu-id="3a913-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a913-130">OUTPUTS</span></span>

### <span data-ttu-id="3a913-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3a913-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="3a913-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a913-132">NOTES</span></span>

## <span data-ttu-id="3a913-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a913-133">RELATED LINKS</span></span>
