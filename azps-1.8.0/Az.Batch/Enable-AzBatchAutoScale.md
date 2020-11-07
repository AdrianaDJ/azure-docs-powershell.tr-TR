---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3107D061-7F25-45D0-8029-C99120A156DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchAutoScale.md
ms.openlocfilehash: 72ba9a2d78ab343b44267c09a7c1524cab7278a9
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761908"
---
# <span data-ttu-id="1e8c1-101">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="1e8c1-101">Enable-AzBatchAutoScale</span></span>

## <span data-ttu-id="1e8c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8c1-103">Havuzda otomatik ölçeklendirmeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-103">Enables automatic scaling of a pool.</span></span>

## <span data-ttu-id="1e8c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e8c1-104">SYNTAX</span></span>

```
Enable-AzBatchAutoScale [-Id] <String> [[-AutoScaleFormula] <String>]
 [[-AutoScaleEvaluationInterval] <TimeSpan>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e8c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8c1-106">**Enable-Azbatchotomatik ölçeklendirme** cmdlet 'i belirtilen havuzun otomatik ölçeklendirmesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-106">The **Enable-AzBatchAutoScale** cmdlet enables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="1e8c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e8c1-107">EXAMPLES</span></span>

### <span data-ttu-id="1e8c1-108">Örnek 1: havuz için otomatik ölçeklendirmeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1e8c1-108">Example 1: Enable automatic scaling for a pool</span></span>
```
PS C:\>$Formula = 'totalNodes=($CPUPercent.GetSamplePercent(TimeInterval_Minute*0,TimeInterval_Minute*10)<0.7?5:(min($CPUPercent.GetSample(TimeInterval_Minute*0, TimeInterval_Minute*10))>0.8?($CurrentDedicated*1.1):$CurrentDedicated));$TargetDedicated=min(100,totalNodes);';
PS C:\> Enable-AzBatchAutoScale -Id "MyPool" -AutoScaleFormula $Formula -BatchContext $Context
```

<span data-ttu-id="1e8c1-109">İlk komut bir formül tanımlar ve $Formula değişkenine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-109">The first command defines a formula, and then saves it to the $Formula variable.</span></span>
<span data-ttu-id="1e8c1-110">İkinci komut, $Formula formülü kullanarak MyPool adlı havuzda otomatik ölçeklendirmeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-110">The second command enables automatic scaling on the pool named MyPool using the formula in $Formula.</span></span>

## <span data-ttu-id="1e8c1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e8c1-111">PARAMETERS</span></span>

### <span data-ttu-id="1e8c1-112">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="1e8c1-112">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="1e8c1-113">Otomatik ölçeklendirme formülüne göre havuz boyutu otomatik olarak düzeltilecek kadar geçen süreyi dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-113">Specifies the amount of time (in minutes) that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="1e8c1-114">Varsayılan değer 15 dakikadır ve en az değer 5 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-114">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="1e8c1-115">-Otomatik ölçek formülü</span><span class="sxs-lookup"><span data-stu-id="1e8c1-115">-AutoScaleFormula</span></span>
<span data-ttu-id="1e8c1-116">Havuzda istenen işlem düğümlerinin formülünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-116">Specifies the formula for the desired number of compute nodes in the pool.</span></span>

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

### <span data-ttu-id="1e8c1-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1e8c1-117">-BatchContext</span></span>
<span data-ttu-id="1e8c1-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1e8c1-119">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1e8c1-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1e8c1-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1e8c1-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1e8c1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8c1-123">-DefaultProfile</span></span>
<span data-ttu-id="1e8c1-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e8c1-125">-ID</span><span class="sxs-lookup"><span data-stu-id="1e8c1-125">-Id</span></span>
<span data-ttu-id="1e8c1-126">Otomatik ölçeklendirmeyi etkinleştirmek için havuzun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-126">Specifies the object ID of the pool for which to enable automatic scaling.</span></span>

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

### <span data-ttu-id="1e8c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8c1-127">CommonParameters</span></span>
<span data-ttu-id="1e8c1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e8c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8c1-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8c1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8c1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e8c1-130">INPUTS</span></span>

### <span data-ttu-id="1e8c1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1e8c1-131">System.String</span></span>

### <span data-ttu-id="1e8c1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1e8c1-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1e8c1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e8c1-133">OUTPUTS</span></span>

### <span data-ttu-id="1e8c1-134">System. void</span><span class="sxs-lookup"><span data-stu-id="1e8c1-134">System.Void</span></span>

## <span data-ttu-id="1e8c1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e8c1-135">NOTES</span></span>

## <span data-ttu-id="1e8c1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e8c1-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e8c1-137">Disable-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="1e8c1-137">Disable-AzBatchAutoScale</span></span>](./Disable-AzBatchAutoScale.md)

[<span data-ttu-id="1e8c1-138">Test-Azbatchotomatik ölçeklendirme</span><span class="sxs-lookup"><span data-stu-id="1e8c1-138">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="1e8c1-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="1e8c1-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


