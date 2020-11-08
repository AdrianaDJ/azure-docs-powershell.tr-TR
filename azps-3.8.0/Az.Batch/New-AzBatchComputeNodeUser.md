---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 1aedf08bf6a9248b9cd3654471240a45b67ee893
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107258"
---
# <span data-ttu-id="30d4f-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="30d4f-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="30d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="30d4f-103">Toplu işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d4f-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="30d4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30d4f-104">SYNTAX</span></span>

### <span data-ttu-id="30d4f-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="30d4f-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30d4f-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="30d4f-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30d4f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="30d4f-107">DESCRIPTION</span></span>
<span data-ttu-id="30d4f-108">**New-AzBatchComputeNodeUser** cmdlet 'ı Azure toplu işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d4f-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="30d4f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30d4f-109">EXAMPLES</span></span>

### <span data-ttu-id="30d4f-110">Örnek 1: yönetici kimlik bilgilerine sahip bir kullanıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="30d4f-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="30d4f-111">Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d4f-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="30d4f-112">Düğüm, KIMLIK MyPool01 havuzunda.</span><span class="sxs-lookup"><span data-stu-id="30d4f-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="30d4f-113">Kullanıcı adı TestUser, parola parola, hesabın süresi yedi gün içinde dolacaktır ve hesabın yönetim kimlik bilgileri vardır.</span><span class="sxs-lookup"><span data-stu-id="30d4f-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="30d4f-114">Örnek 2: ardışık düzeni kullanarak işlem düğümündeki bir kullanıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="30d4f-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="30d4f-115">Bu komut **Get-AzBatchComputeNode** cmdlet 'Ini kullanarak ComputeNode01 adlı COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="30d4f-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="30d4f-116">Bu düğüm KIMLIĞI MyPool01 olan havuzda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="30d4f-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="30d4f-117">Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="30d4f-118">Bu komut Kullanıcı adı TestUser ve parola parolasına sahip bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="30d4f-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="30d4f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30d4f-119">PARAMETERS</span></span>

### <span data-ttu-id="30d4f-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="30d4f-120">-BatchContext</span></span>
<span data-ttu-id="30d4f-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30d4f-122">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30d4f-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30d4f-123">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="30d4f-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30d4f-124">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30d4f-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30d4f-125">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="30d4f-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="30d4f-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="30d4f-126">-ComputeNode</span></span>
<span data-ttu-id="30d4f-127">Bu cmdlet 'in bir kullanıcı hesabı oluşturduğu **PSComputeNode** nesnesi olarak COMPUTE düğümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-128">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="30d4f-128">-ComputeNodeId</span></span>
<span data-ttu-id="30d4f-129">Bu cmdlet 'in bir kullanıcı hesabı oluşturduğu COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d4f-130">-DefaultProfile</span></span>
<span data-ttu-id="30d4f-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30d4f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d4f-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="30d4f-132">-ExpiryTime</span></span>
<span data-ttu-id="30d4f-133">Yeni Kullanıcı hesabı için son kullanma süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="30d4f-134">-Isadmin</span><span class="sxs-lookup"><span data-stu-id="30d4f-134">-IsAdmin</span></span>
<span data-ttu-id="30d4f-135">Cmdlet 'in yönetici kimlik bilgilerine sahip bir kullanıcı hesabı oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="30d4f-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="30d4f-136">-Name</span></span>
<span data-ttu-id="30d4f-137">Yeni yerel Windows hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-138">-Parola</span><span class="sxs-lookup"><span data-stu-id="30d4f-138">-Password</span></span>
<span data-ttu-id="30d4f-139">Kullanıcı hesabı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="30d4f-140">-PoolId</span></span>
<span data-ttu-id="30d4f-141">Kullanıcı hesabının oluşturulacağı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="30d4f-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d4f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d4f-142">CommonParameters</span></span>
<span data-ttu-id="30d4f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30d4f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d4f-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30d4f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d4f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30d4f-145">INPUTS</span></span>

### <span data-ttu-id="30d4f-146">Microsoft.Azure.Commands.Batch. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="30d4f-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="30d4f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="30d4f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30d4f-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30d4f-148">OUTPUTS</span></span>

### <span data-ttu-id="30d4f-149">System. void</span><span class="sxs-lookup"><span data-stu-id="30d4f-149">System.Void</span></span>

## <span data-ttu-id="30d4f-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30d4f-150">NOTES</span></span>

## <span data-ttu-id="30d4f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30d4f-151">RELATED LINKS</span></span>

[<span data-ttu-id="30d4f-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="30d4f-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="30d4f-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="30d4f-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="30d4f-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="30d4f-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="30d4f-155">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="30d4f-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


