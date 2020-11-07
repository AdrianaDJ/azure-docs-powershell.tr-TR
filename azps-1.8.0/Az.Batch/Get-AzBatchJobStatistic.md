---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchjobstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchJobStatistic.md
ms.openlocfilehash: b2c62cf91410e2604875df6f82237445e153f6aa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761885"
---
# <span data-ttu-id="6982e-101">Get-AzBatchJobStatistic</span><span class="sxs-lookup"><span data-stu-id="6982e-101">Get-AzBatchJobStatistic</span></span>

## <span data-ttu-id="6982e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6982e-102">SYNOPSIS</span></span>
<span data-ttu-id="6982e-103">Bir toplu hesabın Proje Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6982e-103">Gets job summary statistics for a Batch account.</span></span>

## <span data-ttu-id="6982e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6982e-104">SYNTAX</span></span>

```
Get-AzBatchJobStatistic -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6982e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6982e-105">DESCRIPTION</span></span>
<span data-ttu-id="6982e-106">**Get-Azbatchjobstatistics** cmdlet 'ı bir Azure toplu hesabındaki tüm işler için ömür Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6982e-106">The **Get-AzBatchJobStatistic** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="6982e-107">İstatistikler, hesabın oluşturulmasından, istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm işlerde toplanır.</span><span class="sxs-lookup"><span data-stu-id="6982e-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="6982e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6982e-108">EXAMPLES</span></span>

### <span data-ttu-id="6982e-109">Örnek 1: tüm işlerde Özet istatistikleri alma</span><span class="sxs-lookup"><span data-stu-id="6982e-109">Example 1: Get summary statistics for all jobs</span></span>
```
PS C:\>Get-AzBatchJobStatistic -BatchContext $Context
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

<span data-ttu-id="6982e-110">İlk komut, **Get-AzBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6982e-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="6982e-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="6982e-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="6982e-112">İkinci komut tüm işler için Özet istatistikleri alır.</span><span class="sxs-lookup"><span data-stu-id="6982e-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="6982e-113">Komutta ilk komuttan $Context değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6982e-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="6982e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6982e-114">PARAMETERS</span></span>

### <span data-ttu-id="6982e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6982e-115">-BatchContext</span></span>
<span data-ttu-id="6982e-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6982e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6982e-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6982e-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="6982e-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="6982e-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="6982e-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6982e-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="6982e-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6982e-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="6982e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6982e-121">-DefaultProfile</span></span>
<span data-ttu-id="6982e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6982e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6982e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6982e-123">CommonParameters</span></span>
<span data-ttu-id="6982e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6982e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6982e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6982e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6982e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6982e-126">INPUTS</span></span>

### <span data-ttu-id="6982e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6982e-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="6982e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6982e-128">OUTPUTS</span></span>

### <span data-ttu-id="6982e-129">Microsoft.Azure.Commands.Batch. Modeller. PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="6982e-129">Microsoft.Azure.Commands.Batch.Models.PSJobStatistics</span></span>

## <span data-ttu-id="6982e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6982e-130">NOTES</span></span>

## <span data-ttu-id="6982e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6982e-131">RELATED LINKS</span></span>

[<span data-ttu-id="6982e-132">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="6982e-132">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="6982e-133">Get-Azbatchpoolistatistiğini</span><span class="sxs-lookup"><span data-stu-id="6982e-133">Get-AzBatchPoolStatistic</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="6982e-134">Get-AzBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="6982e-134">Get-AzBatchPoolUsageMetrics</span></span>](./Get-AzBatchPoolUsageMetric.md)


