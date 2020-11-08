---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: cf8b235d0035955f809b167ba4d532cdae0538c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096191"
---
# <span data-ttu-id="09a42-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="09a42-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="09a42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a42-102">SYNOPSIS</span></span>
<span data-ttu-id="09a42-103">Paylaşma aboneliğindeki veri kümesi eşlemeleriyle ilgili bilgi alır</span><span class="sxs-lookup"><span data-stu-id="09a42-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="09a42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09a42-104">SYNTAX</span></span>

### <span data-ttu-id="09a42-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09a42-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09a42-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="09a42-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09a42-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="09a42-107">DESCRIPTION</span></span>
<span data-ttu-id="09a42-108">**Get-AzDataShareDataSetMapping** cmdlet 'i, ad belirtilmişse belirli bir veri kümesi eşlemesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="09a42-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="09a42-109">Aksi halde, bir paylaşım aboneliğindeki tüm veri kümesi eşlemeleriyle ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="09a42-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="09a42-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09a42-110">EXAMPLES</span></span>

### <span data-ttu-id="09a42-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="09a42-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="09a42-112">Bu komut, paylaşım aboneliğindeki tüm veri kümesi eşlemeleriyle ilgili bilgileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="09a42-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="09a42-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09a42-113">PARAMETERS</span></span>

### <span data-ttu-id="09a42-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09a42-114">-AccountName</span></span>
<span data-ttu-id="09a42-115">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="09a42-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="09a42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a42-116">-DefaultProfile</span></span>
<span data-ttu-id="09a42-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09a42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a42-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="09a42-118">-Name</span></span>
<span data-ttu-id="09a42-119">Azure veri kümesi eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="09a42-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="09a42-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a42-120">-ResourceGroupName</span></span>
<span data-ttu-id="09a42-121">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="09a42-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="09a42-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="09a42-122">-ResourceId</span></span>
<span data-ttu-id="09a42-123">Azure veri kümesi eşlemesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="09a42-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="09a42-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="09a42-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="09a42-125">Azure veri paylaşımı abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="09a42-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="09a42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a42-126">CommonParameters</span></span>
<span data-ttu-id="09a42-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09a42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a42-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09a42-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a42-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09a42-129">INPUTS</span></span>

### <span data-ttu-id="09a42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09a42-130">System.String</span></span>

## <span data-ttu-id="09a42-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09a42-131">OUTPUTS</span></span>

### <span data-ttu-id="09a42-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="09a42-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="09a42-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09a42-133">NOTES</span></span>

## <span data-ttu-id="09a42-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09a42-134">RELATED LINKS</span></span>