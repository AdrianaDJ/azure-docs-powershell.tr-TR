---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323425"
---
# <span data-ttu-id="85db2-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85db2-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="85db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85db2-102">SYNOPSIS</span></span>
<span data-ttu-id="85db2-103">Belirtilen toplu havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="85db2-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="85db2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85db2-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85db2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85db2-105">DESCRIPTION</span></span>
<span data-ttu-id="85db2-106">**Remove-AzBatchPool** cmdlet 'ı belirtilen Azure toplu iş havuzunu siler.</span><span class="sxs-lookup"><span data-stu-id="85db2-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="85db2-107">*Force* parametresini kullanmazsanız onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="85db2-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="85db2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85db2-108">EXAMPLES</span></span>

### <span data-ttu-id="85db2-109">Örnek 1: havuz KIMLIĞINE göre bir toplu Iş havuzu silme</span><span class="sxs-lookup"><span data-stu-id="85db2-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="85db2-110">Bu komut MyPool KIMLIKLI havuzu siler.</span><span class="sxs-lookup"><span data-stu-id="85db2-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="85db2-111">Silme işlemi gerçekleşmeden önce kullanıcıdan onay istenir.</span><span class="sxs-lookup"><span data-stu-id="85db2-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="85db2-112">Örnek 2: zorunlu olarak tüm toplu Iş havuzlarını silme</span><span class="sxs-lookup"><span data-stu-id="85db2-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="85db2-113">Bu komut tüm toplu Iş havuzlarını siler.</span><span class="sxs-lookup"><span data-stu-id="85db2-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="85db2-114">*Force* parametresi bulunduğundan, onay istemi bastırılır.</span><span class="sxs-lookup"><span data-stu-id="85db2-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="85db2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85db2-115">PARAMETERS</span></span>

### <span data-ttu-id="85db2-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="85db2-116">-BatchContext</span></span>
<span data-ttu-id="85db2-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="85db2-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="85db2-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="85db2-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="85db2-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="85db2-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="85db2-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="85db2-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="85db2-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="85db2-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="85db2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85db2-122">-DefaultProfile</span></span>
<span data-ttu-id="85db2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="85db2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85db2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="85db2-124">-Force</span></span>
<span data-ttu-id="85db2-125">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="85db2-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="85db2-126">-ID</span><span class="sxs-lookup"><span data-stu-id="85db2-126">-Id</span></span>
<span data-ttu-id="85db2-127">Silinecek havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="85db2-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="85db2-128">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="85db2-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="85db2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="85db2-129">-Confirm</span></span>
<span data-ttu-id="85db2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="85db2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85db2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85db2-131">-WhatIf</span></span>
<span data-ttu-id="85db2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="85db2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85db2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="85db2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85db2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85db2-134">CommonParameters</span></span>
<span data-ttu-id="85db2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85db2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85db2-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="85db2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85db2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85db2-137">INPUTS</span></span>

### <span data-ttu-id="85db2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="85db2-138">System.String</span></span>

### <span data-ttu-id="85db2-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85db2-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="85db2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85db2-140">OUTPUTS</span></span>

### <span data-ttu-id="85db2-141">System. void</span><span class="sxs-lookup"><span data-stu-id="85db2-141">System.Void</span></span>

## <span data-ttu-id="85db2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85db2-142">NOTES</span></span>

## <span data-ttu-id="85db2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85db2-143">RELATED LINKS</span></span>

[<span data-ttu-id="85db2-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="85db2-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="85db2-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85db2-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="85db2-146">Yeni-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="85db2-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="85db2-147">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="85db2-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
