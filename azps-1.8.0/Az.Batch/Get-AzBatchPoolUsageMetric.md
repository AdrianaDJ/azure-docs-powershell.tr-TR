---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolusagemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolUsageMetric.md
ms.openlocfilehash: 480a39602f0218ed05122005a657c7e7870f7e88
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761872"
---
# <span data-ttu-id="41d12-101">Get-AzBatchPoolUsageMetric</span><span class="sxs-lookup"><span data-stu-id="41d12-101">Get-AzBatchPoolUsageMetric</span></span>

## <span data-ttu-id="41d12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d12-102">SYNOPSIS</span></span>
<span data-ttu-id="41d12-103">Toplu hesap için havuz kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="41d12-103">Gets pool usage metrics for a Batch account.</span></span>

## <span data-ttu-id="41d12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="41d12-104">SYNTAX</span></span>

```
Get-AzBatchPoolUsageMetric [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41d12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="41d12-105">DESCRIPTION</span></span>
<span data-ttu-id="41d12-106">**Get-AzBatchPoolUsageMetric** cmdlet 'i belirtilen hesap için tek tek zaman aralıklarında havuz tarafından toplanan kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="41d12-106">The **Get-AzBatchPoolUsageMetric** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="41d12-107">Belirli bir havuz ve bir zaman aralığı için istatistikleri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41d12-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="41d12-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="41d12-108">EXAMPLES</span></span>

### <span data-ttu-id="41d12-109">Örnek 1: zaman aralığı için havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="41d12-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzBatchPoolUsageMetric -StartTime $StartTime -EndTime $EndTime -BatchContext $context
DataEgressGiB      : 6.68875873088837E-06
DataIngressGiB     : 1.9485130906105E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 8
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.61587512493134E-06
DataIngressGiB     : 1.76150351762772E-05
EndTime            : 5/16/2016 12:30:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:00:00 AM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4

DataEgressGiB      : 7.36676156520844E-06
DataIngressGiB     : 2.10804864764214E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool1
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 7.99999999955555
VirtualMachineSize : standard_d4

DataEgressGiB      : 5.80586493015289E-06
DataIngressGiB     : 1.80602073669434E-05
EndTime            : 5/16/2016 1:00:00 AM
PoolId             : testpool2
StartTime          : 5/16/2016 12:30:00 AM
TotalCoreHours     : 11.9999999993333
VirtualMachineSize : standard_d4
```

<span data-ttu-id="41d12-110">İlk komut, **Get-AzBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41d12-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="41d12-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="41d12-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="41d12-112">Sonraki iki komut Get-Date cmdlet 'ini kullanarak **TarihSaat** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="41d12-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="41d12-113">Komutlar, $StartTime ve $EndTime değişkenlerinde son komutla kullanım için depolar.</span><span class="sxs-lookup"><span data-stu-id="41d12-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="41d12-114">Son komutu, belirli başlangıç ve bitiş zamanları arasındaki zaman aralığı boyunca havuz tarafından toplanan tüm havuz kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="41d12-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="41d12-115">Örnek 2: filtre kullanarak havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="41d12-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzBatchPoolUsageMetric -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="41d12-116">Bu komut, ContosoPool adlı havuzun kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="41d12-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="41d12-117">Komut, havuzu belirtmek için bir filtre dizesi belirtir ve önceki örnekle aynı $Context değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="41d12-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="41d12-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="41d12-118">PARAMETERS</span></span>

### <span data-ttu-id="41d12-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="41d12-119">-BatchContext</span></span>
<span data-ttu-id="41d12-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="41d12-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41d12-121">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d12-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="41d12-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="41d12-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="41d12-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="41d12-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="41d12-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="41d12-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="41d12-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d12-125">-DefaultProfile</span></span>
<span data-ttu-id="41d12-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="41d12-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41d12-127">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="41d12-127">-EndTime</span></span>
<span data-ttu-id="41d12-128">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="41d12-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="41d12-129">En az iki saat öncesine bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="41d12-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="41d12-130">Bitiş saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="41d12-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d12-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="41d12-131">-Filter</span></span>
<span data-ttu-id="41d12-132">Bu cmdlet 'in retruns ölçülerini filtrelemek için kullanılacak bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="41d12-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="41d12-133">Tek geçerli özellik bir dize değeriyle **poolId** .</span><span class="sxs-lookup"><span data-stu-id="41d12-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="41d12-134">Olası işlemler şunlardır: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="41d12-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d12-135">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="41d12-135">-StartTime</span></span>
<span data-ttu-id="41d12-136">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="41d12-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="41d12-137">En az iki ve yarı saat daha önce bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="41d12-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="41d12-138">Başlangıç saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="41d12-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d12-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d12-139">CommonParameters</span></span>
<span data-ttu-id="41d12-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="41d12-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d12-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d12-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d12-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="41d12-142">INPUTS</span></span>

### <span data-ttu-id="41d12-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="41d12-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="41d12-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="41d12-144">OUTPUTS</span></span>

### <span data-ttu-id="41d12-145">Microsoft.Azure.Commands.Batch. Modeller. Pspoolusage ölçümleri</span><span class="sxs-lookup"><span data-stu-id="41d12-145">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="41d12-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="41d12-146">NOTES</span></span>

## <span data-ttu-id="41d12-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="41d12-147">RELATED LINKS</span></span>

[<span data-ttu-id="41d12-148">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="41d12-148">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="41d12-149">Get-AzBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="41d12-149">Get-AzBatchPoolStatistics</span></span>](./Get-AzBatchPoolStatistic.md)

[<span data-ttu-id="41d12-150">Get-AzBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="41d12-150">Get-AzBatchJobStatistics</span></span>](./Get-AzBatchJobStatistic.md)

