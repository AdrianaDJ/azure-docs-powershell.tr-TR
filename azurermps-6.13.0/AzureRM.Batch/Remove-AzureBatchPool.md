---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 4cfb497b98d20b5cf3741c90934e9e104b93ddcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587296"
---
# <span data-ttu-id="70c8c-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="70c8c-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="70c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="70c8c-103">Belirtilen toplu havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="70c8c-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70c8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70c8c-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c8c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70c8c-105">DESCRIPTION</span></span>
<span data-ttu-id="70c8c-106">**Remove-AzureBatchPool** cmdlet 'ı belirtilen Azure toplu iş havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="70c8c-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="70c8c-107">*Force* parametresini kullanmazsanız onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="70c8c-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="70c8c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70c8c-108">EXAMPLES</span></span>

### <span data-ttu-id="70c8c-109">Örnek 1: havuz KIMLIĞINE göre bir toplu Iş havuzu silme</span><span class="sxs-lookup"><span data-stu-id="70c8c-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="70c8c-110">Bu komut MyPool KIMLIKLI havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="70c8c-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="70c8c-111">Silme işlemi gerçekleşmeden önce kullanıcıdan onay istenir.</span><span class="sxs-lookup"><span data-stu-id="70c8c-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="70c8c-112">Örnek 2: zorunlu olarak tüm toplu Iş havuzlarını silme</span><span class="sxs-lookup"><span data-stu-id="70c8c-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="70c8c-113">Bu komut tüm toplu Iş havuzlarını siler.</span><span class="sxs-lookup"><span data-stu-id="70c8c-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="70c8c-114">*Force* parametresi bulunduğundan, onay istemi bastırılır.</span><span class="sxs-lookup"><span data-stu-id="70c8c-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="70c8c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70c8c-115">PARAMETERS</span></span>

### <span data-ttu-id="70c8c-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="70c8c-116">-BatchContext</span></span>
<span data-ttu-id="70c8c-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c8c-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="70c8c-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70c8c-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="70c8c-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="70c8c-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="70c8c-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70c8c-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="70c8c-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="70c8c-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="70c8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c8c-122">-DefaultProfile</span></span>
<span data-ttu-id="70c8c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70c8c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70c8c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="70c8c-124">-Force</span></span>
<span data-ttu-id="70c8c-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="70c8c-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70c8c-126">-ID</span><span class="sxs-lookup"><span data-stu-id="70c8c-126">-Id</span></span>
<span data-ttu-id="70c8c-127">Silinecek havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="70c8c-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="70c8c-128">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="70c8c-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="70c8c-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="70c8c-129">-Confirm</span></span>
<span data-ttu-id="70c8c-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70c8c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c8c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c8c-131">-WhatIf</span></span>
<span data-ttu-id="70c8c-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70c8c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c8c-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70c8c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c8c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c8c-134">CommonParameters</span></span>
<span data-ttu-id="70c8c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70c8c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c8c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c8c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c8c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70c8c-137">INPUTS</span></span>

### <span data-ttu-id="70c8c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="70c8c-138">System.String</span></span>

### <span data-ttu-id="70c8c-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="70c8c-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="70c8c-140">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="70c8c-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="70c8c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70c8c-141">OUTPUTS</span></span>

### <span data-ttu-id="70c8c-142">System. void</span><span class="sxs-lookup"><span data-stu-id="70c8c-142">System.Void</span></span>

## <span data-ttu-id="70c8c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70c8c-143">NOTES</span></span>

## <span data-ttu-id="70c8c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70c8c-144">RELATED LINKS</span></span>

[<span data-ttu-id="70c8c-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="70c8c-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="70c8c-146">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="70c8c-146">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="70c8c-147">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="70c8c-147">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="70c8c-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="70c8c-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


