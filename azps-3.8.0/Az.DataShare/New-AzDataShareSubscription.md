---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 01cff184a2db4364536d4088103380f3f28b47a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097307"
---
# <span data-ttu-id="74dec-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="74dec-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="74dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74dec-102">SYNOPSIS</span></span>
<span data-ttu-id="74dec-103">Yeni bir paylaşım aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74dec-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="74dec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74dec-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74dec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74dec-105">DESCRIPTION</span></span>
<span data-ttu-id="74dec-106">**Yeni-Azverisharesubscription** cmdlet 'i, belirtilen veri paylaşımı hesabında ve davet kimliğinde bir paylaşım aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74dec-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="74dec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74dec-107">EXAMPLES</span></span>

### <span data-ttu-id="74dec-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74dec-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="74dec-109">Bu komut, veri paylaşımı hesap WikiAds altındaki Davetionid için yeni bir paylaşım aboneliği Adssharesubscripın oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74dec-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="74dec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74dec-110">PARAMETERS</span></span>

### <span data-ttu-id="74dec-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="74dec-111">-AccountName</span></span>
<span data-ttu-id="74dec-112">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="74dec-112">Azure data share account name</span></span>

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

### <span data-ttu-id="74dec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74dec-113">-DefaultProfile</span></span>
<span data-ttu-id="74dec-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74dec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74dec-115">-Davetsiz</span><span class="sxs-lookup"><span data-stu-id="74dec-115">-InvitationId</span></span>
<span data-ttu-id="74dec-116">Azure veri paylaşımı Davetikodu</span><span class="sxs-lookup"><span data-stu-id="74dec-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="74dec-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="74dec-117">-Name</span></span>
<span data-ttu-id="74dec-118">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="74dec-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="74dec-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74dec-119">-ResourceGroupName</span></span>
<span data-ttu-id="74dec-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="74dec-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="74dec-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="74dec-121">-Confirm</span></span>
<span data-ttu-id="74dec-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74dec-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74dec-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74dec-123">-WhatIf</span></span>
<span data-ttu-id="74dec-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74dec-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74dec-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74dec-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74dec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74dec-126">CommonParameters</span></span>
<span data-ttu-id="74dec-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74dec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74dec-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74dec-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74dec-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74dec-129">INPUTS</span></span>

### <span data-ttu-id="74dec-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="74dec-130">None</span></span>

## <span data-ttu-id="74dec-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74dec-131">OUTPUTS</span></span>

### <span data-ttu-id="74dec-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="74dec-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="74dec-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74dec-133">NOTES</span></span>

## <span data-ttu-id="74dec-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74dec-134">RELATED LINKS</span></span>