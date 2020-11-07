---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938834"
---
# <span data-ttu-id="5aa27-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5aa27-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5aa27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa27-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa27-103">Anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="5aa27-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aa27-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5aa27-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aa27-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5aa27-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa27-106">**Remove-AzureKeyVaultCertificateOperation** cmdlet 'i bir anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="5aa27-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="5aa27-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5aa27-107">EXAMPLES</span></span>

### <span data-ttu-id="5aa27-108">Örnek 1: sertifika işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5aa27-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="5aa27-109">Bu komut, TestCert01 adındaki sertifika işlemini, onay istemeden ContosoKV01 anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5aa27-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="5aa27-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5aa27-110">PARAMETERS</span></span>

### <span data-ttu-id="5aa27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa27-111">-DefaultProfile</span></span>
<span data-ttu-id="5aa27-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5aa27-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aa27-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5aa27-113">-Force</span></span>
<span data-ttu-id="5aa27-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5aa27-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5aa27-115">-Name</span></span>
<span data-ttu-id="5aa27-116">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa27-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5aa27-117">-PassThru</span></span>
<span data-ttu-id="5aa27-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5aa27-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5aa27-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5aa27-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5aa27-120">-VaultName</span></span>
<span data-ttu-id="5aa27-121">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa27-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="5aa27-122">-Confirm</span></span>
<span data-ttu-id="5aa27-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5aa27-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa27-124">-WhatIf</span></span>
<span data-ttu-id="5aa27-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5aa27-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa27-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5aa27-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa27-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5aa27-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa27-128">CommonParameters</span></span>
<span data-ttu-id="5aa27-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5aa27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa27-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aa27-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa27-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5aa27-131">INPUTS</span></span>

## <span data-ttu-id="5aa27-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5aa27-132">OUTPUTS</span></span>

### <span data-ttu-id="5aa27-133">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5aa27-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5aa27-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5aa27-134">NOTES</span></span>

## <span data-ttu-id="5aa27-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5aa27-135">RELATED LINKS</span></span>

[<span data-ttu-id="5aa27-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5aa27-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="5aa27-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5aa27-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

