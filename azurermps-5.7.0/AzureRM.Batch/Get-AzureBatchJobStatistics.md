---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: E655684D-9601-4A0B-BB09-EFB787EB2B1B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchjobstatistics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchJobStatistics.md
ms.openlocfilehash: 80ee6f881731f61b045e448e8a231ae9c971552d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591732"
---
# <span data-ttu-id="285a3-101">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="285a3-101">Get-AzureBatchJobStatistics</span></span>

## <span data-ttu-id="285a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285a3-102">SYNOPSIS</span></span>
<span data-ttu-id="285a3-103">Bir toplu hesabın Proje Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="285a3-103">Gets job summary statistics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="285a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="285a3-104">SYNTAX</span></span>

```
Get-AzureBatchJobStatistics -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="285a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="285a3-105">DESCRIPTION</span></span>
<span data-ttu-id="285a3-106">**Get-AzureBatchJobStatistics** cmdlet 'ı bir Azure toplu hesabındaki tüm işler için ömür Özeti istatistiklerini alır.</span><span class="sxs-lookup"><span data-stu-id="285a3-106">The **Get-AzureBatchJobStatistics** cmdlet gets lifetime summary statistics for all of the jobs in an Azure Batch account.</span></span>
<span data-ttu-id="285a3-107">İstatistikler, hesabın oluşturulmasından, istatistiklerin en son güncelleştirme saatine kadar, hesapta var olan tüm işlerde toplanır.</span><span class="sxs-lookup"><span data-stu-id="285a3-107">Statistics are aggregated across all jobs that have ever existed in the account, from account creation to the last update time of the statistics.</span></span>

## <span data-ttu-id="285a3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="285a3-108">EXAMPLES</span></span>

### <span data-ttu-id="285a3-109">Örnek 1: tüm işlerde Özet istatistikleri alma</span><span class="sxs-lookup"><span data-stu-id="285a3-109">Example 1: Get summary statistics for all jobs</span></span>
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

<span data-ttu-id="285a3-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="285a3-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="285a3-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="285a3-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="285a3-112">İkinci komut tüm işler için Özet istatistikleri alır.</span><span class="sxs-lookup"><span data-stu-id="285a3-112">The second command gets the summary statistics for all of the jobs.</span></span>
<span data-ttu-id="285a3-113">Komutta ilk komuttan $Context değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="285a3-113">The command uses the $Context value from the first command.</span></span>

## <span data-ttu-id="285a3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="285a3-114">PARAMETERS</span></span>

### <span data-ttu-id="285a3-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="285a3-115">-BatchContext</span></span>
<span data-ttu-id="285a3-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="285a3-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="285a3-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="285a3-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="285a3-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="285a3-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="285a3-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="285a3-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="285a3-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="285a3-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="285a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285a3-121">-DefaultProfile</span></span>
<span data-ttu-id="285a3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="285a3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="285a3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285a3-123">CommonParameters</span></span>
<span data-ttu-id="285a3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="285a3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285a3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285a3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285a3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="285a3-126">INPUTS</span></span>

### <span data-ttu-id="285a3-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="285a3-127">BatchAccountContext</span></span>
<span data-ttu-id="285a3-128">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="285a3-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="285a3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="285a3-129">OUTPUTS</span></span>

### <span data-ttu-id="285a3-130">PSJobStatistics</span><span class="sxs-lookup"><span data-stu-id="285a3-130">PSJobStatistics</span></span>

## <span data-ttu-id="285a3-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="285a3-131">NOTES</span></span>

## <span data-ttu-id="285a3-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="285a3-132">RELATED LINKS</span></span>

[<span data-ttu-id="285a3-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="285a3-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="285a3-134">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="285a3-134">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="285a3-135">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="285a3-135">Get-AzureBatchPoolUsageMetrics</span></span>](./Get-AzureBatchPoolUsageMetrics.md)


