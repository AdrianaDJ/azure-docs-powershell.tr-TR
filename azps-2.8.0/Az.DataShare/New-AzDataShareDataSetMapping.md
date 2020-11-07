---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSetMapping.md
ms.openlocfilehash: 0d7e1d62db25b70423ac40bc53ae0ff68f609eb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752183"
---
# <span data-ttu-id="2408c-101">New-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2408c-101">New-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="2408c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2408c-102">SYNOPSIS</span></span>
<span data-ttu-id="2408c-103">Paylaşım aboneliği için veri kümesi eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2408c-103">Creates data set mapping for share subscription.</span></span>

## <span data-ttu-id="2408c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2408c-104">SYNTAX</span></span>

### <span data-ttu-id="2408c-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2408c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSetMapping [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2408c-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="2408c-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -Container <String> [-FilePath <String>]
 [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2408c-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="2408c-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 -Name <String> -StorageAccountResourceId <String> -DataSetId <String> -FileSystem <String>
 [-FilePath <String>] [-FolderPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2408c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2408c-108">DESCRIPTION</span></span>
<span data-ttu-id="2408c-109">**New-AzDataShareDataSetMapping** cmdlet 'i, paylaşım aboneliğindeki kaynak veri kümeleri ve havuz depolama hesabı arasında veri kümesi eşlemesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2408c-109">The **New-AzDataShareDataSetMapping** cmdlet creates a data set mapping between the source data sets and sink storage account in share subscription.</span></span>

## <span data-ttu-id="2408c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2408c-110">EXAMPLES</span></span>

### <span data-ttu-id="2408c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2408c-111">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccoutName "WikiAdsAccount" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsDataSetMapping" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName        : AdsContainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : AdsStorage
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/AdsShareSubscription/dataSetMappings/AdsDataSetMapping
Name                 : AdsDataSetMapping
Type                 : Microsoft.DataShare/DataSetMappings
```

<span data-ttu-id="2408c-112">Bu komut, veri paylaşımı hesabı WikiAdsAccount ' deki paylaşım aboneliği Adsshar, Share aboneliğinin</span><span class="sxs-lookup"><span data-stu-id="2408c-112">This command creates a data set mapping AdsDataSetMapping to storage account AdsStorage for share subscription AdsShareSubscription in data share account WikiAdsAccount.</span></span>

## <span data-ttu-id="2408c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2408c-113">PARAMETERS</span></span>

### <span data-ttu-id="2408c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2408c-114">-AccountName</span></span>
<span data-ttu-id="2408c-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="2408c-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-116">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="2408c-116">-Container</span></span>
<span data-ttu-id="2408c-117">Azure depolama hesabı kapsayıcısı adı</span><span class="sxs-lookup"><span data-stu-id="2408c-117">Azure storage account container name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-118">-DataSetId</span><span class="sxs-lookup"><span data-stu-id="2408c-118">-DataSetId</span></span>
<span data-ttu-id="2408c-119">Tüketici veri kümesi kimliği</span><span class="sxs-lookup"><span data-stu-id="2408c-119">Consumer data set id</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2408c-120">-DefaultProfile</span></span>
<span data-ttu-id="2408c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2408c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2408c-122">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="2408c-122">-FilePath</span></span>
<span data-ttu-id="2408c-123">Azure depolama dosya yolu</span><span class="sxs-lookup"><span data-stu-id="2408c-123">Azure storage file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-124">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2408c-124">-FileSystem</span></span>
<span data-ttu-id="2408c-125">Azure ADLS Gen2 dosya sistemi adı</span><span class="sxs-lookup"><span data-stu-id="2408c-125">Azure ADLS gen2 file system name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-126">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="2408c-126">-FolderPath</span></span>
<span data-ttu-id="2408c-127">Azure depolama klasörü yolu</span><span class="sxs-lookup"><span data-stu-id="2408c-127">Azure storage folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="2408c-128">-Name</span></span>
<span data-ttu-id="2408c-129">Azure veri kümesi eşleme adı</span><span class="sxs-lookup"><span data-stu-id="2408c-129">Azure data set mapping name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2408c-130">-ResourceGroupName</span></span>
<span data-ttu-id="2408c-131">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2408c-131">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-132">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2408c-132">-ShareSubscriptionName</span></span>
<span data-ttu-id="2408c-133">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="2408c-133">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-134">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="2408c-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="2408c-135">Azure depolama hesabı RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2408c-135">Azure Storage Account ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2408c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="2408c-136">-Confirm</span></span>
<span data-ttu-id="2408c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2408c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2408c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2408c-138">-WhatIf</span></span>
<span data-ttu-id="2408c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2408c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2408c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2408c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2408c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2408c-141">CommonParameters</span></span>
<span data-ttu-id="2408c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2408c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2408c-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2408c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2408c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2408c-144">INPUTS</span></span>

### <span data-ttu-id="2408c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2408c-145">System.String</span></span>

## <span data-ttu-id="2408c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2408c-146">OUTPUTS</span></span>

### <span data-ttu-id="2408c-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="2408c-147">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="2408c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2408c-148">NOTES</span></span>

## <span data-ttu-id="2408c-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2408c-149">RELATED LINKS</span></span>
