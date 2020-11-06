---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 03b7e3999fbc482223365b59867c02c75e9d5ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590766"
---
# <span data-ttu-id="dcc1b-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="dcc1b-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="dcc1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc1b-103">Bir toplu hesabın Proje Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcc1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcc1b-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcc1b-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc1b-106">**Get-AzureBatchJobStatistics** cmdlet 'ı bir Azure toplu hesabındaki tüm işler için ömür Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="dcc1b-107">İstatistikler, hesabın oluşturulmasından, istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm işlerde toplanır.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="dcc1b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcc1b-108">EXAMPLES</span></span>

### <span data-ttu-id="dcc1b-109">Örnek 1: tüm işlerde Özet istatistikleri alma</span><span class="sxs-lookup"><span data-stu-id="dcc1b-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzureBatchJobStatistics -BatchContext $Context
FailedTaskCount    : 330
KernelCpuTime      : 00:24:31.8440000
LastUpdateTime     : 5/16/2016 6:00:00 PM
ReadIOGiB          : 38.1271341182292
ReadIOps           : 26546054
StartTime          : 11/3/2015 9:47:14 PM
SucceededTaskCount : 766
TaskRetryCount     : 0
Url                : https://accountname.westus.batch.azure.com/lifetimejobstats
UserCpuTime        : 20:55:50.3200000
WaitTime           : 03:54:49.8530000
WallClockTime      : 20:55:50.3200000
WriteIOGiB         : 0.159623090177774
WriteIOps          : 146946
```

<span data-ttu-id="dcc1b-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="dcc1b-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="dcc1b-112">İkinci komut tüm işler için Özet istatistikleri alır.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="dcc1b-113">Komutta ilk komuttan $Context değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="dcc1b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcc1b-114">PARAMETERS</span></span>

### <span data-ttu-id="dcc1b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dcc1b-115">-BatchContext</span></span>
<span data-ttu-id="dcc1b-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dcc1b-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcc1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc1b-118">-DefaultProfile</span></span>
<span data-ttu-id="dcc1b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcc1b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc1b-120">CommonParameters</span></span>
<span data-ttu-id="dcc1b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcc1b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc1b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcc1b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc1b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcc1b-123">INPUTS</span></span>

### <span data-ttu-id="dcc1b-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dcc1b-124">BatchAccountContext</span></span>
<span data-ttu-id="dcc1b-125">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="dcc1b-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="dcc1b-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcc1b-126">OUTPUTS</span></span>

### <span data-ttu-id="dcc1b-127">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="dcc1b-127">PSJobStatistics</span></span>

## <span data-ttu-id="dcc1b-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcc1b-128">NOTES</span></span>

## <span data-ttu-id="dcc1b-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcc1b-129">RELATED LINKS</span></span>

[<span data-ttu-id="dcc1b-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dcc1b-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dcc1b-131">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="dcc1b-131">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="dcc1b-132">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="dcc1b-132">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


