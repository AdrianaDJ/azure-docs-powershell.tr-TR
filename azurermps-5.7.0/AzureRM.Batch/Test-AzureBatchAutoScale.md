---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/test-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 4258c5d83b15c2cecb6e2cd4e3edc216efec7a97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586815"
---
# <span data-ttu-id="68e21-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="68e21-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="68e21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e21-102">SYNOPSIS</span></span>
<span data-ttu-id="68e21-103">Havuzda otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="68e21-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68e21-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68e21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68e21-105">DESCRIPTION</span></span>
<span data-ttu-id="68e21-106">**Test-AzureBatchAutoScale** cmdlet 'i belirtilen havuzdaki otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="68e21-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="68e21-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68e21-107">EXAMPLES</span></span>

### <span data-ttu-id="68e21-108">Örnek 1: havuzda otomatik ölçeklendirme formülünü değerlendirme</span><span class="sxs-lookup"><span data-stu-id="68e21-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="68e21-109">İlk komut, örnekte kullanılmak üzere $Formula değişkeninde bir formül depolar.</span><span class="sxs-lookup"><span data-stu-id="68e21-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="68e21-110">İkinci komut, havuzda, KIMLIĞI etkileyen havuz içeren otomatik ölçeklendirme formülünü değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="68e21-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="68e21-111">Final komutu, standart nokta söz dizimini kullanarak **sonuçları** görüntüler.</span><span class="sxs-lookup"><span data-stu-id="68e21-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="68e21-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68e21-112">PARAMETERS</span></span>

### <span data-ttu-id="68e21-113">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="68e21-113">-AutoScaleFormula</span></span>
<span data-ttu-id="68e21-114">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e21-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e21-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="68e21-115">-BatchContext</span></span>
<span data-ttu-id="68e21-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e21-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="68e21-117">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68e21-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="68e21-118">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="68e21-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="68e21-119">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68e21-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="68e21-120">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68e21-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="68e21-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e21-121">-DefaultProfile</span></span>
<span data-ttu-id="68e21-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68e21-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68e21-123">-ID</span><span class="sxs-lookup"><span data-stu-id="68e21-123">-Id</span></span>
<span data-ttu-id="68e21-124">Otomatik ölçeklendirmeyi test etmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e21-124">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e21-125">CommonParameters</span></span>
<span data-ttu-id="68e21-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68e21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e21-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e21-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e21-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68e21-128">INPUTS</span></span>

### <span data-ttu-id="68e21-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="68e21-129">BatchAccountContext</span></span>
<span data-ttu-id="68e21-130">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="68e21-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="68e21-131">Dizisi</span><span class="sxs-lookup"><span data-stu-id="68e21-131">String</span></span>
<span data-ttu-id="68e21-132">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="68e21-132">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="68e21-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68e21-133">OUTPUTS</span></span>

### <span data-ttu-id="68e21-134">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="68e21-134">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="68e21-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68e21-135">NOTES</span></span>

## <span data-ttu-id="68e21-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68e21-136">RELATED LINKS</span></span>

[<span data-ttu-id="68e21-137">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="68e21-137">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="68e21-138">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="68e21-138">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="68e21-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="68e21-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="68e21-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="68e21-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


