---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 57b5476e9b797179acdc513cc5fe536ccf4eee69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096389"
---
# <span data-ttu-id="a5058-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="a5058-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="a5058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5058-102">SYNOPSIS</span></span>
<span data-ttu-id="a5058-103">Paylaşma aboneliğindeki tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a5058-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="a5058-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5058-104">SYNTAX</span></span>

### <span data-ttu-id="a5058-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5058-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5058-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a5058-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5058-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5058-107">DESCRIPTION</span></span>
<span data-ttu-id="a5058-108">**Get-AzDataShareTrigger** cmdlet 'i, veri paylaşımı hesabı altında paylaşım aboneliği tetikleyicisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a5058-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="a5058-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5058-109">EXAMPLES</span></span>

### <span data-ttu-id="a5058-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5058-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="a5058-111">Bu komut, veri paylaşımı hesap WikiAds altında Share aboneliği için Share aboneliği</span><span class="sxs-lookup"><span data-stu-id="a5058-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="a5058-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5058-112">PARAMETERS</span></span>

### <span data-ttu-id="a5058-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5058-113">-AccountName</span></span>
<span data-ttu-id="a5058-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="a5058-114">Azure data share account name</span></span>

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

### <span data-ttu-id="a5058-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5058-115">-DefaultProfile</span></span>
<span data-ttu-id="a5058-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5058-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5058-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5058-117">-Name</span></span>
<span data-ttu-id="a5058-118">Azure veri paylaşımı tetik adı</span><span class="sxs-lookup"><span data-stu-id="a5058-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="a5058-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5058-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5058-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a5058-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a5058-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5058-121">-ResourceId</span></span>
<span data-ttu-id="a5058-122">Tetikleyicinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a5058-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="a5058-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a5058-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="a5058-124">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="a5058-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="a5058-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5058-125">CommonParameters</span></span>
<span data-ttu-id="a5058-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5058-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5058-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5058-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5058-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5058-128">INPUTS</span></span>

### <span data-ttu-id="a5058-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a5058-129">System.String</span></span>

## <span data-ttu-id="a5058-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5058-130">OUTPUTS</span></span>

### <span data-ttu-id="a5058-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="a5058-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="a5058-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5058-132">NOTES</span></span>

## <span data-ttu-id="a5058-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5058-133">RELATED LINKS</span></span>
