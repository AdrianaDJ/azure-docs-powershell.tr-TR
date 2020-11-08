---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareDataSet.md
ms.openlocfilehash: 567d1449bdf84770f4699c84618ccdad0ba43ac4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096304"
---
# <span data-ttu-id="b130f-101">New-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b130f-101">New-AzDataShareDataSet</span></span>

## <span data-ttu-id="b130f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b130f-102">SYNOPSIS</span></span>
<span data-ttu-id="b130f-103">Azure veri paylaşımına veri kümeleri ekler.</span><span class="sxs-lookup"><span data-stu-id="b130f-103">Adds data sets to azure data share.</span></span>

## <span data-ttu-id="b130f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b130f-104">SYNTAX</span></span>

### <span data-ttu-id="b130f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b130f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareDataSet [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b130f-106">ByBlobDataSetParamaterSet</span><span class="sxs-lookup"><span data-stu-id="b130f-106">ByBlobDataSetParamaterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -Container <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b130f-107">ByAdlsGen2DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b130f-107">ByAdlsGen2DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> -FileSystem <String> [-FilePath <String>] [-FolderPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b130f-108">ByAdlsGen1DataSetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b130f-108">ByAdlsGen1DataSetParameterSet</span></span>
```
New-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -StorageAccountResourceId <String> [-FileName <String>] -AdlsGen1FolderPath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b130f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b130f-109">DESCRIPTION</span></span>
<span data-ttu-id="b130f-110">**New-AzDataShareDataSet** cmdlet 'i veri paylaşımı hesabının Azure veri paylaşımında veri kümeleri ekler.</span><span class="sxs-lookup"><span data-stu-id="b130f-110">The **New-AzDataShareDataSet** cmdlet add data sets in azure data share of data share account.</span></span> <span data-ttu-id="b130f-111">Blob, ADLS Gen2 ve ADLS Gen1 türündeki veri kümeleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b130f-111">You can add data sets of type Blob, ADLS Gen2 and ADLS Gen1.</span></span>

## <span data-ttu-id="b130f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b130f-112">EXAMPLES</span></span>

### <span data-ttu-id="b130f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b130f-113">Example 1</span></span>
```
PS C:\> New-AzDataShareDataSet -ResourceroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet" -StorageAccountResourceId "/subscriptions/271cc6ec-e5fe-4813-83bd-8f3b04973e38/resourceGroups/ADS/providers/Microsoft.Storage/storageAccounts/AdsStorage" -Container "AdsContainer"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="b130f-114">Bu komut, Azure veri paylaşımı AdsShare türünde, blob kapsayıcı türündeki bir veri kümesi ekler.</span><span class="sxs-lookup"><span data-stu-id="b130f-114">This command adds a dataset named AdsDataSet of type blob container to azure data share AdsShare.</span></span>

## <span data-ttu-id="b130f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b130f-115">PARAMETERS</span></span>

### <span data-ttu-id="b130f-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b130f-116">-AccountName</span></span>
<span data-ttu-id="b130f-117">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="b130f-117">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-118">-AdlsGen1FolderPath</span><span class="sxs-lookup"><span data-stu-id="b130f-118">-AdlsGen1FolderPath</span></span>
<span data-ttu-id="b130f-119">Azure Storage ADLS Gen1 klasör yolu</span><span class="sxs-lookup"><span data-stu-id="b130f-119">Azure storage ADLS gen1 folder path</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-120">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="b130f-120">-Container</span></span>
<span data-ttu-id="b130f-121">Azure depolama hesabı kapsayıcısı adı</span><span class="sxs-lookup"><span data-stu-id="b130f-121">Azure storage account container name</span></span>

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

### <span data-ttu-id="b130f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b130f-122">-DefaultProfile</span></span>
<span data-ttu-id="b130f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b130f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b130f-124">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="b130f-124">-FileName</span></span>
<span data-ttu-id="b130f-125">Azure Storage ADLS Gen1 dosya adı</span><span class="sxs-lookup"><span data-stu-id="b130f-125">Azure storage ADLS gen1 file name</span></span>

```yaml
Type: System.String
Parameter Sets: ByAdlsGen1DataSetParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-126">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="b130f-126">-FilePath</span></span>
<span data-ttu-id="b130f-127">Azure depolama dosya yolu</span><span class="sxs-lookup"><span data-stu-id="b130f-127">Azure storage file path</span></span>

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

### <span data-ttu-id="b130f-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="b130f-128">-FileSystem</span></span>
<span data-ttu-id="b130f-129">Azure ADLS Gen2 dosya sistemi adı</span><span class="sxs-lookup"><span data-stu-id="b130f-129">Azure ADLS gen2 file system name</span></span>

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

### <span data-ttu-id="b130f-130">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="b130f-130">-FolderPath</span></span>
<span data-ttu-id="b130f-131">Azure depolama klasörü yolu</span><span class="sxs-lookup"><span data-stu-id="b130f-131">Azure storage folder path</span></span>

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

### <span data-ttu-id="b130f-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="b130f-132">-Name</span></span>
<span data-ttu-id="b130f-133">Azure veri kümesi adı</span><span class="sxs-lookup"><span data-stu-id="b130f-133">Azure data set name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b130f-134">-ResourceGroupName</span></span>
<span data-ttu-id="b130f-135">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b130f-135">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-136">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="b130f-136">-ShareName</span></span>
<span data-ttu-id="b130f-137">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="b130f-137">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-138">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="b130f-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="b130f-139">Azure depolama hesabı RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b130f-139">Azure storage account resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByBlobDataSetParamaterSet, ByAdlsGen2DataSetParameterSet, ByAdlsGen1DataSetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b130f-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="b130f-140">-Confirm</span></span>
<span data-ttu-id="b130f-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b130f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b130f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b130f-142">-WhatIf</span></span>
<span data-ttu-id="b130f-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b130f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b130f-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b130f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b130f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b130f-145">CommonParameters</span></span>
<span data-ttu-id="b130f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b130f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b130f-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b130f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b130f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b130f-148">INPUTS</span></span>

### <span data-ttu-id="b130f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b130f-149">System.String</span></span>

## <span data-ttu-id="b130f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b130f-150">OUTPUTS</span></span>

### <span data-ttu-id="b130f-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="b130f-151">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="b130f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b130f-152">NOTES</span></span>

## <span data-ttu-id="b130f-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b130f-153">RELATED LINKS</span></span>
