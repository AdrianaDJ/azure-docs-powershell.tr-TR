---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchAutoScale.md
ms.openlocfilehash: 73c1efe9e25fa02dc06f367eae1d010562eba56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595095"
---
# <span data-ttu-id="bc2cb-101">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bc2cb-101">Enable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="bc2cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2cb-103">Havuzda otomatik ölçeklendirmeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-103">Enables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc2cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc2cb-104">SYNTAX</span></span>

```
Enable-AzureBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc2cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2cb-106">**Enable-AzureBatchAutoScale** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-106">The **Enable-AzureBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="bc2cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="bc2cb-108">Örnek 1: havuz için otomatik ölçeklendirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="bc2cb-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzureBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="bc2cb-109">İlk komut bir formül tanımlar ve $Formula değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>

<span data-ttu-id="bc2cb-110">İkinci komut, $Formula formülü kullanarak MyPool adlı havuzda otomatik ölçeklendirmeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="bc2cb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc2cb-111">PARAMETERS</span></span>

### <span data-ttu-id="bc2cb-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="bc2cb-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="bc2cb-113">Otomatik ölçeklendirme formülüne göre havuz boyutu otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="bc2cb-114">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2cb-115">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="bc2cb-115">-AutoScaleFormula</span></span>
<span data-ttu-id="bc2cb-116">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc2cb-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bc2cb-117">-BatchContext</span></span>
<span data-ttu-id="bc2cb-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bc2cb-119">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bc2cb-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bc2cb-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bc2cb-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bc2cb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc2cb-123">-DefaultProfile</span></span>
<span data-ttu-id="bc2cb-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc2cb-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bc2cb-125">-Id</span></span>
<span data-ttu-id="bc2cb-126">Otomatik ölçeklendirmeyi etkinleştirmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="bc2cb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2cb-127">CommonParameters</span></span>
<span data-ttu-id="bc2cb-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc2cb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2cb-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc2cb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2cb-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc2cb-130">INPUTS</span></span>

### <span data-ttu-id="bc2cb-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bc2cb-131">BatchAccountContext</span></span>
<span data-ttu-id="bc2cb-132">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bc2cb-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bc2cb-133">Dizisi</span><span class="sxs-lookup"><span data-stu-id="bc2cb-133">String</span></span>
<span data-ttu-id="bc2cb-134">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bc2cb-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bc2cb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc2cb-135">OUTPUTS</span></span>

## <span data-ttu-id="bc2cb-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc2cb-136">NOTES</span></span>

## <span data-ttu-id="bc2cb-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc2cb-137">RELATED LINKS</span></span>

[<span data-ttu-id="bc2cb-138">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bc2cb-138">Disable-AzureBatchAutoScale</span></span>](./Disable-AzureBatchAutoScale.md)

[<span data-ttu-id="bc2cb-139">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="bc2cb-139">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="bc2cb-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bc2cb-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


