---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 4ca33a2bf665923d81257c63f123913af0b8029a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937871"
---
# <span data-ttu-id="e8f05-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e8f05-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e8f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f05-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f05-103">Paylaşım aboneliğindeki eşitleme çalıştırmaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e8f05-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="e8f05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8f05-104">SYNTAX</span></span>

### <span data-ttu-id="e8f05-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8f05-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8f05-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e8f05-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8f05-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8f05-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f05-108">**Get-AzDataShareSubscriptionSynchronization** cmdlet 'i, tüketicinin bir veri paylaşımı hesabı altındaki bir paylaşım aboneliğindeki tüm eşitleme çalışmalarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e8f05-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="e8f05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8f05-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f05-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8f05-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="e8f05-111">Bu komut, veri paylaşımı hesap WikiAds altındaki paylaşım aboneliği Adsshar,</span><span class="sxs-lookup"><span data-stu-id="e8f05-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="e8f05-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8f05-112">PARAMETERS</span></span>

### <span data-ttu-id="e8f05-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8f05-113">-AccountName</span></span>
<span data-ttu-id="e8f05-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="e8f05-114">Azure data share account name</span></span>

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

### <span data-ttu-id="e8f05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f05-115">-DefaultProfile</span></span>
<span data-ttu-id="e8f05-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8f05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f05-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8f05-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e8f05-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="e8f05-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8f05-119">-ResourceId</span></span>
<span data-ttu-id="e8f05-120">Azure veri paylaşımı aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e8f05-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="e8f05-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="e8f05-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="e8f05-122">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="e8f05-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="e8f05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f05-123">CommonParameters</span></span>
<span data-ttu-id="e8f05-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8f05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f05-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f05-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f05-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8f05-126">INPUTS</span></span>

### <span data-ttu-id="e8f05-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f05-127">System.String</span></span>

## <span data-ttu-id="e8f05-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8f05-128">OUTPUTS</span></span>

### <span data-ttu-id="e8f05-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="e8f05-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="e8f05-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8f05-130">NOTES</span></span>

## <span data-ttu-id="e8f05-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8f05-131">RELATED LINKS</span></span>
