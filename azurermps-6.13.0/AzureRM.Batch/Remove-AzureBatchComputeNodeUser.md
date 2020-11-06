---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: e4ca1d8fe8db34579a8442ed77ce70d320947a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591405"
---
# <span data-ttu-id="bea45-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="bea45-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="bea45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea45-102">SYNOPSIS</span></span>
<span data-ttu-id="bea45-103">Bir toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="bea45-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bea45-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bea45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bea45-105">DESCRIPTION</span></span>
<span data-ttu-id="bea45-106">**Remove-AzureBatchComputeNodeUser** cmdlet 'ı bir Azure toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="bea45-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="bea45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bea45-107">EXAMPLES</span></span>

### <span data-ttu-id="bea45-108">Örnek 1: onay olmadan bir kullanıcıyı işlem düğümünden silme</span><span class="sxs-lookup"><span data-stu-id="bea45-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="bea45-109">Bu komut, ComputeNode01 adlı COMPUTE düğümünden User14 adındaki kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="bea45-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="bea45-110">Compute düğümü Pool01 adlı havuzda.</span><span class="sxs-lookup"><span data-stu-id="bea45-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="bea45-111">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bea45-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="bea45-112">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="bea45-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bea45-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bea45-113">PARAMETERS</span></span>

### <span data-ttu-id="bea45-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bea45-114">-BatchContext</span></span>
<span data-ttu-id="bea45-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bea45-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bea45-116">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bea45-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bea45-117">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="bea45-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bea45-118">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bea45-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bea45-119">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bea45-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bea45-120">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="bea45-120">-ComputeNodeId</span></span>
<span data-ttu-id="bea45-121">Bu cmdlet 'in Kullanıcı hesabını sildiği COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bea45-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="bea45-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea45-122">-DefaultProfile</span></span>
<span data-ttu-id="bea45-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bea45-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bea45-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="bea45-124">-Name</span></span>
<span data-ttu-id="bea45-125">Silinecek kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bea45-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="bea45-126">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea45-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="bea45-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="bea45-127">-PoolId</span></span>
<span data-ttu-id="bea45-128">Kullanıcı hesabının silineceği COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bea45-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="bea45-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bea45-129">-Confirm</span></span>
<span data-ttu-id="bea45-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bea45-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea45-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea45-131">-WhatIf</span></span>
<span data-ttu-id="bea45-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bea45-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bea45-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bea45-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea45-134">CommonParameters</span></span>
<span data-ttu-id="bea45-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bea45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea45-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea45-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea45-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bea45-137">INPUTS</span></span>

### <span data-ttu-id="bea45-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bea45-138">System.String</span></span>

### <span data-ttu-id="bea45-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bea45-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="bea45-140">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bea45-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="bea45-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bea45-141">OUTPUTS</span></span>

### <span data-ttu-id="bea45-142">System. void</span><span class="sxs-lookup"><span data-stu-id="bea45-142">System.Void</span></span>

## <span data-ttu-id="bea45-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bea45-143">NOTES</span></span>

## <span data-ttu-id="bea45-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bea45-144">RELATED LINKS</span></span>

[<span data-ttu-id="bea45-145">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="bea45-145">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="bea45-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bea45-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bea45-147">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="bea45-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


