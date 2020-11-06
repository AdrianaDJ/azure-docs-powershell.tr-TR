---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594971"
---
# <span data-ttu-id="9daad-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9daad-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="9daad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9daad-102">SYNOPSIS</span></span>
<span data-ttu-id="9daad-103">Belirtilen toplu hesaba sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="9daad-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9daad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9daad-104">SYNTAX</span></span>

### <span data-ttu-id="9daad-105">Dosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9daad-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9daad-106">RawData</span><span class="sxs-lookup"><span data-stu-id="9daad-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9daad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9daad-107">DESCRIPTION</span></span>
<span data-ttu-id="9daad-108">**New-AzureBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="9daad-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="9daad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9daad-109">EXAMPLES</span></span>

### <span data-ttu-id="9daad-110">Örnek 1: dosyadan sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="9daad-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="9daad-111">Bu komut, E:\certificates\mycert.cerfile dosyasını kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="9daad-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="9daad-112">Örnek 2: ham verilerden sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="9daad-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="9daad-113">İlk komut MyCert. pfx adlı dosyadan $RawData değişkenine verileri okur.</span><span class="sxs-lookup"><span data-stu-id="9daad-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="9daad-114">İkinci komut, $RawData depolanan ham verileri kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="9daad-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="9daad-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9daad-115">PARAMETERS</span></span>

### <span data-ttu-id="9daad-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9daad-116">-BatchContext</span></span>
<span data-ttu-id="9daad-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9daad-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9daad-118">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9daad-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9daad-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="9daad-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9daad-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9daad-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9daad-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9daad-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9daad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9daad-122">-DefaultProfile</span></span>
<span data-ttu-id="9daad-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9daad-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9daad-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="9daad-124">-FilePath</span></span>
<span data-ttu-id="9daad-125">Sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9daad-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="9daad-126">Sertifika dosyası. cer veya. pfx biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9daad-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daad-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="9daad-127">-Password</span></span>
<span data-ttu-id="9daad-128">Sertifika özel anahtarına erişmek için parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="9daad-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="9daad-129">. Pfx biçiminde bir sertifika belirtirseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9daad-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9daad-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="9daad-130">-RawData</span></span>
<span data-ttu-id="9daad-131">. Cer veya. pfx biçimindeki ham sertifika verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9daad-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9daad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9daad-132">CommonParameters</span></span>
<span data-ttu-id="9daad-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9daad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9daad-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9daad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9daad-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9daad-135">INPUTS</span></span>

### <span data-ttu-id="9daad-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9daad-136">BatchAccountContext</span></span>
<span data-ttu-id="9daad-137">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9daad-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="9daad-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="9daad-138">Byte[]</span></span>
<span data-ttu-id="9daad-139">' RawData ' parametresi ardışık düzenin ' Byte [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9daad-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="9daad-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9daad-140">OUTPUTS</span></span>

## <span data-ttu-id="9daad-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9daad-141">NOTES</span></span>

## <span data-ttu-id="9daad-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9daad-142">RELATED LINKS</span></span>

[<span data-ttu-id="9daad-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9daad-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="9daad-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9daad-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9daad-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="9daad-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="9daad-146">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9daad-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


