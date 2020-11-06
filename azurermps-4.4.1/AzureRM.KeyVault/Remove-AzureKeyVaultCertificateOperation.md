---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593558"
---
# <span data-ttu-id="956ab-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="956ab-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="956ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="956ab-102">SYNOPSIS</span></span>
<span data-ttu-id="956ab-103">Anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="956ab-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="956ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="956ab-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="956ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="956ab-105">DESCRIPTION</span></span>
<span data-ttu-id="956ab-106">**Remove-AzureKeyVaultCertificateOperation** cmdlet 'i bir anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="956ab-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="956ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="956ab-107">EXAMPLES</span></span>

### <span data-ttu-id="956ab-108">Örnek 1: sertifika işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="956ab-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="956ab-109">Bu komut, TestCert01 adındaki sertifika işlemini, onay istemeden ContosoKV01 anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="956ab-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="956ab-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="956ab-110">PARAMETERS</span></span>

### <span data-ttu-id="956ab-111">-Force</span><span class="sxs-lookup"><span data-stu-id="956ab-111">-Force</span></span>
<span data-ttu-id="956ab-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="956ab-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956ab-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="956ab-113">-Name</span></span>
<span data-ttu-id="956ab-114">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="956ab-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="956ab-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="956ab-115">-PassThru</span></span>
<span data-ttu-id="956ab-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="956ab-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="956ab-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="956ab-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="956ab-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="956ab-118">-VaultName</span></span>
<span data-ttu-id="956ab-119">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="956ab-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="956ab-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="956ab-120">-Confirm</span></span>
<span data-ttu-id="956ab-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="956ab-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="956ab-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="956ab-122">-WhatIf</span></span>
<span data-ttu-id="956ab-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="956ab-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956ab-124">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="956ab-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="956ab-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="956ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="956ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="956ab-126">-DefaultProfile</span></span>
<span data-ttu-id="956ab-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="956ab-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="956ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="956ab-128">CommonParameters</span></span>
<span data-ttu-id="956ab-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="956ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="956ab-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="956ab-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="956ab-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="956ab-131">INPUTS</span></span>

## <span data-ttu-id="956ab-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="956ab-132">OUTPUTS</span></span>

### <span data-ttu-id="956ab-133">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="956ab-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="956ab-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="956ab-134">NOTES</span></span>

## <span data-ttu-id="956ab-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="956ab-135">RELATED LINKS</span></span>

[<span data-ttu-id="956ab-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="956ab-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="956ab-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="956ab-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

