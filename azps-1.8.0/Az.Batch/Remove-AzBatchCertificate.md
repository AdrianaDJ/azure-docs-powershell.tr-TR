---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchCertificate.md
ms.openlocfilehash: 8eef0043bdacc658779bdb2fd0a1241975a6284b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761846"
---
# <span data-ttu-id="4b0fe-101">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b0fe-101">Remove-AzBatchCertificate</span></span>

## <span data-ttu-id="4b0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0fe-103">Hesaptan bir sertifikayı siler.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-103">Deletes a certificate from an account.</span></span>

## <span data-ttu-id="4b0fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b0fe-104">SYNTAX</span></span>

```
Remove-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b0fe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b0fe-105">DESCRIPTION</span></span>
<span data-ttu-id="4b0fe-106">**Remove-AzBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabındaki bir sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-106">The **Remove-AzBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="4b0fe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b0fe-107">EXAMPLES</span></span>

### <span data-ttu-id="4b0fe-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b0fe-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="4b0fe-109">Bu komut belirtilen parmak izine sahip sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="4b0fe-110">Örnek 2: tüm etkin sertifikaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="4b0fe-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="4b0fe-111">Bu komut, Get-AzBatchCertificate cmdlet 'i kullanarak etkin olan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-111">This command gets all certificates that are active by using the Get-AzBatchCertificate cmdlet.</span></span>
<span data-ttu-id="4b0fe-112">Komut, ardışık düzen işlecini kullanarak etkin sertifikaları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4b0fe-113">Bu cmdlet her sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="4b0fe-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4b0fe-115">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="4b0fe-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b0fe-116">PARAMETERS</span></span>

### <span data-ttu-id="4b0fe-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4b0fe-117">-BatchContext</span></span>
<span data-ttu-id="4b0fe-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4b0fe-119">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4b0fe-120">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4b0fe-121">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4b0fe-122">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4b0fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0fe-123">-DefaultProfile</span></span>
<span data-ttu-id="4b0fe-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b0fe-125">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="4b0fe-125">-Thumbprint</span></span>
<span data-ttu-id="4b0fe-126">Bu cmdlet 'in sildiği sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-126">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="4b0fe-127">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="4b0fe-127">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="4b0fe-128">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-128">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="4b0fe-129">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-129">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="4b0fe-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b0fe-130">-Confirm</span></span>
<span data-ttu-id="4b0fe-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b0fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0fe-132">-WhatIf</span></span>
<span data-ttu-id="4b0fe-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b0fe-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b0fe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0fe-135">CommonParameters</span></span>
<span data-ttu-id="4b0fe-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b0fe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0fe-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b0fe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0fe-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b0fe-138">INPUTS</span></span>

### <span data-ttu-id="4b0fe-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4b0fe-139">System.String</span></span>

### <span data-ttu-id="4b0fe-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4b0fe-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4b0fe-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b0fe-141">OUTPUTS</span></span>

### <span data-ttu-id="4b0fe-142">System. void</span><span class="sxs-lookup"><span data-stu-id="4b0fe-142">System.Void</span></span>

## <span data-ttu-id="4b0fe-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b0fe-143">NOTES</span></span>

## <span data-ttu-id="4b0fe-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b0fe-144">RELATED LINKS</span></span>

[<span data-ttu-id="4b0fe-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b0fe-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="4b0fe-146">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="4b0fe-146">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4b0fe-147">Yeni-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4b0fe-147">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="4b0fe-148">Stop-Azbatchcertificatesilinmeye silme</span><span class="sxs-lookup"><span data-stu-id="4b0fe-148">Stop-AzBatchCertificateDeletion</span></span>](./Stop-AzBatchCertificateDeletion.md)

[<span data-ttu-id="4b0fe-149">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4b0fe-149">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


