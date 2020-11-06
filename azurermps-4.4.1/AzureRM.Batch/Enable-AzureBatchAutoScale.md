---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a85ac52622bb752b2e3437eb096f229c4d8e762
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594832"
---
# <span data-ttu-id="b0f7e-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b0f7e-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="b0f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0f7e-103">Havuzda otomatik ölçeklendirmeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0f7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b0f7e-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0f7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b0f7e-106">**Enable-AzureBatchAutoScale** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="b0f7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b0f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="b0f7e-108">Örnek 1: havuz için otomatik ölçeklendirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b0f7e-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="b0f7e-109">İlk komut bir formül tanımlar ve $Formula değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="b0f7e-110">İkinci komut, $Formula formülü kullanarak MyPool adlı havuzda otomatik ölçeklendirmeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="b0f7e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b0f7e-111">PARAMETERS</span></span>

### <span data-ttu-id="b0f7e-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="b0f7e-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="b0f7e-113">Otomatik ölçeklendirme formülüne göre havuz boyutu otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="b0f7e-114">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f7e-115">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="b0f7e-115">-AutoScaleFormula</span></span>
<span data-ttu-id="b0f7e-116">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0f7e-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b0f7e-117">-BatchContext</span></span>
<span data-ttu-id="b0f7e-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b0f7e-119">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b0f7e-120">-ID</span><span class="sxs-lookup"><span data-stu-id="b0f7e-120">-Id</span></span>
<span data-ttu-id="b0f7e-121">Otomatik ölçeklendirmeyi etkinleştirmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-121">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="b0f7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0f7e-122">-DefaultProfile</span></span>
<span data-ttu-id="b0f7e-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0f7e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0f7e-124">CommonParameters</span></span>
<span data-ttu-id="b0f7e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b0f7e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0f7e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0f7e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0f7e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b0f7e-127">INPUTS</span></span>

### <span data-ttu-id="b0f7e-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b0f7e-128">BatchAccountContext</span></span>
<span data-ttu-id="b0f7e-129">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b0f7e-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b0f7e-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b0f7e-130">String</span></span>
<span data-ttu-id="b0f7e-131">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b0f7e-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b0f7e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b0f7e-132">OUTPUTS</span></span>

## <span data-ttu-id="b0f7e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b0f7e-133">NOTES</span></span>

## <span data-ttu-id="b0f7e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b0f7e-134">RELATED LINKS</span></span>

[<span data-ttu-id="b0f7e-135">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b0f7e-135">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="b0f7e-136">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="b0f7e-136">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="b0f7e-137">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b0f7e-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


