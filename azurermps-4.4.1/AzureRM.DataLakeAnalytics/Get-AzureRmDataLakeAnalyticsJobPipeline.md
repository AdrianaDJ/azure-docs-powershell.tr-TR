---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 838fb221952a97234c31c514aa82fc30be7e2f25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594736"
---
# <span data-ttu-id="79123-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="79123-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="79123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79123-102">SYNOPSIS</span></span>
<span data-ttu-id="79123-103">Bir veri Lake Analytics Iş ardışık düzeni veya boru hattı alır.</span><span class="sxs-lookup"><span data-stu-id="79123-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79123-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79123-104">SYNTAX</span></span>

### <span data-ttu-id="79123-105">Tüm hesapta (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79123-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79123-106">Belirli proje ardışık düzeni</span><span class="sxs-lookup"><span data-stu-id="79123-106">Specific Job Pipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79123-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79123-107">DESCRIPTION</span></span>
<span data-ttu-id="79123-108">**Get-Azurermdatalakeanalyzer** , belirli bir Azure Data Lake Analytics iş ardışık düzeni veya ardışık düzen listesi alır.</span><span class="sxs-lookup"><span data-stu-id="79123-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="79123-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79123-109">EXAMPLES</span></span>

### <span data-ttu-id="79123-110">Örnek 1: belirtilen ardışık düzeni alma</span><span class="sxs-lookup"><span data-stu-id="79123-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="79123-111">Bu komut, ' contosoadla ' hesabında, kimliği ' 83cb7ad2-3523-4b82-b909-vseç478b0vseç8aea3 ' olan belirtilen ardışık düzeni alır.</span><span class="sxs-lookup"><span data-stu-id="79123-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="79123-112">Örnek 2: hesaptaki tüm ardışık düzene ait bir liste alma</span><span class="sxs-lookup"><span data-stu-id="79123-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="79123-113">Bu komut, "contosoadla" hesabındaki tüm ardışık düzene ait bir liste alır</span><span class="sxs-lookup"><span data-stu-id="79123-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="79123-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79123-114">PARAMETERS</span></span>

### <span data-ttu-id="79123-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="79123-115">-Account</span></span>
<span data-ttu-id="79123-116">Proje ardışık düzenini almak istediğiniz veri Lake Analytics hesap adının adı.</span><span class="sxs-lookup"><span data-stu-id="79123-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="79123-117">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="79123-117">-PipelineId</span></span>
<span data-ttu-id="79123-118">Bilgi döndürmek için belirli proje ardışık düzeninin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="79123-118">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Pipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79123-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="79123-119">-SubmittedAfter</span></span>
<span data-ttu-id="79123-120">Yalnızca belirtilen süreden sonra gönderilen iş ardışık düzenini döndüren isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="79123-120">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="79123-121">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="79123-121">-SubmittedBefore</span></span>
<span data-ttu-id="79123-122">Yalnızca belirtilen süreden önce gönderilen proje ardışık düzeni döndüren isteğe bağlı bir filtre.</span><span class="sxs-lookup"><span data-stu-id="79123-122">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="79123-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79123-123">-DefaultProfile</span></span>
<span data-ttu-id="79123-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79123-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79123-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79123-125">CommonParameters</span></span>
<span data-ttu-id="79123-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79123-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79123-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79123-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79123-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79123-128">INPUTS</span></span>

### <span data-ttu-id="79123-129">System. String</span><span class="sxs-lookup"><span data-stu-id="79123-129">System.String</span></span>

### <span data-ttu-id="79123-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="79123-130">System.Guid</span></span>

## <span data-ttu-id="79123-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79123-131">OUTPUTS</span></span>

### <span data-ttu-id="79123-132">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psjobpipelineınformation</span><span class="sxs-lookup"><span data-stu-id="79123-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="79123-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79123-133">NOTES</span></span>

## <span data-ttu-id="79123-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79123-134">RELATED LINKS</span></span>

