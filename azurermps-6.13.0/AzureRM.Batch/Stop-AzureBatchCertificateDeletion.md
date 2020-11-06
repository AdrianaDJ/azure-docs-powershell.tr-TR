---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchcertificatedeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: d43754e1b04dadc447de3d727769902f5454f79a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591399"
---
# <span data-ttu-id="44020-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="44020-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="44020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44020-102">SYNOPSIS</span></span>
<span data-ttu-id="44020-103">Sertifikanın başarısız silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="44020-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44020-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44020-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44020-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44020-105">DESCRIPTION</span></span>
<span data-ttu-id="44020-106">**Stop-AzureBatchCertificateDeletion** cmdlet 'ı, Azure Batch hizmetinde bir sertifikanın başarısız silinmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="44020-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="44020-107">Yalnızca sertifika **Deletefailed** durumundaysa, silme işlemini durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="44020-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="44020-108">Bu cmldet sertifikayı **etkin** duruma getirir.</span><span class="sxs-lookup"><span data-stu-id="44020-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="44020-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44020-109">EXAMPLES</span></span>

### <span data-ttu-id="44020-110">Örnek 1: silme işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="44020-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="44020-111">Bu komut, belirtilen parmak izine sahip sertifikayı silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="44020-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="44020-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44020-112">PARAMETERS</span></span>

### <span data-ttu-id="44020-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="44020-113">-BatchContext</span></span>
<span data-ttu-id="44020-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44020-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="44020-115">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="44020-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="44020-116">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="44020-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="44020-117">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="44020-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="44020-118">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="44020-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="44020-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44020-119">-DefaultProfile</span></span>
<span data-ttu-id="44020-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44020-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44020-121">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="44020-121">-Thumbprint</span></span>
<span data-ttu-id="44020-122">Bu cmdlet 'in **etkin** duruma geri aldığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="44020-122">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="44020-123">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="44020-123">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="44020-124">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="44020-124">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="44020-125">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="44020-125">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="44020-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44020-126">CommonParameters</span></span>
<span data-ttu-id="44020-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44020-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44020-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44020-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44020-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44020-129">INPUTS</span></span>

### <span data-ttu-id="44020-130">System. String</span><span class="sxs-lookup"><span data-stu-id="44020-130">System.String</span></span>

### <span data-ttu-id="44020-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="44020-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="44020-132">Parametreler: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="44020-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="44020-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44020-133">OUTPUTS</span></span>

### <span data-ttu-id="44020-134">System. void</span><span class="sxs-lookup"><span data-stu-id="44020-134">System.Void</span></span>

## <span data-ttu-id="44020-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44020-135">NOTES</span></span>

## <span data-ttu-id="44020-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44020-136">RELATED LINKS</span></span>

[<span data-ttu-id="44020-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="44020-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="44020-138">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="44020-138">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="44020-139">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="44020-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


