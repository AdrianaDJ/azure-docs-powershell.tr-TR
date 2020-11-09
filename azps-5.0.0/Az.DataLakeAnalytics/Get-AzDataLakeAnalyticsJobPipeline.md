---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320722"
---
# <span data-ttu-id="52c81-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="52c81-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="52c81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52c81-102">SYNOPSIS</span></span>
<span data-ttu-id="52c81-103">Bir veri Lake Analytics Iş ardışık düzeni veya boru hattı alır.</span><span class="sxs-lookup"><span data-stu-id="52c81-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="52c81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52c81-104">SYNTAX</span></span>

### <span data-ttu-id="52c81-105">GetAllInAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52c81-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52c81-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="52c81-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52c81-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52c81-107">DESCRIPTION</span></span>
<span data-ttu-id="52c81-108">**Get-Azdatalakeanaliz Ticsjobpipeline** , belirli bir Azure Data Lake Analytics iş ardışık düzeni veya ardışık düzen listesi alır.</span><span class="sxs-lookup"><span data-stu-id="52c81-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="52c81-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52c81-109">EXAMPLES</span></span>

### <span data-ttu-id="52c81-110">Örnek 1: belirtilen ardışık düzeni alma</span><span class="sxs-lookup"><span data-stu-id="52c81-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="52c81-111">Bu komut, ' contosoadla ' hesabında, kimliği ' 83cb7ad2-3523-4b82-b909-vseç478b0vseç8aea3 ' olan belirtilen ardışık düzeni alır.</span><span class="sxs-lookup"><span data-stu-id="52c81-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="52c81-112">Örnek 2: hesaptaki tüm ardışık düzene ait bir liste alma</span><span class="sxs-lookup"><span data-stu-id="52c81-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="52c81-113">Bu komut, "contosoadla" hesabındaki tüm ardışık düzene ait bir liste alır</span><span class="sxs-lookup"><span data-stu-id="52c81-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="52c81-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52c81-114">PARAMETERS</span></span>

### <span data-ttu-id="52c81-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="52c81-115">-Account</span></span>
<span data-ttu-id="52c81-116">Proje ardışık düzenini almak istediğiniz veri Lake Analytics hesap adının adı.</span><span class="sxs-lookup"><span data-stu-id="52c81-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="52c81-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c81-117">-DefaultProfile</span></span>
<span data-ttu-id="52c81-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52c81-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52c81-119">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="52c81-119">-PipelineId</span></span>
<span data-ttu-id="52c81-120">Bilgi döndürmek için belirli proje ardışık düzeninin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="52c81-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52c81-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="52c81-121">-SubmittedAfter</span></span>
<span data-ttu-id="52c81-122">Yalnızca belirtilen süreden sonra gönderilen iş ardışık düzenini döndüren isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="52c81-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c81-123">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="52c81-123">-SubmittedBefore</span></span>
<span data-ttu-id="52c81-124">Yalnızca belirtilen süreden önce gönderilen proje ardışık düzeni döndüren isteğe bağlı bir filtre.</span><span class="sxs-lookup"><span data-stu-id="52c81-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52c81-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c81-125">CommonParameters</span></span>
<span data-ttu-id="52c81-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52c81-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c81-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52c81-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c81-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52c81-128">INPUTS</span></span>

### <span data-ttu-id="52c81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="52c81-129">System.String</span></span>

### <span data-ttu-id="52c81-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="52c81-130">System.Guid</span></span>

### <span data-ttu-id="52c81-131">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="52c81-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="52c81-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52c81-132">OUTPUTS</span></span>

### <span data-ttu-id="52c81-133">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psjobpipelineınformation</span><span class="sxs-lookup"><span data-stu-id="52c81-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="52c81-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52c81-134">NOTES</span></span>

## <span data-ttu-id="52c81-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52c81-135">RELATED LINKS</span></span>
