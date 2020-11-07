---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765066"
---
# <span data-ttu-id="4f3c6-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4f3c6-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="4f3c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3c6-103">Belirtilen toplu hesaba sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f3c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f3c6-104">SYNTAX</span></span>

### <span data-ttu-id="4f3c6-105">Dosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f3c6-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f3c6-106">RawData</span><span class="sxs-lookup"><span data-stu-id="4f3c6-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f3c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f3c6-107">DESCRIPTION</span></span>
<span data-ttu-id="4f3c6-108">**New-AzureBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="4f3c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f3c6-109">EXAMPLES</span></span>

### <span data-ttu-id="4f3c6-110">Örnek 1: dosyadan sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="4f3c6-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="4f3c6-111">Bu komut, E:\certificates\mycert.cerfile dosyasını kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="4f3c6-112">Örnek 2: ham verilerden sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="4f3c6-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="4f3c6-113">İlk komut MyCert. pfx adlı dosyadan $RawData değişkenine verileri okur.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="4f3c6-114">İkinci komut, $RawData depolanan ham verileri kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="4f3c6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f3c6-115">PARAMETERS</span></span>

### <span data-ttu-id="4f3c6-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f3c6-116">-BatchContext</span></span>
<span data-ttu-id="4f3c6-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4f3c6-118">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4f3c6-119">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="4f3c6-119">-FilePath</span></span>
<span data-ttu-id="4f3c6-120">Sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="4f3c6-121">Sertifika dosyası. cer veya. pfx biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-121">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f3c6-122">-Parola</span><span class="sxs-lookup"><span data-stu-id="4f3c6-122">-Password</span></span>
<span data-ttu-id="4f3c6-123">Sertifika özel anahtarına erişmek için parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="4f3c6-124">. Pfx biçiminde bir sertifika belirtirseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f3c6-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="4f3c6-125">-RawData</span></span>
<span data-ttu-id="4f3c6-126">. Cer veya. pfx biçimindeki ham sertifika verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f3c6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3c6-127">-DefaultProfile</span></span>
<span data-ttu-id="4f3c6-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f3c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3c6-129">CommonParameters</span></span>
<span data-ttu-id="4f3c6-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f3c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3c6-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3c6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3c6-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f3c6-132">INPUTS</span></span>

### <span data-ttu-id="4f3c6-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f3c6-133">BatchAccountContext</span></span>
<span data-ttu-id="4f3c6-134">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4f3c6-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4f3c6-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="4f3c6-135">Byte[]</span></span>
<span data-ttu-id="4f3c6-136">' RawData ' parametresi ardışık düzenin ' Byte [] ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4f3c6-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="4f3c6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f3c6-137">OUTPUTS</span></span>

## <span data-ttu-id="4f3c6-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f3c6-138">NOTES</span></span>

## <span data-ttu-id="4f3c6-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f3c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="4f3c6-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4f3c6-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="4f3c6-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4f3c6-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4f3c6-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4f3c6-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="4f3c6-143">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4f3c6-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


