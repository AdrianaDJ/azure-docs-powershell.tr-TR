---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3DFFD0F2-6CD8-4FBE-B15C-8505CBF8F44E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchCertificate.md
ms.openlocfilehash: c63caed99a10851d6172e0db5dcc33e3404be215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588277"
---
# <span data-ttu-id="acddd-101">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="acddd-101">Remove-AzureBatchCertificate</span></span>

## <span data-ttu-id="acddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acddd-102">SYNOPSIS</span></span>
<span data-ttu-id="acddd-103">Hesaptan bir sertifikayı siler.</span><span class="sxs-lookup"><span data-stu-id="acddd-103">Deletes a certificate from an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acddd-104">SYNTAX</span></span>

```
Remove-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acddd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acddd-105">DESCRIPTION</span></span>
<span data-ttu-id="acddd-106">**Remove-AzureBatchCertificate** cmdlet 'ı belirtilen Azure toplu hesabındaki bir sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="acddd-106">The **Remove-AzureBatchCertificate** cmdlet removes a certificate from the specified Azure Batch account.</span></span>

## <span data-ttu-id="acddd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acddd-107">EXAMPLES</span></span>

### <span data-ttu-id="acddd-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="acddd-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureBatchCertificate -ThumbprintAlgorithm "sha1" -Thumbprint "c1e494a415149c5f211c4778b52f2e834a07247c" -BatchContext $Context
```

<span data-ttu-id="acddd-109">Bu komut belirtilen parmak izine sahip sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="acddd-109">This command removes the certificate that has the specified thumbprint.</span></span>

### <span data-ttu-id="acddd-110">Örnek 2: tüm etkin sertifikaları kaldırma</span><span class="sxs-lookup"><span data-stu-id="acddd-110">Example 2:Remove all active certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context | Remove-AzureBatchCertificate -Force -BatchContext $Context
```

<span data-ttu-id="acddd-111">Bu komut, Get-AzureBatchCertificate cmdlet 'i kullanarak etkin olan tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="acddd-111">This command gets all certificates that are active by using the Get-AzureBatchCertificate cmdlet.</span></span>
<span data-ttu-id="acddd-112">Komut, ardışık düzen işlecini kullanarak etkin sertifikaları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="acddd-112">The command passes the active certificates to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="acddd-113">Bu cmdlet her sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="acddd-113">That cmdlet removes each certificate.</span></span>
<span data-ttu-id="acddd-114">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acddd-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="acddd-115">Bu nedenle, komut sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="acddd-115">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="acddd-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acddd-116">PARAMETERS</span></span>

### <span data-ttu-id="acddd-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="acddd-117">-BatchContext</span></span>
<span data-ttu-id="acddd-118">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acddd-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="acddd-119">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="acddd-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="acddd-120">-Parmak izi</span><span class="sxs-lookup"><span data-stu-id="acddd-120">-Thumbprint</span></span>
<span data-ttu-id="acddd-121">Bu cmdlet 'in sildiği sertifikanın parmak izini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acddd-121">Specifies the thumbprint of the certificate that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="acddd-122">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="acddd-122">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="acddd-123">*Parmak izi* parametresini türetmek için kullanılan algoritmayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="acddd-123">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="acddd-124">Şu anda tek geçerli değer SHA1 ' dır.</span><span class="sxs-lookup"><span data-stu-id="acddd-124">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="acddd-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="acddd-125">-Confirm</span></span>
<span data-ttu-id="acddd-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acddd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acddd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acddd-127">-WhatIf</span></span>
<span data-ttu-id="acddd-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acddd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acddd-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acddd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acddd-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acddd-130">-DefaultProfile</span></span>
<span data-ttu-id="acddd-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acddd-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acddd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acddd-132">CommonParameters</span></span>
<span data-ttu-id="acddd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acddd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acddd-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acddd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acddd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acddd-135">INPUTS</span></span>

### <span data-ttu-id="acddd-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="acddd-136">BatchAccountContext</span></span>
<span data-ttu-id="acddd-137">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="acddd-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="acddd-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acddd-138">OUTPUTS</span></span>

## <span data-ttu-id="acddd-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acddd-139">NOTES</span></span>

## <span data-ttu-id="acddd-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acddd-140">RELATED LINKS</span></span>

[<span data-ttu-id="acddd-141">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="acddd-141">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="acddd-142">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="acddd-142">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="acddd-143">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="acddd-143">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="acddd-144">Stop-AzureBatchCertificateDeletion</span><span class="sxs-lookup"><span data-stu-id="acddd-144">Stop-AzureBatchCertificateDeletion</span></span>](./Stop-AzureBatchCertificateDeletion.md)

[<span data-ttu-id="acddd-145">Azure toplu Iş cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="acddd-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


