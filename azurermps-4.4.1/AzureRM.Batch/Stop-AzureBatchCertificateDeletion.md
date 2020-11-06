---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B3C8A2DB-6571-418D-8C4B-3BE3FDA42F89
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchCertificateDeletion.md
ms.openlocfilehash: 820e94b75c19d49f4e49ee8419f7807a839f925b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591799"
---
# <span data-ttu-id="ad7fc-101">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="ad7fc-101">Stop-AzureBatchCertificateDeletion</span></span>

## <span data-ttu-id="ad7fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ad7fc-103">Sertifikanın başarısız silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-103">Cancels a failed deletion of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad7fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad7fc-104">SYNTAX</span></span>

```
Stop-AzureBatchCertificateDeletion [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad7fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad7fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ad7fc-106">**Stop-AzureBatchCertificateDeletion** cmdlet 'ı, Azure Batch hizmetinde bir sertifikanın başarısız silinmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-106">The **Stop-AzureBatchCertificateDeletion** cmdlet cancels a failed deletion of a certificate in the Azure Batch service.</span></span>
<span data-ttu-id="ad7fc-107">Yalnızca sertifika **Deletefailed** durumundaysa, silme işlemini durdurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-107">You can stop a deletion only if the certificate is in the **DeleteFailed** state.</span></span>
<span data-ttu-id="ad7fc-108">Bu cmldet sertifikayı **etkin** duruma getirir.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-108">This cmldet restores the certificate to the **Active** state.</span></span>

## <span data-ttu-id="ad7fc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad7fc-109">EXAMPLES</span></span>

### <span data-ttu-id="ad7fc-110">Örnek 1: silme işlemini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="ad7fc-110">Example 1: Cancel a deletion</span></span>
```
PS C:\>Stop-AzureBatchCertificateDeletion -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="ad7fc-111">Bu komut, belirtilen parmak izine sahip sertifikayı silme işlemini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-111">This command cancels the deletion of the certificate that has the specified thumbprint.</span></span>

## <span data-ttu-id="ad7fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad7fc-112">PARAMETERS</span></span>

### <span data-ttu-id="ad7fc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ad7fc-113">-BatchContext</span></span>
<span data-ttu-id="ad7fc-114">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ad7fc-115">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ad7fc-116">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="ad7fc-116">-Thumbprint</span></span>
<span data-ttu-id="ad7fc-117">Bu cmdlet 'in **etkin** duruma geri aldığı sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-117">Specifies the thumbprint of the certificate that this cmdlet restores to the **Active** state.</span></span>

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

### <span data-ttu-id="ad7fc-118">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ad7fc-118">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ad7fc-119">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-119">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="ad7fc-120">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-120">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="ad7fc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad7fc-121">-DefaultProfile</span></span>
<span data-ttu-id="ad7fc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad7fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad7fc-123">CommonParameters</span></span>
<span data-ttu-id="ad7fc-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad7fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad7fc-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad7fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad7fc-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad7fc-126">INPUTS</span></span>

### <span data-ttu-id="ad7fc-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ad7fc-127">BatchAccountContext</span></span>
<span data-ttu-id="ad7fc-128">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ad7fc-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ad7fc-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad7fc-129">OUTPUTS</span></span>

## <span data-ttu-id="ad7fc-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad7fc-130">NOTES</span></span>

## <span data-ttu-id="ad7fc-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad7fc-131">RELATED LINKS</span></span>

[<span data-ttu-id="ad7fc-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ad7fc-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ad7fc-133">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="ad7fc-133">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="ad7fc-134">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ad7fc-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


