---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: 7e8159a7a17276d749adb89ea4e1b82118f9b2bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591413"
---
# <span data-ttu-id="ae599-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae599-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="ae599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae599-102">SYNOPSIS</span></span>
<span data-ttu-id="ae599-103">Hesaptan bir sertifikayı siler.</span><span class="sxs-lookup"><span data-stu-id="ae599-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae599-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae599-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae599-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae599-105">DESCRIPTION</span></span>
<span data-ttu-id="ae599-106">**Remove-AzureBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabındaki bir sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae599-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="ae599-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae599-107">EXAMPLES</span></span>

### <span data-ttu-id="ae599-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae599-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="ae599-109">Bu komut belirtilen parmak izine sahip sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae599-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="ae599-110">Örnek 2: tüm etkin sertifikaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="ae599-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="ae599-111">Bu komut, Get-AzureBatchCertificate cmdlet 'i kullanarak etkin olan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="ae599-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="ae599-112">Komut, ardışık düzen işlecini kullanarak etkin sertifikaları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ae599-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ae599-113">Bu cmdlet her sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ae599-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="ae599-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae599-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ae599-115">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="ae599-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ae599-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae599-116">PARAMETERS</span></span>

### <span data-ttu-id="ae599-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ae599-117">-BatchContext</span></span>
<span data-ttu-id="ae599-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae599-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ae599-119">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ae599-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ae599-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="ae599-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ae599-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ae599-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ae599-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ae599-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ae599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae599-123">-DefaultProfile</span></span>
<span data-ttu-id="ae599-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae599-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae599-125">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="ae599-125">-Thumbprint</span></span>
<span data-ttu-id="ae599-126">Bu cmdlet 'in sildiği sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae599-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ae599-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ae599-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ae599-128">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae599-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ae599-129">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ae599-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="ae599-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae599-130">-Confirm</span></span>
<span data-ttu-id="ae599-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae599-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae599-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae599-132">-WhatIf</span></span>
<span data-ttu-id="ae599-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae599-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae599-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae599-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae599-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae599-135">CommonParameters</span></span>
<span data-ttu-id="ae599-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae599-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae599-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae599-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae599-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae599-138">INPUTS</span></span>

### <span data-ttu-id="ae599-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ae599-139">System.String</span></span>

### <span data-ttu-id="ae599-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ae599-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="ae599-141">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ae599-141">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="ae599-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae599-142">OUTPUTS</span></span>

### <span data-ttu-id="ae599-143">System. void</span><span class="sxs-lookup"><span data-stu-id="ae599-143">System.Void</span></span>

## <span data-ttu-id="ae599-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae599-144">NOTES</span></span>

## <span data-ttu-id="ae599-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae599-145">RELATED LINKS</span></span>

[<span data-ttu-id="ae599-146">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae599-146">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="ae599-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ae599-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ae599-148">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ae599-148">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="ae599-149">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="ae599-149">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="ae599-150">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ae599-150">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


