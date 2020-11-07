---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: be9b7d5ed8f5f26e31c04f96e14d14573fd0a0f0
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761835"
---
# <span data-ttu-id="07c14-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="07c14-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="07c14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07c14-102">SYNOPSIS</span></span>
<span data-ttu-id="07c14-103">Belirtilen toplu havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="07c14-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="07c14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07c14-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07c14-105">DESCRIPTION</span></span>
<span data-ttu-id="07c14-106">**Remove-AzBatchPool** cmdlet 'ı belirtilen Azure toplu iş havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="07c14-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="07c14-107">*Force* parametresini kullanmazsanız onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="07c14-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="07c14-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07c14-108">EXAMPLES</span></span>

### <span data-ttu-id="07c14-109">Örnek 1: havuz KIMLIĞINE göre bir toplu Iş havuzu silme</span><span class="sxs-lookup"><span data-stu-id="07c14-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="07c14-110">Bu komut MyPool KIMLIKLI havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="07c14-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="07c14-111">Silme işlemi gerçekleşmeden önce kullanıcıdan onay istenir.</span><span class="sxs-lookup"><span data-stu-id="07c14-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="07c14-112">Örnek 2: zorunlu olarak tüm toplu Iş havuzlarını silme</span><span class="sxs-lookup"><span data-stu-id="07c14-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="07c14-113">Bu komut tüm toplu Iş havuzlarını siler.</span><span class="sxs-lookup"><span data-stu-id="07c14-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="07c14-114">*Force* parametresi bulunduğundan, onay istemi bastırılır.</span><span class="sxs-lookup"><span data-stu-id="07c14-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="07c14-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07c14-115">PARAMETERS</span></span>

### <span data-ttu-id="07c14-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="07c14-116">-BatchContext</span></span>
<span data-ttu-id="07c14-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07c14-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="07c14-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07c14-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="07c14-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="07c14-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="07c14-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07c14-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="07c14-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="07c14-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="07c14-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c14-122">-DefaultProfile</span></span>
<span data-ttu-id="07c14-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07c14-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c14-124">-Force</span><span class="sxs-lookup"><span data-stu-id="07c14-124">-Force</span></span>
<span data-ttu-id="07c14-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="07c14-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07c14-126">-ID</span><span class="sxs-lookup"><span data-stu-id="07c14-126">-Id</span></span>
<span data-ttu-id="07c14-127">Silinecek havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="07c14-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="07c14-128">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="07c14-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="07c14-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="07c14-129">-Confirm</span></span>
<span data-ttu-id="07c14-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="07c14-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c14-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c14-131">-WhatIf</span></span>
<span data-ttu-id="07c14-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="07c14-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07c14-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="07c14-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c14-134">CommonParameters</span></span>
<span data-ttu-id="07c14-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07c14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c14-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c14-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c14-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07c14-137">INPUTS</span></span>

### <span data-ttu-id="07c14-138">System. String</span><span class="sxs-lookup"><span data-stu-id="07c14-138">System.String</span></span>

### <span data-ttu-id="07c14-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="07c14-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="07c14-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07c14-140">OUTPUTS</span></span>

### <span data-ttu-id="07c14-141">System. void</span><span class="sxs-lookup"><span data-stu-id="07c14-141">System.Void</span></span>

## <span data-ttu-id="07c14-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07c14-142">NOTES</span></span>

## <span data-ttu-id="07c14-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07c14-143">RELATED LINKS</span></span>

[<span data-ttu-id="07c14-144">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="07c14-144">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="07c14-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="07c14-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="07c14-146">Yeni-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="07c14-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="07c14-147">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="07c14-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


