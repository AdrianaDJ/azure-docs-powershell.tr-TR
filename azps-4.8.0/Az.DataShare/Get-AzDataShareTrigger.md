---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareTrigger.md
ms.openlocfilehash: 23554c4de23062fa44a690843232dbc6337e3c9e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109678"
---
# <span data-ttu-id="d21a0-101">Get-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d21a0-101">Get-AzDataShareTrigger</span></span>

## <span data-ttu-id="d21a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d21a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d21a0-103">Paylaşma aboneliğindeki tetik hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d21a0-103">Gets information about a trigger in share subscription.</span></span>

## <span data-ttu-id="d21a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d21a0-104">SYNTAX</span></span>

### <span data-ttu-id="d21a0-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d21a0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d21a0-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d21a0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d21a0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d21a0-107">DESCRIPTION</span></span>
<span data-ttu-id="d21a0-108">**Get-AzDataShareTrigger** cmdlet 'i, veri paylaşımı hesabı altında paylaşım aboneliği tetikleyicisi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d21a0-108">The **Get-AzDataShareTrigger** cmdlet gets information about trigger for share subscription under data share account.</span></span>

## <span data-ttu-id="d21a0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d21a0-109">EXAMPLES</span></span>

### <span data-ttu-id="d21a0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d21a0-110">Example 1</span></span>
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

<span data-ttu-id="d21a0-111">Bu komut, veri paylaşımı hesap WikiAds altında Share aboneliği için Share aboneliği</span><span class="sxs-lookup"><span data-stu-id="d21a0-111">This command gets information about trigger AdsTrigger for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="d21a0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d21a0-112">PARAMETERS</span></span>

### <span data-ttu-id="d21a0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d21a0-113">-AccountName</span></span>
<span data-ttu-id="d21a0-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="d21a0-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d21a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d21a0-115">-DefaultProfile</span></span>
<span data-ttu-id="d21a0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d21a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d21a0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d21a0-117">-Name</span></span>
<span data-ttu-id="d21a0-118">Azure veri paylaşımı tetik adı</span><span class="sxs-lookup"><span data-stu-id="d21a0-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="d21a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d21a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="d21a0-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d21a0-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d21a0-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d21a0-121">-ResourceId</span></span>
<span data-ttu-id="d21a0-122">Tetikleyicinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d21a0-122">The resource id of the trigger</span></span>

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

### <span data-ttu-id="d21a0-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d21a0-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="d21a0-124">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="d21a0-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d21a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d21a0-125">CommonParameters</span></span>
<span data-ttu-id="d21a0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d21a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d21a0-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d21a0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d21a0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d21a0-128">INPUTS</span></span>

### <span data-ttu-id="d21a0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d21a0-129">System.String</span></span>

## <span data-ttu-id="d21a0-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d21a0-130">OUTPUTS</span></span>

### <span data-ttu-id="d21a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="d21a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="d21a0-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d21a0-132">NOTES</span></span>

## <span data-ttu-id="d21a0-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d21a0-133">RELATED LINKS</span></span>
