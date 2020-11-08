---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchCertificateDeletion.md
ms.openlocfilehash: 39b37f6f81a849e7ea3fc59dde6c99bebc3bfd1d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107238"
---
# <span data-ttu-id="b5af2-101">Stop-AzBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="b5af2-101">Stop-AzBatchCertificateDeletion</span></span>

## <span data-ttu-id="b5af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5af2-102">SYNOPSIS</span></span>
<span data-ttu-id="b5af2-103">Sertifikanın başarısız silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b5af2-103">Cancels a failed deletion of a certificate.</span></span>

## <span data-ttu-id="b5af2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5af2-104">SYNTAX</span></span>

```
Stop-AzBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5af2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5af2-105">DESCRIPTION</span></span>
<span data-ttu-id="b5af2-106">**Stop-Azbatchcertificatesilinmeye** cmdlet 'ı Azure toplu iş hizmetinde bir sertifikanın başarısız silinmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b5af2-106">The **Stop-AzBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="b5af2-107">Yalnızca sertifika **Deletefailed** durumundaysa, silme işlemini durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5af2-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="b5af2-108">Bu cmdlet, sertifikayı **etkin** duruma getirir.</span><span class="sxs-lookup"><span data-stu-id="b5af2-108">This cmdlet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="b5af2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5af2-109">EXAMPLES</span></span>

### <span data-ttu-id="b5af2-110">Örnek 1: silme işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="b5af2-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="b5af2-111">Bu komut, belirtilen parmak izine sahip sertifikayı silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="b5af2-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="b5af2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5af2-112">PARAMETERS</span></span>

### <span data-ttu-id="b5af2-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b5af2-113">-BatchContext</span></span>
<span data-ttu-id="b5af2-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5af2-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b5af2-115">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5af2-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b5af2-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="b5af2-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b5af2-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5af2-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b5af2-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b5af2-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b5af2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5af2-119">-DefaultProfile</span></span>
<span data-ttu-id="b5af2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5af2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5af2-121">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="b5af2-121">-Thumbprint</span></span>
<span data-ttu-id="b5af2-122">Bu cmdlet 'in **etkin** duruma geri aldığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5af2-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="b5af2-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b5af2-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b5af2-124">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5af2-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b5af2-125">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="b5af2-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="b5af2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5af2-126">CommonParameters</span></span>
<span data-ttu-id="b5af2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5af2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5af2-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b5af2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5af2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5af2-129">INPUTS</span></span>

### <span data-ttu-id="b5af2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b5af2-130">System.String</span></span>

### <span data-ttu-id="b5af2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b5af2-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b5af2-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5af2-132">OUTPUTS</span></span>

### <span data-ttu-id="b5af2-133">System. void</span><span class="sxs-lookup"><span data-stu-id="b5af2-133">System.Void</span></span>

## <span data-ttu-id="b5af2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5af2-134">NOTES</span></span>

## <span data-ttu-id="b5af2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5af2-135">RELATED LINKS</span></span>

[<span data-ttu-id="b5af2-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b5af2-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b5af2-137">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b5af2-137">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="b5af2-138">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b5af2-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


