---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: 25fe1f4e89b7ea569899fc980a55c3a30acbf77a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594819"
---
# <span data-ttu-id="5c160-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="5c160-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="5c160-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c160-102">SYNOPSIS</span></span>
<span data-ttu-id="5c160-103">Toplu hesap için havuz Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="5c160-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c160-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c160-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c160-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c160-105">DESCRIPTION</span></span>
<span data-ttu-id="5c160-106">**Get-AzureBatchPoolStatistics** cmdlet 'i belirtilen hesaptaki tüm havuzların kullanım ömrü istatistiğini alır.</span><span class="sxs-lookup"><span data-stu-id="5c160-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="5c160-107">İstatistikler, hesap oluşturma aşamasından istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm havuzlardan toplanır.</span><span class="sxs-lookup"><span data-stu-id="5c160-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="5c160-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c160-108">EXAMPLES</span></span>

### <span data-ttu-id="5c160-109">Örnek 1: hesaptaki tüm havuzlardaki kaynak istatistiklerini alma</span><span class="sxs-lookup"><span data-stu-id="5c160-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzureBatchPoolStatistics -BatchContext $Context
PS C:\> $PoolStatistics.ResourceStatistics 
AverageCpuPercentage : 0.351232518750755
AverageDiskGiB       : 55.2569014701165
AverageMemoryGiB     : 2.87273772318252
DiskReadGiB          : 45.1326256990433
DiskReadIOps         : 878278
DiskWriteGiB         : 1230.72120628133
DiskWriteIOps        : 176832212
LastUpdateTime       : 5/16/2016 4:30:00 PM
NetworkReadGiB       : 29.3502839952707
NetworkWriteGiB      : 25.5208827350289
PeakDiskGiB          : 21.9638671875
PeakMemoryGiB        : 1.11184692382813
StartTime            : 2/10/2016 7:07:24 PM
```

<span data-ttu-id="5c160-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c160-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="5c160-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="5c160-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="5c160-112">İkinci komut belirtilen hesaptaki tüm havuzların istatistiklerini alır ve $PoolStatistics depolar.</span><span class="sxs-lookup"><span data-stu-id="5c160-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="5c160-113">Final komutu $PoolStatistics 'un **Resourcestatistiği** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5c160-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="5c160-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c160-114">PARAMETERS</span></span>

### <span data-ttu-id="5c160-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5c160-115">-BatchContext</span></span>
<span data-ttu-id="5c160-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c160-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5c160-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5c160-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="5c160-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c160-118">-DefaultProfile</span></span>
<span data-ttu-id="5c160-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c160-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c160-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c160-120">CommonParameters</span></span>
<span data-ttu-id="5c160-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c160-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c160-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c160-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c160-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c160-123">INPUTS</span></span>

### <span data-ttu-id="5c160-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5c160-124">BatchAccountContext</span></span>
<span data-ttu-id="5c160-125">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5c160-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="5c160-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c160-126">OUTPUTS</span></span>

### <span data-ttu-id="5c160-127">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="5c160-127">PSPoolStatistics</span></span>

## <span data-ttu-id="5c160-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c160-128">NOTES</span></span>

## <span data-ttu-id="5c160-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c160-129">RELATED LINKS</span></span>

[<span data-ttu-id="5c160-130">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5c160-130">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5c160-131">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="5c160-131">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="5c160-132">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="5c160-132">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


