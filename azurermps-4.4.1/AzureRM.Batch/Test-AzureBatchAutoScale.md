---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: BF0C1A2F-2703-492F-A3A7-053416A5D1EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Test-AzureBatchAutoScale.md
ms.openlocfilehash: 2ab8ca197c1d78980e1683f9572f6d3f6d4d55fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762074"
---
# <span data-ttu-id="8ede6-101">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ede6-101">Test-AzureBatchAutoScale</span></span>

## <span data-ttu-id="8ede6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ede6-102">SYNOPSIS</span></span>
<span data-ttu-id="8ede6-103">Havuzda otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="8ede6-103">Gets the result of an automatic scaling formula on a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ede6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ede6-104">SYNTAX</span></span>

```
Test-AzureBatchAutoScale [-Id] <String> [-AutoScaleFormula] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ede6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ede6-105">DESCRIPTION</span></span>
<span data-ttu-id="8ede6-106">**Test-AzureBatchAutoScale** cmdlet 'i belirtilen havuzdaki otomatik ölçeklendirme formülünün sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="8ede6-106">The **Test-AzureBatchAutoScale** cmdlet gets the result of an automatic scaling formula on the specified pool.</span></span>

## <span data-ttu-id="8ede6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ede6-107">EXAMPLES</span></span>

### <span data-ttu-id="8ede6-108">Örnek 1: havuzda otomatik ölçeklendirme formülünü değerlendirme</span><span class="sxs-lookup"><span data-stu-id="8ede6-108">Example 1: Evaluate an autoscale formula on a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> $Evaluation = Test-AzureBatchAutoScale -Id "ContosoPool" -AutoScaleFormula $Formula -BatchContext $Context
PS C:\> $Evaluation.AutoScaleRun.Results
$TargetDedicated=5;$NodeDeallocationOption=requeue;totalNodes=5
```

<span data-ttu-id="8ede6-109">İlk komut, örnekte kullanılmak üzere $Formula değişkeninde bir formül depolar.</span><span class="sxs-lookup"><span data-stu-id="8ede6-109">The first command stores a formula in the $Formula variable for use in the example.</span></span>

<span data-ttu-id="8ede6-110">İkinci komut, havuzda, KIMLIĞI etkileyen havuz içeren otomatik ölçeklendirme formülünü değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="8ede6-110">The second command evaluates the autoscale formula on the pool that has the ID ContosoPool.</span></span>

<span data-ttu-id="8ede6-111">Final komutu, standart nokta söz dizimini kullanarak **sonuçları** görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8ede6-111">The final command displays the **Results** by using standard dot syntax.</span></span>

## <span data-ttu-id="8ede6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ede6-112">PARAMETERS</span></span>

### <span data-ttu-id="8ede6-113">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="8ede6-113">-AutoScaleFormula</span></span>
<span data-ttu-id="8ede6-114">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ede6-114">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="8ede6-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8ede6-115">-BatchContext</span></span>
<span data-ttu-id="8ede6-116">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ede6-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ede6-117">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ede6-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="8ede6-118">-ID</span><span class="sxs-lookup"><span data-stu-id="8ede6-118">-Id</span></span>
<span data-ttu-id="8ede6-119">Otomatik ölçeklendirmeyi test etmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ede6-119">Specifies the object ID of the pool for which to test automatic scaling.</span></span>

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

### <span data-ttu-id="8ede6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ede6-120">-DefaultProfile</span></span>
<span data-ttu-id="8ede6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ede6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ede6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ede6-122">CommonParameters</span></span>
<span data-ttu-id="8ede6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ede6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ede6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ede6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ede6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ede6-125">INPUTS</span></span>

### <span data-ttu-id="8ede6-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ede6-126">BatchAccountContext</span></span>
<span data-ttu-id="8ede6-127">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8ede6-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="8ede6-128">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8ede6-128">String</span></span>
<span data-ttu-id="8ede6-129">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8ede6-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8ede6-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ede6-130">OUTPUTS</span></span>

### <span data-ttu-id="8ede6-131">PSAutoScaleEvaluation</span><span class="sxs-lookup"><span data-stu-id="8ede6-131">PSAutoScaleEvaluation</span></span>

## <span data-ttu-id="8ede6-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ede6-132">NOTES</span></span>

## <span data-ttu-id="8ede6-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ede6-133">RELATED LINKS</span></span>

[<span data-ttu-id="8ede6-134">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ede6-134">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="8ede6-135">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ede6-135">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="8ede6-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8ede6-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8ede6-137">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="8ede6-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


