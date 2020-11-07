---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 6f89e7db5d2df2c475be1ac9875fd1e87217db77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765068"
---
# <span data-ttu-id="7a101-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a101-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="7a101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a101-102">SYNOPSIS</span></span>
<span data-ttu-id="7a101-103">Belirtilen toplu hesap altında toplu Iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7a101-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a101-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a101-104">SYNTAX</span></span>

### <span data-ttu-id="7a101-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a101-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a101-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="7a101-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a101-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a101-107">DESCRIPTION</span></span>
<span data-ttu-id="7a101-108">**Get-AzureBatchPool** cmdlet 'ı, *batchcontext* parametresiyle belirtilen toplu Iş hesabı altındaki Azure toplu iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7a101-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="7a101-109">Tek bir havuz almak için *ID* parametresini kullanabilir veya açık bir veri Protokolü (OData) filtresiyle eşleşen havuzları almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a101-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="7a101-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a101-110">EXAMPLES</span></span>

### <span data-ttu-id="7a101-111">Örnek 1: KIMLIĞE göre havuz alma</span><span class="sxs-lookup"><span data-stu-id="7a101-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzureBatchPool -Id "MyPool" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="7a101-112">Bu komut MyPool KIMLIKLI havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="7a101-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="7a101-113">Örnek 2: OData filtresi kullanarak tüm havuzları alma</span><span class="sxs-lookup"><span data-stu-id="7a101-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzureBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
AllocationState                      : Resizing
AllocationStateTransitionTime        : 7/25/2015 9:30:28 PM
AutoScaleEnabled                     : False
AutoScaleFormula                     : 
AutoScaleRun                         : 
CertificateReferences                : 
CreationTime                         : 7/25/2015 9:30:28 PM
CurrentDedicated                     : 0
CurrentOSVersion                     : *
DisplayName                          : 
ETag                                 : 0x8D29538429CF04C
Id                                   : MyPool
InterComputeNodeCommunicationEnabled : False
LastModified                         : 7/25/2015 9:30:28 PM
MaxTasksPerComputeNode               : 1
Metadata                             : 
OSFamily                             : 4
ResizeError                          : 
ResizeTimeout                        : 00:05:00
TaskSchedulingPolicy                 : Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
StartTask                            : 
State                                : Active
StateTransitionTime                  : 7/25/2015 9:30:28 PM
Statistics                           : 
TargetDedicated                      : 1
TargetOSVersion                      : *
Url                                  : https://cmdletexample.westus.batch.azure.com/pools/MyPool
VirtualMachineSize                   : small
```

<span data-ttu-id="7a101-114">Bu komut, kimlikleri *Filter* parametresini kullanarak kimlikleri ile başlayan havuzları alır.</span><span class="sxs-lookup"><span data-stu-id="7a101-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="7a101-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a101-115">PARAMETERS</span></span>

### <span data-ttu-id="7a101-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a101-116">-BatchContext</span></span>
<span data-ttu-id="7a101-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a101-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7a101-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="7a101-119">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="7a101-119">-Expand</span></span>
<span data-ttu-id="7a101-120">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-120">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="7a101-121">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a101-121">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="7a101-122">-Filtre</span><span class="sxs-lookup"><span data-stu-id="7a101-122">-Filter</span></span>
<span data-ttu-id="7a101-123">Havuzlar sorgulanırken kullanılacak OData filtresi yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-123">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="7a101-124">Filtre belirtmezseniz, *Batchcontext* parametresiyle belirtilen toplu hesap altındaki Tüm havuzlar verilir.</span><span class="sxs-lookup"><span data-stu-id="7a101-124">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a101-125">-ID</span><span class="sxs-lookup"><span data-stu-id="7a101-125">-Id</span></span>
<span data-ttu-id="7a101-126">Alınacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-126">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="7a101-127">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a101-127">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a101-128">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7a101-128">-MaxCount</span></span>
<span data-ttu-id="7a101-129">Döndürülecek en fazla havuz sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-129">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="7a101-130">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="7a101-130">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="7a101-131">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="7a101-131">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a101-132">-Select</span><span class="sxs-lookup"><span data-stu-id="7a101-132">-Select</span></span>
<span data-ttu-id="7a101-133">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a101-133">Specifies an OData select clause.</span></span>
<span data-ttu-id="7a101-134">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a101-134">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="7a101-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a101-135">-DefaultProfile</span></span>
<span data-ttu-id="7a101-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a101-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a101-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a101-137">CommonParameters</span></span>
<span data-ttu-id="7a101-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a101-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a101-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a101-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a101-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a101-140">INPUTS</span></span>

### <span data-ttu-id="7a101-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a101-141">BatchAccountContext</span></span>
<span data-ttu-id="7a101-142">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7a101-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="7a101-143">Dizisi</span><span class="sxs-lookup"><span data-stu-id="7a101-143">String</span></span>
<span data-ttu-id="7a101-144">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7a101-144">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="7a101-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a101-145">OUTPUTS</span></span>

### <span data-ttu-id="7a101-146">Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="7a101-146">PSCloudPool</span></span>

## <span data-ttu-id="7a101-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a101-147">NOTES</span></span>

## <span data-ttu-id="7a101-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a101-148">RELATED LINKS</span></span>

[<span data-ttu-id="7a101-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7a101-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7a101-150">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a101-150">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="7a101-151">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a101-151">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="7a101-152">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="7a101-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


