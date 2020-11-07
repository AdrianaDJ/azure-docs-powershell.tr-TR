---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4B373447-3078-4C1F-932E-8337AB170DEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpoolusagemetrics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPoolUsageMetrics.md
ms.openlocfilehash: 881e5d1cbd188589f4e0e28384ecf926b3495233
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763177"
---
# <span data-ttu-id="d7ce7-101">Get-AzureBatchPoolUsageMetrics</span><span class="sxs-lookup"><span data-stu-id="d7ce7-101">Get-AzureBatchPoolUsageMetrics</span></span>

## <span data-ttu-id="d7ce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ce7-103">Toplu hesap için havuz kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-103">Gets pool usage metrics for a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ce7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7ce7-104">SYNTAX</span></span>

```
Get-AzureBatchPoolUsageMetrics [-StartTime <DateTime>] [-EndTime <DateTime>] [-Filter <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7ce7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="d7ce7-106">**Get-AzureBatchPoolUsageMetrics** cmdlet 'i belirtilen hesap için tek tek zaman aralıklarında havuz tarafından toplanan kullanım ölçümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-106">The **Get-AzureBatchPoolUsageMetrics** cmdlet gets the usage metrics, aggregated by pool across individual time intervals, for the specified account.</span></span>
<span data-ttu-id="d7ce7-107">Belirli bir havuz ve bir zaman aralığı için istatistikleri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-107">You can get the statistics for a specific pool and for a time range.</span></span>

## <span data-ttu-id="d7ce7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7ce7-108">EXAMPLES</span></span>

### <span data-ttu-id="d7ce7-109">Örnek 1: zaman aralığı için havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="d7ce7-109">Example 1: Get pool usage metrics for a time range</span></span>
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

<span data-ttu-id="d7ce7-110">İlk komut, **Get-AzureRmBatchAccountKeys** kullanarak contosobatchaccount adlı toplu hesap için hesap anahtarlarına bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-110">The first command creates an object reference to the account keys for the batch account named ContosoBatchAccount by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="d7ce7-111">Komut bu nesne başvurusunu $Context değişkenine depolar.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-111">The command stores this object reference in the $Context variable.</span></span>
<span data-ttu-id="d7ce7-112">Sonraki iki komut Get-Date cmdlet 'ini kullanarak **TarihSaat** nesneleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-112">The next two commands create **DateTime** objects by using the Get-Date cmdlet.</span></span>
<span data-ttu-id="d7ce7-113">Komutlar, $StartTime ve $EndTime değişkenlerinde son komutla kullanım için depolar.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-113">The commands store these values in the $StartTime and $EndTime variables for use with the final command.</span></span>
<span data-ttu-id="d7ce7-114">Son komutu, belirli başlangıç ve bitiş zamanları arasındaki zaman aralığı boyunca havuz tarafından toplanan tüm havuz kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-114">The final command returns all of the pool usage metrics, aggregated by pool, across time interval between the specified start and end times.</span></span>

### <span data-ttu-id="d7ce7-115">Örnek 2: filtre kullanarak havuz kullanım ölçümlerini alma</span><span class="sxs-lookup"><span data-stu-id="d7ce7-115">Example 2: Get pool usage metrics by using a filter</span></span>
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

<span data-ttu-id="d7ce7-116">Bu komut, ContosoPool adlı havuzun kullanım ölçümlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-116">This command returns the usage metrics for pool named ContosoPool.</span></span>
<span data-ttu-id="d7ce7-117">Komut, havuzu belirtmek için bir filtre dizesi belirtir ve önceki örnekle aynı $Context değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-117">The command specifies a filter string to specify that pool, and uses the same $Context value as the previous example.</span></span>

## <span data-ttu-id="d7ce7-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7ce7-118">PARAMETERS</span></span>

### <span data-ttu-id="d7ce7-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d7ce7-119">-BatchContext</span></span>
<span data-ttu-id="d7ce7-120">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d7ce7-121">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d7ce7-122">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d7ce7-123">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d7ce7-124">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d7ce7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ce7-125">-DefaultProfile</span></span>
<span data-ttu-id="d7ce7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7ce7-127">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="d7ce7-127">-EndTime</span></span>
<span data-ttu-id="d7ce7-128">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının sonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-128">Specifies the end of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="d7ce7-129">En az iki saat öncesine bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-129">Specify a time at least two hours earlier.</span></span>
<span data-ttu-id="d7ce7-130">Bitiş saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-130">If you do not specify an end time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="d7ce7-131">-Filtre</span><span class="sxs-lookup"><span data-stu-id="d7ce7-131">-Filter</span></span>
<span data-ttu-id="d7ce7-132">Bu cmdlet 'in retruns ölçülerini filtrelemek için kullanılacak bir OData filtresi yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-132">Specifies an OData filter clause to use to filter the metrics that this cmdlet retruns.</span></span>
<span data-ttu-id="d7ce7-133">Tek geçerli özellik bir dize değeriyle **poolId** .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-133">The only valid property is **poolId** with a string value.</span></span>
<span data-ttu-id="d7ce7-134">Olası işlemler şunlardır: EQ, GE, gt, Le, lt, StartsWith.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-134">Possible operations are the following: eq, ge, gt, le, lt, startswith.</span></span>

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

### <span data-ttu-id="d7ce7-135">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d7ce7-135">-StartTime</span></span>
<span data-ttu-id="d7ce7-136">Bu cmdlet 'in kullanım ölçümlerini aldığı zaman aralığının başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-136">Specifies the start of a time range for which this cmdlet gets usage metrics.</span></span>
<span data-ttu-id="d7ce7-137">En az iki ve yarı saat daha önce bir saat belirtin.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-137">Specify a time at least two and a half hours earlier.</span></span>
<span data-ttu-id="d7ce7-138">Başlangıç saati belirtmezseniz, bu cmdlet Şu anda kullanılabilen son toplama aralığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-138">If you do not specify a start time, this cmdlet uses the last aggregation interval currently available.</span></span>

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

### <span data-ttu-id="d7ce7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ce7-139">CommonParameters</span></span>
<span data-ttu-id="d7ce7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7ce7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ce7-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ce7-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ce7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7ce7-142">INPUTS</span></span>

### <span data-ttu-id="d7ce7-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d7ce7-143">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="d7ce7-144">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7ce7-144">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="d7ce7-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7ce7-145">OUTPUTS</span></span>

### <span data-ttu-id="d7ce7-146">Microsoft.Azure.Commands.Batch. Modeller. Pspoolusage ölçümleri</span><span class="sxs-lookup"><span data-stu-id="d7ce7-146">Microsoft.Azure.Commands.Batch.Models.PSPoolUsageMetrics</span></span>

## <span data-ttu-id="d7ce7-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7ce7-147">NOTES</span></span>

## <span data-ttu-id="d7ce7-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7ce7-148">RELATED LINKS</span></span>

[<span data-ttu-id="d7ce7-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d7ce7-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d7ce7-150">Get-AzureBatchPoolStatistics</span><span class="sxs-lookup"><span data-stu-id="d7ce7-150">Get-AzureBatchPoolStatistics</span></span>](./Get-AzureBatchPoolStatistics.md)

[<span data-ttu-id="d7ce7-151">Get-AzureBatchJobStatistics</span><span class="sxs-lookup"><span data-stu-id="d7ce7-151">Get-AzureBatchJobStatistics</span></span>](./Get-AzureBatchJobStatistics.md)


