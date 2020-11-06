---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchPool.md
ms.openlocfilehash: 8f5a4aee0087f34769f099b6e9b44d249b53f7d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592346"
---
# <span data-ttu-id="ab322-101">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ab322-101">Get-AzureBatchPool</span></span>

## <span data-ttu-id="ab322-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab322-102">SYNOPSIS</span></span>
<span data-ttu-id="ab322-103">Belirtilen toplu hesap altında toplu Iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ab322-103">Gets Batch pools under the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab322-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab322-104">SYNTAX</span></span>

### <span data-ttu-id="ab322-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab322-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab322-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="ab322-106">Id</span></span>
```
Get-AzureBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab322-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab322-107">DESCRIPTION</span></span>
<span data-ttu-id="ab322-108">**Get-AzureBatchPool** cmdlet 'ı, *batchcontext* parametresiyle belirtilen toplu Iş hesabı altındaki Azure toplu iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="ab322-108">The **Get-AzureBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="ab322-109">Tek bir havuz almak için *ID* parametresini kullanabilir veya açık bir veri Protokolü (OData) filtresiyle eşleşen havuzları almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab322-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="ab322-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab322-110">EXAMPLES</span></span>

### <span data-ttu-id="ab322-111">Örnek 1: KIMLIĞE göre havuz alma</span><span class="sxs-lookup"><span data-stu-id="ab322-111">Example 1: Get a pool by ID</span></span>
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

<span data-ttu-id="ab322-112">Bu komut MyPool KIMLIKLI havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="ab322-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="ab322-113">Örnek 2: OData filtresi kullanarak tüm havuzları alma</span><span class="sxs-lookup"><span data-stu-id="ab322-113">Example 2: Get all pools using an OData filter</span></span>
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

<span data-ttu-id="ab322-114">Bu komut, kimlikleri *Filter* parametresini kullanarak kimlikleri ile başlayan havuzları alır.</span><span class="sxs-lookup"><span data-stu-id="ab322-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="ab322-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab322-115">PARAMETERS</span></span>

### <span data-ttu-id="ab322-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab322-116">-BatchContext</span></span>
<span data-ttu-id="ab322-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab322-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ab322-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab322-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="ab322-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab322-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ab322-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab322-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ab322-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab322-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab322-122">-DefaultProfile</span></span>
<span data-ttu-id="ab322-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab322-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab322-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="ab322-124">-Expand</span></span>
<span data-ttu-id="ab322-125">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="ab322-126">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab322-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="ab322-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ab322-127">-Filter</span></span>
<span data-ttu-id="ab322-128">Havuzlar sorgulanırken kullanılacak OData filtresi yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="ab322-129">Filtre belirtmezseniz, *Batchcontext* parametresiyle belirtilen toplu hesap altındaki Tüm havuzlar verilir.</span><span class="sxs-lookup"><span data-stu-id="ab322-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="ab322-130">-ID</span><span class="sxs-lookup"><span data-stu-id="ab322-130">-Id</span></span>
<span data-ttu-id="ab322-131">Alınacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="ab322-132">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab322-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ab322-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ab322-133">-MaxCount</span></span>
<span data-ttu-id="ab322-134">Döndürülecek en fazla havuz sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="ab322-135">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="ab322-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="ab322-136">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ab322-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="ab322-137">-Select</span><span class="sxs-lookup"><span data-stu-id="ab322-137">-Select</span></span>
<span data-ttu-id="ab322-138">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab322-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="ab322-139">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab322-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="ab322-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab322-140">CommonParameters</span></span>
<span data-ttu-id="ab322-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab322-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab322-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab322-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab322-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab322-143">INPUTS</span></span>

### <span data-ttu-id="ab322-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ab322-144">System.String</span></span>

### <span data-ttu-id="ab322-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab322-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ab322-146">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab322-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ab322-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab322-147">OUTPUTS</span></span>

### <span data-ttu-id="ab322-148">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="ab322-148">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="ab322-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab322-149">NOTES</span></span>

## <span data-ttu-id="ab322-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab322-150">RELATED LINKS</span></span>

[<span data-ttu-id="ab322-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ab322-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ab322-152">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ab322-152">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="ab322-153">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ab322-153">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="ab322-154">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ab322-154">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


