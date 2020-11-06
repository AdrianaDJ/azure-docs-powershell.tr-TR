---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589899"
---
# <span data-ttu-id="fdf49-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="fdf49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdf49-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf49-103">Toplu iş çizelgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdf49-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fdf49-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf49-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fdf49-105">DESCRIPTION</span></span>
<span data-ttu-id="fdf49-106">**Remove-AzureBatchJobSchedule** cmdlet 'ı bir Azure toplu iş çizelgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fdf49-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="fdf49-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fdf49-107">EXAMPLES</span></span>

## <span data-ttu-id="fdf49-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fdf49-108">PARAMETERS</span></span>

### <span data-ttu-id="fdf49-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fdf49-109">-BatchContext</span></span>
<span data-ttu-id="fdf49-110">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdf49-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fdf49-111">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fdf49-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="fdf49-112">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="fdf49-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="fdf49-113">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fdf49-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="fdf49-114">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fdf49-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="fdf49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf49-115">-DefaultProfile</span></span>
<span data-ttu-id="fdf49-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fdf49-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf49-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fdf49-117">-Force</span></span>
<span data-ttu-id="fdf49-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fdf49-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf49-119">-ID</span><span class="sxs-lookup"><span data-stu-id="fdf49-119">-Id</span></span>
<span data-ttu-id="fdf49-120">Kaldırılacak iş zamanlamasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fdf49-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdf49-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="fdf49-121">-Confirm</span></span>
<span data-ttu-id="fdf49-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fdf49-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf49-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf49-123">-WhatIf</span></span>
<span data-ttu-id="fdf49-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fdf49-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdf49-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fdf49-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf49-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf49-126">CommonParameters</span></span>
<span data-ttu-id="fdf49-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fdf49-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf49-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf49-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf49-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fdf49-129">INPUTS</span></span>

### <span data-ttu-id="fdf49-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fdf49-130">BatchAccountContext</span></span>
<span data-ttu-id="fdf49-131">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fdf49-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="fdf49-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fdf49-132">OUTPUTS</span></span>

## <span data-ttu-id="fdf49-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fdf49-133">NOTES</span></span>

## <span data-ttu-id="fdf49-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fdf49-134">RELATED LINKS</span></span>

[<span data-ttu-id="fdf49-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fdf49-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="fdf49-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="fdf49-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="fdf49-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="fdf49-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="fdf49-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


