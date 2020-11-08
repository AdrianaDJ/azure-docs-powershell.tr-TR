---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: 95530c75575742e848f39861bed1710be75e318c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938711"
---
# <span data-ttu-id="5cc34-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="5cc34-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="5cc34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc34-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc34-103">Toplu işlem düğümündeki bir hesabın özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="5cc34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cc34-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cc34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cc34-105">DESCRIPTION</span></span>
<span data-ttu-id="5cc34-106">**Set-AzBatchComputeNodeUser** cmdlet 'i, bir Azure toplu işlem düğümündeki Kullanıcı hesabının özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="5cc34-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cc34-107">EXAMPLES</span></span>

### <span data-ttu-id="5cc34-108">Örnek 1: Kullanıcı hesabını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5cc34-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="5cc34-109">Bu komut, ContosoPool adlı havuzda belirtilen KIMLIĞE sahip işlem düğümündeki PFuller adındaki Kullanıcı hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="5cc34-110">Komut hesap parolasını ve son kullanma süresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="5cc34-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cc34-111">PARAMETERS</span></span>

### <span data-ttu-id="5cc34-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5cc34-112">-BatchContext</span></span>
<span data-ttu-id="5cc34-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5cc34-114">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cc34-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5cc34-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="5cc34-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5cc34-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5cc34-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5cc34-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5cc34-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5cc34-118">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="5cc34-118">-ComputeNodeId</span></span>
<span data-ttu-id="5cc34-119">Bu cmdlet 'in üzerinde yaptığı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5cc34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc34-120">-DefaultProfile</span></span>
<span data-ttu-id="5cc34-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cc34-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cc34-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5cc34-122">-ExpiryTime</span></span>
<span data-ttu-id="5cc34-123">Kullanıcı hesabı için son kullanma süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="5cc34-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cc34-124">-Name</span></span>
<span data-ttu-id="5cc34-125">Bu cmdlet 'in değiştirdiği Kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5cc34-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="5cc34-126">-Password</span></span>
<span data-ttu-id="5cc34-127">Kullanıcı hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="5cc34-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="5cc34-128">-PoolId</span></span>
<span data-ttu-id="5cc34-129">Bu cmdlet 'in üzerinde çalıştırıldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cc34-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5cc34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc34-130">CommonParameters</span></span>
<span data-ttu-id="5cc34-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cc34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc34-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc34-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc34-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cc34-133">INPUTS</span></span>

### <span data-ttu-id="5cc34-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5cc34-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5cc34-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cc34-135">OUTPUTS</span></span>

### <span data-ttu-id="5cc34-136">System. void</span><span class="sxs-lookup"><span data-stu-id="5cc34-136">System.Void</span></span>

## <span data-ttu-id="5cc34-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cc34-137">NOTES</span></span>

## <span data-ttu-id="5cc34-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cc34-138">RELATED LINKS</span></span>

[<span data-ttu-id="5cc34-139">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="5cc34-139">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5cc34-140">Yeni-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="5cc34-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="5cc34-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="5cc34-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="5cc34-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="5cc34-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

