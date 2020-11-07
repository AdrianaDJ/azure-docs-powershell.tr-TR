---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761905"
---
# <span data-ttu-id="06c5b-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="06c5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="06c5b-103">Toplu işi etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="06c5b-103">Enables a Batch job.</span></span>

## <span data-ttu-id="06c5b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06c5b-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06c5b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="06c5b-106">**Enable-AzBatchJob** cmdlet 'ı Azure toplu işine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="06c5b-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="06c5b-107">İşi etkinleştirdikten sonra yeni görevler çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="06c5b-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="06c5b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06c5b-108">EXAMPLES</span></span>

### <span data-ttu-id="06c5b-109">Örnek 1: bir toplu işi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="06c5b-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="06c5b-110">Bu komut, Iş-000001 KIMLIĞINE sahip işi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="06c5b-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="06c5b-111">$Context değişkenine bağlam atamak için Get-AzBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="06c5b-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="06c5b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06c5b-112">PARAMETERS</span></span>

### <span data-ttu-id="06c5b-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="06c5b-113">-BatchContext</span></span>
<span data-ttu-id="06c5b-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06c5b-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="06c5b-115">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06c5b-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="06c5b-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="06c5b-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="06c5b-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="06c5b-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="06c5b-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06c5b-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="06c5b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c5b-119">-DefaultProfile</span></span>
<span data-ttu-id="06c5b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06c5b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c5b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="06c5b-121">-Id</span></span>
<span data-ttu-id="06c5b-122">Bu cmdlet 'in etkinleştirmesine iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="06c5b-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="06c5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c5b-123">CommonParameters</span></span>
<span data-ttu-id="06c5b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06c5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c5b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06c5b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c5b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06c5b-126">INPUTS</span></span>

### <span data-ttu-id="06c5b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06c5b-127">System.String</span></span>

### <span data-ttu-id="06c5b-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="06c5b-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="06c5b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06c5b-129">OUTPUTS</span></span>

### <span data-ttu-id="06c5b-130">System. void</span><span class="sxs-lookup"><span data-stu-id="06c5b-130">System.Void</span></span>

## <span data-ttu-id="06c5b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06c5b-131">NOTES</span></span>

## <span data-ttu-id="06c5b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06c5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="06c5b-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="06c5b-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="06c5b-135">Yeni-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="06c5b-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="06c5b-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="06c5b-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="06c5b-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="06c5b-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


