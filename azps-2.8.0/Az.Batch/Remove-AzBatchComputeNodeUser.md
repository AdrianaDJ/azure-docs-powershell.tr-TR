---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938642"
---
# <span data-ttu-id="f14f9-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="f14f9-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="f14f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f14f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f14f9-103">Bir toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="f14f9-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="f14f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f14f9-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f14f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f14f9-105">DESCRIPTION</span></span>
<span data-ttu-id="f14f9-106">**Remove-AzBatchComputeNodeUser** cmdlet 'ı bir Azure toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="f14f9-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="f14f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f14f9-107">EXAMPLES</span></span>

### <span data-ttu-id="f14f9-108">Örnek 1: onay olmadan bir kullanıcıyı işlem düğümünden silme</span><span class="sxs-lookup"><span data-stu-id="f14f9-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="f14f9-109">Bu komut, ComputeNode01 adlı COMPUTE düğümünden User14 adındaki kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="f14f9-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="f14f9-110">Compute düğümü Pool01 adlı havuzda.</span><span class="sxs-lookup"><span data-stu-id="f14f9-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="f14f9-111">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f14f9-112">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="f14f9-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f14f9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f14f9-113">PARAMETERS</span></span>

### <span data-ttu-id="f14f9-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f14f9-114">-BatchContext</span></span>
<span data-ttu-id="f14f9-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f14f9-116">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f14f9-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f14f9-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="f14f9-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f14f9-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f14f9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f14f9-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f14f9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f14f9-120">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="f14f9-120">-ComputeNodeId</span></span>
<span data-ttu-id="f14f9-121">Bu cmdlet 'in Kullanıcı hesabını sildiği COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14f9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14f9-122">-DefaultProfile</span></span>
<span data-ttu-id="f14f9-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f14f9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14f9-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f14f9-124">-Name</span></span>
<span data-ttu-id="f14f9-125">Silinecek kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="f14f9-126">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="f14f9-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f14f9-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="f14f9-127">-PoolId</span></span>
<span data-ttu-id="f14f9-128">Kullanıcı hesabının silineceği COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="f14f9-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="f14f9-129">-Confirm</span></span>
<span data-ttu-id="f14f9-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f14f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f14f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14f9-131">-WhatIf</span></span>
<span data-ttu-id="f14f9-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f14f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14f9-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f14f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14f9-134">CommonParameters</span></span>
<span data-ttu-id="f14f9-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f14f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f14f9-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14f9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14f9-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f14f9-137">INPUTS</span></span>

### <span data-ttu-id="f14f9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f14f9-138">System.String</span></span>

### <span data-ttu-id="f14f9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f14f9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f14f9-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f14f9-140">OUTPUTS</span></span>

### <span data-ttu-id="f14f9-141">System. void</span><span class="sxs-lookup"><span data-stu-id="f14f9-141">System.Void</span></span>

## <span data-ttu-id="f14f9-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f14f9-142">NOTES</span></span>

## <span data-ttu-id="f14f9-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f14f9-143">RELATED LINKS</span></span>

[<span data-ttu-id="f14f9-144">Yeni-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="f14f9-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="f14f9-145">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="f14f9-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f14f9-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="f14f9-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


