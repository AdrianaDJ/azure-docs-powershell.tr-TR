---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: d0fefe06ad5392d2fe50552203a08872eea4e61f
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761859"
---
# <span data-ttu-id="743ce-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="743ce-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="743ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743ce-102">SYNOPSIS</span></span>
<span data-ttu-id="743ce-103">Belirtilen toplu hesaba sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="743ce-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="743ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="743ce-104">SYNTAX</span></span>

### <span data-ttu-id="743ce-105">Dosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="743ce-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="743ce-106">RawData</span><span class="sxs-lookup"><span data-stu-id="743ce-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="743ce-107">DESCRIPTION</span></span>
<span data-ttu-id="743ce-108">**New-AzBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="743ce-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="743ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="743ce-109">EXAMPLES</span></span>

### <span data-ttu-id="743ce-110">Örnek 1: dosyadan sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="743ce-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="743ce-111">Bu komut, E:\certificates\mycert.cerfile dosyasını kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="743ce-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="743ce-112">Örnek 2: ham verilerden sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="743ce-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="743ce-113">İlk komut MyCert. pfx adlı dosyadan $RawData değişkenine verileri okur.</span><span class="sxs-lookup"><span data-stu-id="743ce-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="743ce-114">İkinci komut, $RawData depolanan ham verileri kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="743ce-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="743ce-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="743ce-115">PARAMETERS</span></span>

### <span data-ttu-id="743ce-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="743ce-116">-BatchContext</span></span>
<span data-ttu-id="743ce-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="743ce-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="743ce-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="743ce-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="743ce-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="743ce-119">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="743ce-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="743ce-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="743ce-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="743ce-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="743ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743ce-122">-DefaultProfile</span></span>
<span data-ttu-id="743ce-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="743ce-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743ce-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="743ce-124">-FilePath</span></span>
<span data-ttu-id="743ce-125">Sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="743ce-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="743ce-126">Sertifika dosyası. cer veya. pfx biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="743ce-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="743ce-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="743ce-127">-Password</span></span>
<span data-ttu-id="743ce-128">Sertifika özel anahtarına erişmek için parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="743ce-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="743ce-129">. Pfx biçiminde bir sertifika belirtirseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="743ce-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="743ce-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="743ce-130">-RawData</span></span>
<span data-ttu-id="743ce-131">. Cer veya. pfx biçimindeki ham sertifika verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="743ce-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="743ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743ce-132">CommonParameters</span></span>
<span data-ttu-id="743ce-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="743ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743ce-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743ce-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="743ce-135">INPUTS</span></span>

### <span data-ttu-id="743ce-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="743ce-136">System.Byte[]</span></span>

### <span data-ttu-id="743ce-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="743ce-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="743ce-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="743ce-138">OUTPUTS</span></span>

### <span data-ttu-id="743ce-139">System. void</span><span class="sxs-lookup"><span data-stu-id="743ce-139">System.Void</span></span>

## <span data-ttu-id="743ce-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="743ce-140">NOTES</span></span>

## <span data-ttu-id="743ce-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="743ce-141">RELATED LINKS</span></span>

[<span data-ttu-id="743ce-142">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="743ce-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="743ce-143">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="743ce-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="743ce-144">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="743ce-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="743ce-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="743ce-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


