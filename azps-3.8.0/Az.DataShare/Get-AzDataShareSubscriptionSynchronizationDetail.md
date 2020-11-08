---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: ffa9de86a7ebbb70361752b8c7733129eb024845
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937870"
---
# <span data-ttu-id="4a7b2-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="4a7b2-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="4a7b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a7b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4a7b2-103">Paylaşma aboneliğinin ayrıntılarını eşitleme hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4a7b2-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="4a7b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a7b2-104">SYNTAX</span></span>

### <span data-ttu-id="4a7b2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a7b2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a7b2-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4a7b2-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a7b2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a7b2-107">DESCRIPTION</span></span>
<span data-ttu-id="4a7b2-108">**Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet 'i, bir paylaşım aboneliği için başlatılan eşitlemenin ayrıntılarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4a7b2-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="4a7b2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a7b2-109">EXAMPLES</span></span>

### <span data-ttu-id="4a7b2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a7b2-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="4a7b2-111">Bu komut, veri paylaşımı hesap WikiAds altında paylaşım aboneliği Adssharesubscripın altında başlatılan eşitleme hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4a7b2-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="4a7b2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a7b2-112">PARAMETERS</span></span>

### <span data-ttu-id="4a7b2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a7b2-113">-AccountName</span></span>
<span data-ttu-id="4a7b2-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="4a7b2-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4a7b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a7b2-115">-DefaultProfile</span></span>
<span data-ttu-id="4a7b2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a7b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a7b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a7b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="4a7b2-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4a7b2-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4a7b2-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4a7b2-119">-ResourceId</span></span>
<span data-ttu-id="4a7b2-120">Azure veri paylaşımı aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4a7b2-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="4a7b2-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4a7b2-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="4a7b2-122">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="4a7b2-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4a7b2-123">-Synchronizationıd</span><span class="sxs-lookup"><span data-stu-id="4a7b2-123">-SynchronizationId</span></span>
<span data-ttu-id="4a7b2-124">Abonelik paylaşımının eşitleme kimliği</span><span class="sxs-lookup"><span data-stu-id="4a7b2-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="4a7b2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a7b2-125">CommonParameters</span></span>
<span data-ttu-id="4a7b2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a7b2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a7b2-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a7b2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a7b2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a7b2-128">INPUTS</span></span>

### <span data-ttu-id="4a7b2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4a7b2-129">System.String</span></span>

## <span data-ttu-id="4a7b2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a7b2-130">OUTPUTS</span></span>

### <span data-ttu-id="4a7b2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşım</span><span class="sxs-lookup"><span data-stu-id="4a7b2-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="4a7b2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a7b2-132">NOTES</span></span>

## <span data-ttu-id="4a7b2-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a7b2-133">RELATED LINKS</span></span>