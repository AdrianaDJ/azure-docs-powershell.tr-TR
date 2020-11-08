---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275019"
---
# <span data-ttu-id="04235-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="04235-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="04235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04235-102">SYNOPSIS</span></span>
<span data-ttu-id="04235-103">Paylaşım aboneliğindeki eşitleme çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="04235-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="04235-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04235-104">SYNTAX</span></span>

### <span data-ttu-id="04235-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04235-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04235-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="04235-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04235-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="04235-107">DESCRIPTION</span></span>
<span data-ttu-id="04235-108">**Get-AzDataShareSubscriptionSynchronization** cmdlet 'i, tüketicinin bir veri paylaşımı hesabı altındaki bir paylaşım aboneliğindeki tüm eşitleme çalışmalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="04235-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="04235-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04235-109">EXAMPLES</span></span>

### <span data-ttu-id="04235-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="04235-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="04235-111">Bu komut, veri paylaşımı hesap WikiAds altındaki paylaşım aboneliği Adsshar,</span><span class="sxs-lookup"><span data-stu-id="04235-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="04235-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04235-112">PARAMETERS</span></span>

### <span data-ttu-id="04235-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04235-113">-AccountName</span></span>
<span data-ttu-id="04235-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="04235-114">Azure data share account name</span></span>

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

### <span data-ttu-id="04235-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04235-115">-DefaultProfile</span></span>
<span data-ttu-id="04235-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04235-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04235-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04235-117">-ResourceGroupName</span></span>
<span data-ttu-id="04235-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="04235-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="04235-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="04235-119">-ResourceId</span></span>
<span data-ttu-id="04235-120">Azure veri paylaşımı aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="04235-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="04235-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="04235-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="04235-122">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="04235-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="04235-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04235-123">CommonParameters</span></span>
<span data-ttu-id="04235-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04235-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04235-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="04235-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04235-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04235-126">INPUTS</span></span>

### <span data-ttu-id="04235-127">System. String</span><span class="sxs-lookup"><span data-stu-id="04235-127">System.String</span></span>

## <span data-ttu-id="04235-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04235-128">OUTPUTS</span></span>

### <span data-ttu-id="04235-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="04235-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="04235-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04235-130">NOTES</span></span>

## <span data-ttu-id="04235-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04235-131">RELATED LINKS</span></span>
