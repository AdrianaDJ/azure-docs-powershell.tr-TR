---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 44D877F1-D066-4C9C-A797-05EF03785B54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPool.md
ms.openlocfilehash: a94b4b8bee590fa31972d2b80c9c3f2d06c566e6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761877"
---
# <span data-ttu-id="79e9d-101">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="79e9d-101">Get-AzBatchPool</span></span>

## <span data-ttu-id="79e9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="79e9d-103">Belirtilen toplu hesap altında toplu Iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-103">Gets Batch pools under the specified Batch account.</span></span>

## <span data-ttu-id="79e9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79e9d-104">SYNTAX</span></span>

### <span data-ttu-id="79e9d-105">ODataFilter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79e9d-105">ODataFilter (Default)</span></span>
```
Get-AzBatchPool [-Filter <String>] [-MaxCount <Int32>] [-Select <String>] [-Expand <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e9d-106">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="79e9d-106">Id</span></span>
```
Get-AzBatchPool [[-Id] <String>] [-Select <String>] [-Expand <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79e9d-107">DESCRIPTION</span></span>
<span data-ttu-id="79e9d-108">**Get-AzBatchPool** cmdlet 'ı, *batchcontext* parametresiyle belirtilen toplu Iş hesabı altındaki Azure toplu iş havuzlarını alır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-108">The **Get-AzBatchPool** cmdlet gets the Azure Batch pools under the Batch account specified with the *BatchContext* parameter.</span></span>
<span data-ttu-id="79e9d-109">Tek bir havuz almak için *ID* parametresini kullanabilir veya açık bir veri Protokolü (OData) filtresiyle eşleşen havuzları almak için *Filter* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e9d-109">You can use the *Id* parameter to get a single pool, or you can use the *Filter* parameter to get the pools that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="79e9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79e9d-110">EXAMPLES</span></span>

### <span data-ttu-id="79e9d-111">Örnek 1: KIMLIĞE göre havuz alma</span><span class="sxs-lookup"><span data-stu-id="79e9d-111">Example 1: Get a pool by ID</span></span>
```
PS C:\>Get-AzBatchPool -Id "MyPool" -BatchContext $Context
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

<span data-ttu-id="79e9d-112">Bu komut MyPool KIMLIKLI havuzu alır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-112">This command gets the pool with ID MyPool.</span></span>

### <span data-ttu-id="79e9d-113">Örnek 2: OData filtresi kullanarak tüm havuzları alma</span><span class="sxs-lookup"><span data-stu-id="79e9d-113">Example 2: Get all pools using an OData filter</span></span>
```
PS C:\>Get-AzBatchPool -Filter "startswith(id,'My')" -BatchContext $Context
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

<span data-ttu-id="79e9d-114">Bu komut, kimlikleri *Filter* parametresini kullanarak kimlikleri ile başlayan havuzları alır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-114">This command gets the pools whose IDs start with My by using the *Filter* parameter.</span></span>

## <span data-ttu-id="79e9d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79e9d-115">PARAMETERS</span></span>

### <span data-ttu-id="79e9d-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79e9d-116">-BatchContext</span></span>
<span data-ttu-id="79e9d-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79e9d-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79e9d-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="79e9d-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79e9d-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79e9d-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="79e9d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79e9d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e9d-122">-DefaultProfile</span></span>
<span data-ttu-id="79e9d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79e9d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e9d-124">-Genişletme</span><span class="sxs-lookup"><span data-stu-id="79e9d-124">-Expand</span></span>
<span data-ttu-id="79e9d-125">Açık Veri Protokolü (OData) genişletme yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-125">Specifies an Open Data Protocol (OData) expand clause.</span></span>
<span data-ttu-id="79e9d-126">Aldığınız ana varlığın ilişkili varlıklarını almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="79e9d-126">Specify a value for this parameter to get associated entities of the main entity that you get.</span></span>

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

### <span data-ttu-id="79e9d-127">-Filtre</span><span class="sxs-lookup"><span data-stu-id="79e9d-127">-Filter</span></span>
<span data-ttu-id="79e9d-128">Havuzlar sorgulanırken kullanılacak OData filtresi yan tümcesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-128">Specifies the OData filter clause to use when querying for pools.</span></span>
<span data-ttu-id="79e9d-129">Filtre belirtmezseniz, *Batchcontext* parametresiyle belirtilen toplu hesap altındaki Tüm havuzlar verilir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-129">If you do not specify a filter, all pools under the Batch account specified with the *BatchContext* parameter are returned.</span></span>

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

### <span data-ttu-id="79e9d-130">-ID</span><span class="sxs-lookup"><span data-stu-id="79e9d-130">-Id</span></span>
<span data-ttu-id="79e9d-131">Alınacak havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-131">Specifies the ID of the pool to get.</span></span>
<span data-ttu-id="79e9d-132">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="79e9d-132">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="79e9d-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="79e9d-133">-MaxCount</span></span>
<span data-ttu-id="79e9d-134">Döndürülecek en fazla havuz sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-134">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="79e9d-135">Sıfır (0) veya daha kısa bir değer belirtirseniz cmdlet üst sınırı kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="79e9d-135">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="79e9d-136">Varsayılan değer 1000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="79e9d-136">The default value is 1000.</span></span>

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

### <span data-ttu-id="79e9d-137">-Select</span><span class="sxs-lookup"><span data-stu-id="79e9d-137">-Select</span></span>
<span data-ttu-id="79e9d-138">Bir OData select yan tümcesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="79e9d-138">Specifies an OData select clause.</span></span>
<span data-ttu-id="79e9d-139">Tüm nesne özellikleri yerine belirli özellikleri almak için bu parametre için bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="79e9d-139">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="79e9d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e9d-140">CommonParameters</span></span>
<span data-ttu-id="79e9d-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79e9d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e9d-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e9d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e9d-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79e9d-143">INPUTS</span></span>

### <span data-ttu-id="79e9d-144">System. String</span><span class="sxs-lookup"><span data-stu-id="79e9d-144">System.String</span></span>

### <span data-ttu-id="79e9d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79e9d-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="79e9d-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79e9d-146">OUTPUTS</span></span>

### <span data-ttu-id="79e9d-147">Microsoft.Azure.Commands.Batch. Modeller. Pscses havuzu</span><span class="sxs-lookup"><span data-stu-id="79e9d-147">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

## <span data-ttu-id="79e9d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79e9d-148">NOTES</span></span>

## <span data-ttu-id="79e9d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79e9d-149">RELATED LINKS</span></span>

[<span data-ttu-id="79e9d-150">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="79e9d-150">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="79e9d-151">Yeni-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="79e9d-151">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="79e9d-152">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="79e9d-152">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="79e9d-153">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="79e9d-153">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

