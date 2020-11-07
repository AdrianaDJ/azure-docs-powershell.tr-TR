---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 43f9c55e6da93392e95191d1b601f771221e1caa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762966"
---
# <span data-ttu-id="7bccf-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="7bccf-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="7bccf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bccf-102">SYNOPSIS</span></span>
<span data-ttu-id="7bccf-103">Veri kaynağını bir veri Lake Analytics hesabından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bccf-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bccf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bccf-104">SYNTAX</span></span>

### <span data-ttu-id="7bccf-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bccf-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bccf-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7bccf-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bccf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bccf-107">DESCRIPTION</span></span>
<span data-ttu-id="7bccf-108">**Remove-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics hesabından veri kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bccf-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="7bccf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bccf-109">EXAMPLES</span></span>

### <span data-ttu-id="7bccf-110">Örnek 1: veri kaynağını kaldırma</span><span class="sxs-lookup"><span data-stu-id="7bccf-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="7bccf-111">Bu komut, AzureStorage01 adındaki veri kaynağını ContosoAdlAccount adlı hesaptan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bccf-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="7bccf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bccf-112">PARAMETERS</span></span>

### <span data-ttu-id="7bccf-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="7bccf-113">-Account</span></span>
<span data-ttu-id="7bccf-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bccf-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="7bccf-115">-Blob</span></span>
<span data-ttu-id="7bccf-116">Kaldırılacak AzureBlob depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bccf-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7bccf-117">-DataLakeStore</span></span>
<span data-ttu-id="7bccf-118">Kaldırılacak AzureData Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bccf-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bccf-119">-DefaultProfile</span></span>
<span data-ttu-id="7bccf-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7bccf-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7bccf-121">-Force</span></span>
<span data-ttu-id="7bccf-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7bccf-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bccf-123">-PassThru</span></span>
<span data-ttu-id="7bccf-124">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7bccf-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7bccf-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7bccf-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bccf-126">-ResourceGroupName</span></span>
<span data-ttu-id="7bccf-127">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bccf-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bccf-128">-Confirm</span></span>
<span data-ttu-id="7bccf-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bccf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bccf-130">-WhatIf</span></span>
<span data-ttu-id="7bccf-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bccf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bccf-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bccf-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bccf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bccf-133">CommonParameters</span></span>
<span data-ttu-id="7bccf-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bccf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bccf-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bccf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bccf-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bccf-136">INPUTS</span></span>

### <span data-ttu-id="7bccf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7bccf-137">System.String</span></span>

## <span data-ttu-id="7bccf-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bccf-138">OUTPUTS</span></span>

### <span data-ttu-id="7bccf-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7bccf-139">System.Boolean</span></span>

## <span data-ttu-id="7bccf-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bccf-140">NOTES</span></span>

## <span data-ttu-id="7bccf-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bccf-141">RELATED LINKS</span></span>

[<span data-ttu-id="7bccf-142">Add-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="7bccf-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="7bccf-143">Set-Azurermdatalakeanalyzer Ticsdatasource</span><span class="sxs-lookup"><span data-stu-id="7bccf-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


