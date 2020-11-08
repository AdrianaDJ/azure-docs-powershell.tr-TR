---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 8188C617-4895-4B43-8D3B-FA6FC5B868DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolStatistic.md
ms.openlocfilehash: 650d5fdd615ad44c30417eb0927e4c946e6a92d5
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107180"
---
# <span data-ttu-id="54341-101">Get-AzBatchPoolStatistic</span><span class="sxs-lookup"><span data-stu-id="54341-101">Get-AzBatchPoolStatistic</span></span>

## <span data-ttu-id="54341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54341-102">SYNOPSIS</span></span>
<span data-ttu-id="54341-103">Toplu hesap için havuz Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="54341-103">Gets pool summary statistics for a Batch account.</span></span>

## <span data-ttu-id="54341-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54341-104">SYNTAX</span></span>

```
Get-AzBatchPoolStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54341-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54341-105">DESCRIPTION</span></span>
<span data-ttu-id="54341-106">**Get-Azbatchpoolstatistics** cmdlet 'i belirtilen hesaptaki tüm havuzlardaki ömür istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="54341-106">The **Get-AzBatchPoolStatistic** cmdlet gets the lifetime statistics for all of the pools in the specified account.</span></span>
<span data-ttu-id="54341-107">İstatistikler, hesap oluşturma aşamasından istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm havuzlardan toplanır.</span><span class="sxs-lookup"><span data-stu-id="54341-107">Statistics are aggregated across all pools that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="54341-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54341-108">EXAMPLES</span></span>

### <span data-ttu-id="54341-109">Örnek 1: hesaptaki tüm havuzlardaki kaynak istatistiklerini alma</span><span class="sxs-lookup"><span data-stu-id="54341-109">Example 1: Get resource statistics of all pools in an account</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> $PoolStatistics = Get-AzBatchPoolStatistic -BatchContext $Context
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

<span data-ttu-id="54341-110">İlk komut, **Get-AzBatchAccountKey** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54341-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="54341-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="54341-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="54341-112">İkinci komut belirtilen hesaptaki tüm havuzların istatistiklerini alır ve $PoolStatistics depolar.</span><span class="sxs-lookup"><span data-stu-id="54341-112">The second command gets the statistics of all of the pools in the specified account, and then stores them in the $PoolStatistics.</span></span>
<span data-ttu-id="54341-113">Final komutu $PoolStatistics 'un **Resourcestatistiği** özelliğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="54341-113">The final command displays the **ResourceStatistics** property of $PoolStatistics.</span></span>

## <span data-ttu-id="54341-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54341-114">PARAMETERS</span></span>

### <span data-ttu-id="54341-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="54341-115">-BatchContext</span></span>
<span data-ttu-id="54341-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54341-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54341-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54341-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="54341-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="54341-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="54341-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54341-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="54341-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="54341-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="54341-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54341-121">-DefaultProfile</span></span>
<span data-ttu-id="54341-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54341-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54341-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54341-123">CommonParameters</span></span>
<span data-ttu-id="54341-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54341-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54341-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="54341-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54341-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54341-126">INPUTS</span></span>

### <span data-ttu-id="54341-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54341-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="54341-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54341-128">OUTPUTS</span></span>

### <span data-ttu-id="54341-129">Microsoft.Azure.Commands.Batch. Modeller. PSPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="54341-129">Microsoft.Azure.Commands.Batch.Models.PSPoolStatistics</span></span>

## <span data-ttu-id="54341-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54341-130">NOTES</span></span>

## <span data-ttu-id="54341-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54341-131">RELATED LINKS</span></span>

[<span data-ttu-id="54341-132">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="54341-132">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="54341-133">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="54341-133">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)

[<span data-ttu-id="54341-134">Get-Azbatchjobistatistiğini</span><span class="sxs-lookup"><span data-stu-id="54341-134">Get-AzBatchJobStatistic</span></span>](./Get-AzBatchJobStatistic.md)


