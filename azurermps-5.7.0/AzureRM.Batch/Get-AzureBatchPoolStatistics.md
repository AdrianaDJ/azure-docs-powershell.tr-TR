---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolStatistics.md
ms.openlocfilehash: e51f10fb7d1043e7a0f9addb9c874224ce952dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587699"
---
# <span data-ttu-id="9892b-101">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9892b-101">Get-AzureBatchPoolStatistics</span></span>

## <span data-ttu-id="9892b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9892b-102">SYNOPSIS</span></span>
<span data-ttu-id="9892b-103">Toplu hesap için havuz Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="9892b-103">Gets pool summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9892b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9892b-104">SYNTAX</span></span>

```
Get-AzureBatchPoolStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9892b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9892b-105">DESCRIPTION</span></span>
<span data-ttu-id="9892b-106">**Get-AzureBatchPoolStatistics** cmdlet 'i belirtilen hesaptaki tüm havuzların kullanım ömrü istatistiğini alır.</span><span class="sxs-lookup"><span data-stu-id="9892b-106">The **Get-AzureBatchPoolStatistics** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="9892b-107">İstatistikler, hesap oluşturma aşamasından istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm havuzlardan toplanır.</span><span class="sxs-lookup"><span data-stu-id="9892b-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="9892b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9892b-108">EXAMPLES</span></span>

### <span data-ttu-id="9892b-109">Örnek 1: hesaptaki tüm havuzlardaki kaynak istatistiklerini alma</span><span class="sxs-lookup"><span data-stu-id="9892b-109">Example 1: Get resource statistics of all pools in an account</span></span>
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

<span data-ttu-id="9892b-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9892b-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="9892b-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="9892b-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="9892b-112">İkinci komut belirtilen hesaptaki tüm havuzların istatistiklerini alır ve $PoolStatistics depolar.</span><span class="sxs-lookup"><span data-stu-id="9892b-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>

<span data-ttu-id="9892b-113">Final komutu $PoolStatistics 'un **Resourcestatistiği** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="9892b-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="9892b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9892b-114">PARAMETERS</span></span>

### <span data-ttu-id="9892b-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9892b-115">-BatchContext</span></span>
<span data-ttu-id="9892b-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9892b-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9892b-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9892b-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9892b-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="9892b-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9892b-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9892b-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9892b-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9892b-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9892b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9892b-121">-DefaultProfile</span></span>
<span data-ttu-id="9892b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9892b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9892b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9892b-123">CommonParameters</span></span>
<span data-ttu-id="9892b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9892b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9892b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9892b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9892b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9892b-126">INPUTS</span></span>

### <span data-ttu-id="9892b-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9892b-127">BatchAccountContext</span></span>
<span data-ttu-id="9892b-128">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9892b-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="9892b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9892b-129">OUTPUTS</span></span>

### <span data-ttu-id="9892b-130">PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="9892b-130">PSPoolStatistics</span></span>

## <span data-ttu-id="9892b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9892b-131">NOTES</span></span>

## <span data-ttu-id="9892b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9892b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9892b-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9892b-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9892b-134">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="9892b-134">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)

[<span data-ttu-id="9892b-135">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="9892b-135">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


