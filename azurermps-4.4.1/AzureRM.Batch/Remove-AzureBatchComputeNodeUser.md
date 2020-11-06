---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593172"
---
# <span data-ttu-id="6bd9a-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="6bd9a-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="6bd9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd9a-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd9a-103">Bir toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6bd9a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bd9a-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd9a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bd9a-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd9a-106">**Remove-AzureBatchComputeNodeUser** cmdlet 'ı bir Azure toplu işlem düğümünden Kullanıcı hesabını siler.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="6bd9a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bd9a-107">EXAMPLES</span></span>

### <span data-ttu-id="6bd9a-108">Örnek 1: onay olmadan bir kullanıcıyı işlem düğümünden silme</span><span class="sxs-lookup"><span data-stu-id="6bd9a-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="6bd9a-109">Bu komut, ComputeNode01 adlı COMPUTE düğümünden User14 adındaki kullanıcıyı siler.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="6bd9a-110">Compute düğümü Pool01 adlı havuzda.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="6bd9a-111">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="6bd9a-112">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6bd9a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bd9a-113">PARAMETERS</span></span>

### <span data-ttu-id="6bd9a-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6bd9a-114">-BatchContext</span></span>
<span data-ttu-id="6bd9a-115">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6bd9a-116">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="6bd9a-117">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="6bd9a-117">-ComputeNodeId</span></span>
<span data-ttu-id="6bd9a-118">Bu cmdlet 'in Kullanıcı hesabını sildiği COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="6bd9a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bd9a-119">-Name</span></span>
<span data-ttu-id="6bd9a-120">Silinecek kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="6bd9a-121">Joker karakterler belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-121">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="6bd9a-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="6bd9a-122">-PoolId</span></span>
<span data-ttu-id="6bd9a-123">Kullanıcı hesabının silineceği COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="6bd9a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bd9a-124">-Confirm</span></span>
<span data-ttu-id="6bd9a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bd9a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bd9a-126">-WhatIf</span></span>
<span data-ttu-id="6bd9a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bd9a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bd9a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd9a-129">-DefaultProfile</span></span>
<span data-ttu-id="6bd9a-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6bd9a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd9a-131">CommonParameters</span></span>
<span data-ttu-id="6bd9a-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bd9a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd9a-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd9a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd9a-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bd9a-134">INPUTS</span></span>

### <span data-ttu-id="6bd9a-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6bd9a-135">BatchAccountContext</span></span>
<span data-ttu-id="6bd9a-136">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6bd9a-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="6bd9a-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bd9a-137">OUTPUTS</span></span>

## <span data-ttu-id="6bd9a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bd9a-138">NOTES</span></span>

## <span data-ttu-id="6bd9a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bd9a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6bd9a-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="6bd9a-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="6bd9a-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="6bd9a-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="6bd9a-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6bd9a-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


