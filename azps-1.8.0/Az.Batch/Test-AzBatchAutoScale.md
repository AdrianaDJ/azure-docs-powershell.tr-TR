---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/test-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Test-AzBatchAutoScale.md
ms.openlocfilehash: dcac72f8ca362ea87d464e024d6e77b2b3b61425
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761817"
---
# <span data-ttu-id="ec6cd-101">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="ec6cd-101">Test-AzBatchAutoScale</span></span>

## <span data-ttu-id="ec6cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec6cd-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6cd-103">Havuzda otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-103">Gets the result of an automatic scaling formula on a pool.</span></span>

## <span data-ttu-id="ec6cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec6cd-104">SYNTAX</span></span>

```
Test-AzBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec6cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec6cd-105">DESCRIPTION</span></span>
<span data-ttu-id="ec6cd-106">**Test-Azbatchotomatik ölçeklendirme** cmdlet 'i, belirtilen havuzdaki otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-106">The **Test-AzBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="ec6cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec6cd-107">EXAMPLES</span></span>

### <span data-ttu-id="ec6cd-108">Örnek 1: havuzda otomatik ölçeklendirme formülünü değerlendirme</span><span class="sxs-lookup"><span data-stu-id="ec6cd-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="ec6cd-109">İlk komut, örnekte kullanılmak üzere $Formula değişkeninde bir formül depolar.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>
<span data-ttu-id="ec6cd-110">İkinci komut, havuzda, KIMLIĞI etkileyen havuz içeren otomatik ölçeklendirme formülünü değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>
<span data-ttu-id="ec6cd-111">Final komutu, standart nokta söz dizimini kullanarak **sonuçları** görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="ec6cd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec6cd-112">PARAMETERS</span></span>

### <span data-ttu-id="ec6cd-113">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="ec6cd-113">-AutoScaleFormula</span></span>
<span data-ttu-id="ec6cd-114">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6cd-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ec6cd-115">-BatchContext</span></span>
<span data-ttu-id="ec6cd-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ec6cd-117">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ec6cd-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ec6cd-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ec6cd-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ec6cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6cd-121">-DefaultProfile</span></span>
<span data-ttu-id="ec6cd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec6cd-123">-ID</span><span class="sxs-lookup"><span data-stu-id="ec6cd-123">-Id</span></span>
<span data-ttu-id="ec6cd-124">Otomatik ölçeklendirmeyi test etmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec6cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6cd-125">CommonParameters</span></span>
<span data-ttu-id="ec6cd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec6cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6cd-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec6cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6cd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec6cd-128">INPUTS</span></span>

### <span data-ttu-id="ec6cd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ec6cd-129">System.String</span></span>

### <span data-ttu-id="ec6cd-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ec6cd-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ec6cd-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec6cd-131">OUTPUTS</span></span>

### <span data-ttu-id="ec6cd-132">Microsoft.Azure.Commands.Batch. Modeller. Psautosalerun</span><span class="sxs-lookup"><span data-stu-id="ec6cd-132">Microsoft.Azure.Commands.Batch.Models.PSAutoScaleRun</span></span>

## <span data-ttu-id="ec6cd-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec6cd-133">NOTES</span></span>

## <span data-ttu-id="ec6cd-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec6cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="ec6cd-135">Disable-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="ec6cd-135">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="ec6cd-136">Enable-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="ec6cd-136">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="ec6cd-137">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="ec6cd-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ec6cd-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ec6cd-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


