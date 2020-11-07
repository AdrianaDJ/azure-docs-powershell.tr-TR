---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: e6f4562daf77204a96991ddeef9164f2f6aff17a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752210"
---
# <span data-ttu-id="4d892-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4d892-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="4d892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d892-102">SYNOPSIS</span></span>
<span data-ttu-id="4d892-103">Paylaşım aboneliğindeki kaynak veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4d892-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="4d892-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d892-104">SYNTAX</span></span>

### <span data-ttu-id="4d892-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d892-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d892-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4d892-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d892-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d892-107">DESCRIPTION</span></span>
<span data-ttu-id="4d892-108">**Get-AzDataShareSourceDataSet** cmdlet 'i, paylaşım aboneliğindeki kaynak veri kümeleri hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d892-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="4d892-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d892-109">EXAMPLES</span></span>

### <span data-ttu-id="4d892-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4d892-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="4d892-111">Kaynak paylaşımında kullanılabilir veri kümelerini alır</span><span class="sxs-lookup"><span data-stu-id="4d892-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="4d892-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d892-112">PARAMETERS</span></span>

### <span data-ttu-id="4d892-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d892-113">-AccountName</span></span>
<span data-ttu-id="4d892-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="4d892-114">Azure data share account name</span></span>

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

### <span data-ttu-id="4d892-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d892-115">-DefaultProfile</span></span>
<span data-ttu-id="4d892-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d892-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d892-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d892-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d892-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4d892-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4d892-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4d892-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="4d892-120">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="4d892-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="4d892-121">-Sharesubscriptionresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d892-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="4d892-122">Azure veri paylaşımı aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4d892-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="4d892-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d892-123">CommonParameters</span></span>
<span data-ttu-id="4d892-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d892-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d892-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d892-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d892-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d892-126">INPUTS</span></span>

### <span data-ttu-id="4d892-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4d892-127">System.String</span></span>

## <span data-ttu-id="4d892-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d892-128">OUTPUTS</span></span>

### <span data-ttu-id="4d892-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="4d892-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="4d892-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d892-130">NOTES</span></span>

## <span data-ttu-id="4d892-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d892-131">RELATED LINKS</span></span>
