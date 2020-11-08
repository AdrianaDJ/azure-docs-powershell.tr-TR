---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275991"
---
# <span data-ttu-id="57606-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="57606-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="57606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57606-102">SYNOPSIS</span></span>
<span data-ttu-id="57606-103">Toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="57606-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="57606-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57606-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57606-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57606-105">DESCRIPTION</span></span>
<span data-ttu-id="57606-106">**Disable-Azbatchjobzamanlama** cmdlet 'ı bir Azure toplu iş çizelgesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="57606-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="57606-107">Bir zamanlamayı devre dışı bırakırsanız, işler bu zamanlamaya göre oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="57606-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="57606-108">Devre dışı bir zamanlamayı daha sonra etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57606-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="57606-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57606-109">EXAMPLES</span></span>

### <span data-ttu-id="57606-110">Örnek 1: iş çizelgesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="57606-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="57606-111">Bu komut, KIMLIĞI JobSchedule17 olan iş zamanlamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="57606-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="57606-112">$Context değişkenine bağlam atamak için **Get-AzBatchAccountKey** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="57606-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="57606-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57606-113">PARAMETERS</span></span>

### <span data-ttu-id="57606-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="57606-114">-BatchContext</span></span>
<span data-ttu-id="57606-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57606-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="57606-116">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57606-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="57606-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="57606-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="57606-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57606-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="57606-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="57606-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="57606-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57606-120">-DefaultProfile</span></span>
<span data-ttu-id="57606-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57606-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57606-122">-ID</span><span class="sxs-lookup"><span data-stu-id="57606-122">-Id</span></span>
<span data-ttu-id="57606-123">Bu cmdlet 'in devre dışı olduğu iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="57606-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="57606-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57606-124">CommonParameters</span></span>
<span data-ttu-id="57606-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57606-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57606-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="57606-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57606-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57606-127">INPUTS</span></span>

### <span data-ttu-id="57606-128">System. String</span><span class="sxs-lookup"><span data-stu-id="57606-128">System.String</span></span>

### <span data-ttu-id="57606-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="57606-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="57606-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57606-130">OUTPUTS</span></span>

### <span data-ttu-id="57606-131">System. void</span><span class="sxs-lookup"><span data-stu-id="57606-131">System.Void</span></span>

## <span data-ttu-id="57606-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57606-132">NOTES</span></span>

## <span data-ttu-id="57606-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57606-133">RELATED LINKS</span></span>

[<span data-ttu-id="57606-134">Enable-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="57606-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="57606-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="57606-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="57606-136">Get-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="57606-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="57606-137">Yeni-Azbatchjobplanlama</span><span class="sxs-lookup"><span data-stu-id="57606-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="57606-138">Remove-Azbatchjobplan</span><span class="sxs-lookup"><span data-stu-id="57606-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="57606-139">Stop-Azbatchjobzamanlama</span><span class="sxs-lookup"><span data-stu-id="57606-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="57606-140">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="57606-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
