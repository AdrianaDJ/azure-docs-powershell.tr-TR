---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 0c591a60e1a7b1a5b5d20e7a4747bc8c08389816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752219"
---
# <span data-ttu-id="89469-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="89469-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="89469-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89469-102">SYNOPSIS</span></span>
<span data-ttu-id="89469-103">Azure veri paylaşımı 'ndaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="89469-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="89469-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89469-104">SYNTAX</span></span>

### <span data-ttu-id="89469-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89469-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89469-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="89469-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89469-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89469-107">DESCRIPTION</span></span>
<span data-ttu-id="89469-108">**Get-AzDataShareDataSet** cmdlet 'i Azure veri paylaşımı hesabındaki bir paylaşıma eklenmiş veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="89469-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="89469-109">Veri kümesinin adını belirtirseniz, bu cmdlet veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="89469-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="89469-110">Bir ad belirtmezseniz, bu cmdlet paylaşımdaki tüm veri kümeleri hakkında bilgi alır. Miyim</span><span class="sxs-lookup"><span data-stu-id="89469-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="89469-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89469-111">EXAMPLES</span></span>

### <span data-ttu-id="89469-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89469-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="89469-113">Bu komut, Azure veri paylaşımı hesap WikiAdsAccount ve kaynak grup REKLAMLARı 'ndaki Share AdsShare 'daki veri kümesi Adsiveri kümesi hakkındaki bilgileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="89469-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="89469-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89469-114">PARAMETERS</span></span>

### <span data-ttu-id="89469-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89469-115">-AccountName</span></span>
<span data-ttu-id="89469-116">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="89469-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="89469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89469-117">-DefaultProfile</span></span>
<span data-ttu-id="89469-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89469-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89469-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="89469-119">-Name</span></span>
<span data-ttu-id="89469-120">Azure veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="89469-120">Azure data set name.</span></span>

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

### <span data-ttu-id="89469-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89469-121">-ResourceGroupName</span></span>
<span data-ttu-id="89469-122">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="89469-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="89469-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89469-123">-ResourceId</span></span>
<span data-ttu-id="89469-124">Azure veri kümesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="89469-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="89469-125">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="89469-125">-ShareName</span></span>
<span data-ttu-id="89469-126">Azure veri paylaşımı adı.</span><span class="sxs-lookup"><span data-stu-id="89469-126">Azure data share name.</span></span>

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

### <span data-ttu-id="89469-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89469-127">CommonParameters</span></span>
<span data-ttu-id="89469-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89469-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89469-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89469-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89469-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89469-130">INPUTS</span></span>

### <span data-ttu-id="89469-131">System. String</span><span class="sxs-lookup"><span data-stu-id="89469-131">System.String</span></span>

## <span data-ttu-id="89469-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89469-132">OUTPUTS</span></span>

### <span data-ttu-id="89469-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="89469-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="89469-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89469-134">NOTES</span></span>

## <span data-ttu-id="89469-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89469-135">RELATED LINKS</span></span>
