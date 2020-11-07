---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591137"
---
# <span data-ttu-id="4fea3-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea3-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="4fea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fea3-102">SYNOPSIS</span></span>
<span data-ttu-id="4fea3-103">Belirtilen toplu havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="4fea3-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fea3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fea3-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fea3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fea3-105">DESCRIPTION</span></span>
<span data-ttu-id="4fea3-106">**Remove-AzureBatchPool** cmdlet 'ı belirtilen Azure toplu iş havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="4fea3-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="4fea3-107">*Force* parametresini kullanmazsanız onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="4fea3-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="4fea3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fea3-108">EXAMPLES</span></span>

### <span data-ttu-id="4fea3-109">Örnek 1: havuz KIMLIĞINE göre bir toplu Iş havuzu silme</span><span class="sxs-lookup"><span data-stu-id="4fea3-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="4fea3-110">Bu komut MyPool KIMLIKLI havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="4fea3-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="4fea3-111">Silme işlemi gerçekleşmeden önce kullanıcıdan onay istenir.</span><span class="sxs-lookup"><span data-stu-id="4fea3-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="4fea3-112">Örnek 2: zorunlu olarak tüm toplu Iş havuzlarını silme</span><span class="sxs-lookup"><span data-stu-id="4fea3-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="4fea3-113">Bu komut tüm toplu Iş havuzlarını siler.</span><span class="sxs-lookup"><span data-stu-id="4fea3-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="4fea3-114">*Force* parametresi bulunduğundan, onay istemi bastırılır.</span><span class="sxs-lookup"><span data-stu-id="4fea3-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="4fea3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fea3-115">PARAMETERS</span></span>

### <span data-ttu-id="4fea3-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4fea3-116">-BatchContext</span></span>
<span data-ttu-id="4fea3-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fea3-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4fea3-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4fea3-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4fea3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4fea3-119">-Force</span></span>
<span data-ttu-id="4fea3-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4fea3-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4fea3-121">-Id</span></span>
<span data-ttu-id="4fea3-122">Silinecek havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fea3-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="4fea3-123">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4fea3-123">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fea3-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fea3-124">-Confirm</span></span>
<span data-ttu-id="4fea3-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fea3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fea3-126">-WhatIf</span></span>
<span data-ttu-id="4fea3-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fea3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fea3-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fea3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fea3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fea3-129">-DefaultProfile</span></span>
<span data-ttu-id="4fea3-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fea3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fea3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fea3-131">CommonParameters</span></span>
<span data-ttu-id="4fea3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fea3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fea3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fea3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fea3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fea3-134">INPUTS</span></span>

### <span data-ttu-id="4fea3-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4fea3-135">BatchAccountContext</span></span>
<span data-ttu-id="4fea3-136">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4fea3-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4fea3-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fea3-137">OUTPUTS</span></span>

## <span data-ttu-id="4fea3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fea3-138">NOTES</span></span>

## <span data-ttu-id="4fea3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fea3-139">RELATED LINKS</span></span>

[<span data-ttu-id="4fea3-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4fea3-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4fea3-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea3-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="4fea3-142">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="4fea3-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="4fea3-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4fea3-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

