---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: c6a89a5c42daea7991711dfa0c96953856949aed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587283"
---
# <span data-ttu-id="39369-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="39369-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="39369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39369-102">SYNOPSIS</span></span>
<span data-ttu-id="39369-103">Toplu işlem düğümündeki bir hesabın özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="39369-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39369-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39369-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39369-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="39369-105">DESCRIPTION</span></span>
<span data-ttu-id="39369-106">**Set-AzureBatchComputeNodeUser** cmdlet 'ı, Azure toplu işlem düğümündeki bir kullanıcı hesabının özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="39369-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="39369-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39369-107">EXAMPLES</span></span>

### <span data-ttu-id="39369-108">Örnek 1: Kullanıcı hesabını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="39369-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="39369-109">Bu komut, ContosoPool adlı havuzda belirtilen KIMLIĞE sahip işlem düğümündeki PFuller adındaki Kullanıcı hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="39369-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="39369-110">Komut hesap parolasını ve son kullanma süresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="39369-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="39369-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39369-111">PARAMETERS</span></span>

### <span data-ttu-id="39369-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="39369-112">-BatchContext</span></span>
<span data-ttu-id="39369-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="39369-114">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="39369-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="39369-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="39369-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="39369-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="39369-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="39369-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="39369-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="39369-118">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="39369-118">-ComputeNodeId</span></span>
<span data-ttu-id="39369-119">Bu cmdlet 'in üzerinde yaptığı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39369-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39369-120">-DefaultProfile</span></span>
<span data-ttu-id="39369-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39369-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39369-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="39369-122">-ExpiryTime</span></span>
<span data-ttu-id="39369-123">Kullanıcı hesabı için son kullanma süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39369-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="39369-124">-Name</span></span>
<span data-ttu-id="39369-125">Bu cmdlet 'in değiştirdiği Kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39369-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="39369-126">-Password</span></span>
<span data-ttu-id="39369-127">Kullanıcı hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39369-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="39369-128">-PoolId</span></span>
<span data-ttu-id="39369-129">Bu cmdlet 'in üzerinde çalıştırıldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="39369-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39369-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39369-130">CommonParameters</span></span>
<span data-ttu-id="39369-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39369-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39369-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39369-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39369-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39369-133">INPUTS</span></span>

### <span data-ttu-id="39369-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="39369-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="39369-135">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="39369-135">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="39369-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39369-136">OUTPUTS</span></span>

### <span data-ttu-id="39369-137">System. void</span><span class="sxs-lookup"><span data-stu-id="39369-137">System.Void</span></span>

## <span data-ttu-id="39369-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39369-138">NOTES</span></span>

## <span data-ttu-id="39369-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39369-139">RELATED LINKS</span></span>

[<span data-ttu-id="39369-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="39369-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="39369-141">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="39369-141">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="39369-142">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="39369-142">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="39369-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="39369-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


