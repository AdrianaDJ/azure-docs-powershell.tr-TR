---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 3e52b2f3c9bddb2039b87b373d0963d51827f293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591082"
---
# <span data-ttu-id="83c64-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="83c64-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="83c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83c64-102">SYNOPSIS</span></span>
<span data-ttu-id="83c64-103">Toplu işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83c64-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83c64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83c64-104">SYNTAX</span></span>

### <span data-ttu-id="83c64-105">Kimliğe</span><span class="sxs-lookup"><span data-stu-id="83c64-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83c64-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="83c64-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83c64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83c64-107">DESCRIPTION</span></span>
<span data-ttu-id="83c64-108">**New-AzureBatchComputeNodeUser** cmdlet 'ı Azure toplu işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83c64-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="83c64-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83c64-109">EXAMPLES</span></span>

### <span data-ttu-id="83c64-110">Örnek 1: yönetici kimlik bilgilerine sahip bir kullanıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="83c64-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="83c64-111">Bu komut, ComputeNode01 KIMLIĞINE sahip işlem düğümündeki bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83c64-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="83c64-112">Düğüm, KIMLIK MyPool01 havuzunda.</span><span class="sxs-lookup"><span data-stu-id="83c64-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="83c64-113">Kullanıcı adı TestUser, parola parola, hesabın süresi yedi gün içinde dolacaktır ve hesabın yönetim kimlik bilgileri vardır.</span><span class="sxs-lookup"><span data-stu-id="83c64-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="83c64-114">Örnek 2: ardışık düzeni kullanarak işlem düğümündeki bir kullanıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="83c64-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="83c64-115">Bu komut **Get-AzureBatchComputeNode** cmdlet 'Ini kullanarak ComputeNode01 adlı COMPUTE düğümünü alır.</span><span class="sxs-lookup"><span data-stu-id="83c64-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="83c64-116">Bu düğüm KIMLIĞI MyPool01 olan havuzda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="83c64-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="83c64-117">Komut bu işlem düğümünü ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="83c64-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="83c64-118">Bu komut, Kullanıcı adı Testuserve parola parolasının bulunduğu bir kullanıcı hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="83c64-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="83c64-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83c64-119">PARAMETERS</span></span>

### <span data-ttu-id="83c64-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="83c64-120">-BatchContext</span></span>
<span data-ttu-id="83c64-121">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="83c64-122">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83c64-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="83c64-123">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="83c64-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="83c64-124">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83c64-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="83c64-125">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83c64-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="83c64-126">-ComputeNode</span></span>
<span data-ttu-id="83c64-127">Bu cmdlet 'in bir kullanıcı hesabı oluşturduğu **PSComputeNode** nesnesi olarak COMPUTE düğümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-128">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="83c64-128">-ComputeNodeId</span></span>
<span data-ttu-id="83c64-129">Bu cmdlet 'in bir kullanıcı hesabı oluşturduğu COMPUTE düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c64-130">-DefaultProfile</span></span>
<span data-ttu-id="83c64-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83c64-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="83c64-132">-ExpiryTime</span></span>
<span data-ttu-id="83c64-133">Yeni Kullanıcı hesabı için son kullanma süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-134">-Isadmin</span><span class="sxs-lookup"><span data-stu-id="83c64-134">-IsAdmin</span></span>
<span data-ttu-id="83c64-135">Cmdlet 'in yönetici kimlik bilgilerine sahip bir kullanıcı hesabı oluşturacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83c64-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="83c64-136">-Name</span></span>
<span data-ttu-id="83c64-137">Yeni yerel Windows hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-138">-Parola</span><span class="sxs-lookup"><span data-stu-id="83c64-138">-Password</span></span>
<span data-ttu-id="83c64-139">Kullanıcı hesabı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-139">Specifies the user account password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="83c64-140">-PoolId</span></span>
<span data-ttu-id="83c64-141">Kullanıcı hesabının oluşturulacağı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="83c64-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83c64-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c64-142">CommonParameters</span></span>
<span data-ttu-id="83c64-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83c64-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c64-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c64-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c64-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83c64-145">INPUTS</span></span>

### <span data-ttu-id="83c64-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="83c64-146">BatchAccountContext</span></span>
<span data-ttu-id="83c64-147">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="83c64-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="83c64-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="83c64-148">PSComputeNode</span></span>
<span data-ttu-id="83c64-149">' ComputeNode ' parametresi ardışık düzen için ' PSComputeNode ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="83c64-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="83c64-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83c64-150">OUTPUTS</span></span>

## <span data-ttu-id="83c64-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83c64-151">NOTES</span></span>

## <span data-ttu-id="83c64-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83c64-152">RELATED LINKS</span></span>

[<span data-ttu-id="83c64-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="83c64-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="83c64-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="83c64-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="83c64-155">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="83c64-155">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="83c64-156">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="83c64-156">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


