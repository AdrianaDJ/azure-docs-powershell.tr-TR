---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolusagemetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: b8a6a7b40d0dd4756aff94c1e1b653efef03bca6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587695"
---
# <span data-ttu-id="2f423-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="2f423-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="2f423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f423-102">SYNOPSIS</span></span>
<span data-ttu-id="2f423-103">Toplu hesap için havuz kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2f423-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f423-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f423-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f423-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f423-105">DESCRIPTION</span></span>
<span data-ttu-id="2f423-106">**Get-AzureBatchPoolUsageMetrics** cmdlet 'i belirtilen hesap için tek tek zaman aralıklarında havuz tarafından toplanan kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2f423-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="2f423-107">Belirli bir havuz ve bir zaman aralığı için istatistikleri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f423-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="2f423-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f423-108">EXAMPLES</span></span>

### <span data-ttu-id="2f423-109">Örnek 1: zaman aralığı için havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="2f423-109">Example 1: Get pool usage metrics for a time range</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> $StartTime = Get-Date -Date "2016-05-16 00:00:00Z"
PS C:\> $EndTime = Get-Date -Date "2016-05-16 01:00:00Z"
PS C:\> Get-AzureBatchPoolUsageMetrics -StartTime $StartTime -EndTime $EndTime -BatchContext $context
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

<span data-ttu-id="2f423-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f423-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="2f423-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="2f423-111">The command stores this object reference in the $Context variable.</span></span>

<span data-ttu-id="2f423-112">Sonraki iki komut Get-Date cmdlet 'ini kullanarak **TarihSaat** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f423-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="2f423-113">Komutlar, $StartTime ve $EndTime değişkenlerinde son komutla kullanım için depolar.</span><span class="sxs-lookup"><span data-stu-id="2f423-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>

<span data-ttu-id="2f423-114">Son komutu, belirli başlangıç ve bitiş zamanları arasındaki zaman aralığı boyunca havuz tarafından toplanan tüm havuz kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f423-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="2f423-115">Örnek 2: filtre kullanarak havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="2f423-115">Example 2: Get pool usage metrics by using a filter</span></span>
```
PS C:\>Get-AzureBatchPoolUsageMetrics -Filter "poolId eq 'ContosoPool'" -BatchContext $Context
DataEgressGiB      : 9.0496614575386E-06
DataIngressGiB     : 2.60043889284134E-05
EndTime            : 5/16/2016 5:30:00 PM
PoolId             : MyPool
StartTime          : 5/16/2016 5:00:00 PM
TotalCoreHours     : 12
VirtualMachineSize : standard_d4
```

<span data-ttu-id="2f423-116">Bu komut, ContosoPool adlı havuzun kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f423-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="2f423-117">Komut, havuzu belirtmek için bir filtre dizesi belirtir ve önceki örnekle aynı $Context değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f423-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="2f423-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f423-118">PARAMETERS</span></span>

### <span data-ttu-id="2f423-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2f423-119">-BatchContext</span></span>
<span data-ttu-id="2f423-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f423-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2f423-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f423-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2f423-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="2f423-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2f423-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f423-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2f423-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2f423-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2f423-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f423-125">-DefaultProfile</span></span>
<span data-ttu-id="2f423-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f423-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f423-127">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="2f423-127">-EndTime</span></span>
<span data-ttu-id="2f423-128">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f423-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="2f423-129">En az iki saat öncesine bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="2f423-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="2f423-130">Bitiş saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f423-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f423-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="2f423-131">-Filter</span></span>
<span data-ttu-id="2f423-132">Bu cmdlet 'in retruns ölçülerini filtrelemek için kullanılacak bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f423-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="2f423-133">Tek geçerli özellik bir dize değeriyle **poolId** .</span><span class="sxs-lookup"><span data-stu-id="2f423-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="2f423-134">Olası işlemler şunlardır: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="2f423-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f423-135">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="2f423-135">-StartTime</span></span>
<span data-ttu-id="2f423-136">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2f423-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="2f423-137">En az iki ve yarı saat daha önce bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="2f423-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="2f423-138">Başlangıç saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f423-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f423-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f423-139">CommonParameters</span></span>
<span data-ttu-id="2f423-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f423-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f423-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f423-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f423-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f423-142">INPUTS</span></span>

### <span data-ttu-id="2f423-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2f423-143">BatchAccountContext</span></span>
<span data-ttu-id="2f423-144">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2f423-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="2f423-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f423-145">OUTPUTS</span></span>

### <span data-ttu-id="2f423-146">Pspoolusage ölçümleri</span><span class="sxs-lookup"><span data-stu-id="2f423-146">PSPoolUsageMetrics</span></span>

## <span data-ttu-id="2f423-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f423-147">NOTES</span></span>

## <span data-ttu-id="2f423-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f423-148">RELATED LINKS</span></span>

[<span data-ttu-id="2f423-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2f423-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="2f423-150">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="2f423-150">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="2f423-151">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="2f423-151">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


