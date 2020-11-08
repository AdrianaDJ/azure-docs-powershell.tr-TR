---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276421"
---
# <span data-ttu-id="e4624-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e4624-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="e4624-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4624-102">SYNOPSIS</span></span>
<span data-ttu-id="e4624-103">Belirtilen toplu hesaba sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="e4624-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="e4624-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4624-104">SYNTAX</span></span>

### <span data-ttu-id="e4624-105">Dosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4624-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4624-106">RawData</span><span class="sxs-lookup"><span data-stu-id="e4624-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4624-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4624-107">DESCRIPTION</span></span>
<span data-ttu-id="e4624-108">**New-AzBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="e4624-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="e4624-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4624-109">EXAMPLES</span></span>

### <span data-ttu-id="e4624-110">Örnek 1: dosyadan sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="e4624-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="e4624-111">Bu komut, E:\certificates\mycert.cerfile dosyasını kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="e4624-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="e4624-112">Örnek 2: ham verilerden sertifika ekleme</span><span class="sxs-lookup"><span data-stu-id="e4624-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="e4624-113">İlk komut MyCert. pfx adlı dosyadan $RawData değişkenine verileri okur.</span><span class="sxs-lookup"><span data-stu-id="e4624-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="e4624-114">İkinci komut, $RawData depolanan ham verileri kullanarak belirtilen toplu hesap hesabına sertifika ekler.</span><span class="sxs-lookup"><span data-stu-id="e4624-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="e4624-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4624-115">PARAMETERS</span></span>

### <span data-ttu-id="e4624-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e4624-116">-BatchContext</span></span>
<span data-ttu-id="e4624-117">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4624-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e4624-118">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4624-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e4624-119">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKey cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="e4624-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e4624-120">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4624-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e4624-121">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4624-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e4624-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4624-122">-DefaultProfile</span></span>
<span data-ttu-id="e4624-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4624-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4624-124">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="e4624-124">-FilePath</span></span>
<span data-ttu-id="e4624-125">Sertifika dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4624-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="e4624-126">Sertifika dosyası. cer veya. pfx biçiminde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e4624-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="e4624-127">-Tür</span><span class="sxs-lookup"><span data-stu-id="e4624-127">-Kind</span></span>
<span data-ttu-id="e4624-128">Oluşturulacak sertifika türü.</span><span class="sxs-lookup"><span data-stu-id="e4624-128">The kind of certificate to create.</span></span> <span data-ttu-id="e4624-129">Bu belirtilmezse, parolası olmayan tüm sertifikaların CER ve parola içeren tüm sertifikaların PFX olduğu varsayılır.</span><span class="sxs-lookup"><span data-stu-id="e4624-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4624-130">-Parola</span><span class="sxs-lookup"><span data-stu-id="e4624-130">-Password</span></span>
<span data-ttu-id="e4624-131">Sertifika özel anahtarına erişmek için parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4624-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="e4624-132">. Pfx biçiminde bir sertifika belirtirseniz bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4624-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="e4624-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="e4624-133">-RawData</span></span>
<span data-ttu-id="e4624-134">. Cer veya. pfx biçimindeki ham sertifika verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4624-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="e4624-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4624-135">CommonParameters</span></span>
<span data-ttu-id="e4624-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4624-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4624-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e4624-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4624-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4624-138">INPUTS</span></span>

### <span data-ttu-id="e4624-139">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="e4624-139">System.Byte[]</span></span>

### <span data-ttu-id="e4624-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e4624-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e4624-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4624-141">OUTPUTS</span></span>

### <span data-ttu-id="e4624-142">System. void</span><span class="sxs-lookup"><span data-stu-id="e4624-142">System.Void</span></span>

## <span data-ttu-id="e4624-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4624-143">NOTES</span></span>

## <span data-ttu-id="e4624-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4624-144">RELATED LINKS</span></span>

[<span data-ttu-id="e4624-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e4624-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="e4624-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="e4624-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e4624-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="e4624-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="e4624-148">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e4624-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
