---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6fb398e44b2e6de8a0d00e9a8d737916fafa2472
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764721"
---
# <span data-ttu-id="c2e25-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c2e25-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="c2e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e25-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e25-103">Toplu işlem düğümündeki bir hesabın özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2e25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2e25-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2e25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2e25-105">DESCRIPTION</span></span>
<span data-ttu-id="c2e25-106">**Set-AzureBatchComputeNodeUser** cmdlet 'ı, Azure toplu işlem düğümündeki bir kullanıcı hesabının özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="c2e25-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2e25-107">EXAMPLES</span></span>

### <span data-ttu-id="c2e25-108">Örnek 1: Kullanıcı hesabını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c2e25-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="c2e25-109">Bu komut, ContosoPool adlı havuzda belirtilen KIMLIĞE sahip işlem düğümündeki PFuller adındaki Kullanıcı hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="c2e25-110">Komut hesap parolasını ve son kullanma süresini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="c2e25-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2e25-111">PARAMETERS</span></span>

### <span data-ttu-id="c2e25-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c2e25-112">-BatchContext</span></span>
<span data-ttu-id="c2e25-113">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c2e25-114">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2e25-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c2e25-115">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="c2e25-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c2e25-116">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c2e25-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c2e25-117">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c2e25-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c2e25-118">-Computenodeıd</span><span class="sxs-lookup"><span data-stu-id="c2e25-118">-ComputeNodeId</span></span>
<span data-ttu-id="c2e25-119">Bu cmdlet 'in üzerinde yaptığı işlem düğümünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e25-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e25-120">-DefaultProfile</span></span>
<span data-ttu-id="c2e25-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2e25-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2e25-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="c2e25-122">-ExpiryTime</span></span>
<span data-ttu-id="c2e25-123">Kullanıcı hesabı için son kullanma süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="c2e25-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2e25-124">-Name</span></span>
<span data-ttu-id="c2e25-125">Bu cmdlet 'in değiştirdiği Kullanıcı hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e25-126">-Parola</span><span class="sxs-lookup"><span data-stu-id="c2e25-126">-Password</span></span>
<span data-ttu-id="c2e25-127">Kullanıcı hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-127">Specifies the password for the user account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e25-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c2e25-128">-PoolId</span></span>
<span data-ttu-id="c2e25-129">Bu cmdlet 'in üzerinde çalıştırıldığı COMPUTE düğümünü içeren havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2e25-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e25-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e25-130">CommonParameters</span></span>
<span data-ttu-id="c2e25-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2e25-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e25-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2e25-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e25-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2e25-133">INPUTS</span></span>

### <span data-ttu-id="c2e25-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c2e25-134">BatchAccountContext</span></span>
<span data-ttu-id="c2e25-135">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c2e25-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c2e25-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2e25-136">OUTPUTS</span></span>

## <span data-ttu-id="c2e25-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2e25-137">NOTES</span></span>

## <span data-ttu-id="c2e25-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2e25-138">RELATED LINKS</span></span>

[<span data-ttu-id="c2e25-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c2e25-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c2e25-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c2e25-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c2e25-141">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c2e25-141">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="c2e25-142">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c2e25-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


