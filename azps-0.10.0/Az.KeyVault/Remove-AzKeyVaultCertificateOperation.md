---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935777"
---
# <span data-ttu-id="30f89-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="30f89-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="30f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f89-102">SYNOPSIS</span></span>
<span data-ttu-id="30f89-103">Anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="30f89-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="30f89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30f89-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30f89-105">DESCRIPTION</span></span>
<span data-ttu-id="30f89-106">**Remove-AzKeyVaultCertificateOperation** cmdlet 'i anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="30f89-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="30f89-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30f89-107">EXAMPLES</span></span>

### <span data-ttu-id="30f89-108">Örnek 1: sertifika işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="30f89-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="30f89-109">Bu komut, TestCert01 adındaki sertifika işlemini, onay istemeden ContosoKV01 anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30f89-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="30f89-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30f89-110">PARAMETERS</span></span>

### <span data-ttu-id="30f89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f89-111">-DefaultProfile</span></span>
<span data-ttu-id="30f89-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="30f89-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30f89-113">-Force</span><span class="sxs-lookup"><span data-stu-id="30f89-113">-Force</span></span>
<span data-ttu-id="30f89-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="30f89-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30f89-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="30f89-115">-Name</span></span>
<span data-ttu-id="30f89-116">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30f89-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="30f89-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="30f89-117">-PassThru</span></span>
<span data-ttu-id="30f89-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="30f89-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="30f89-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="30f89-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="30f89-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="30f89-120">-VaultName</span></span>
<span data-ttu-id="30f89-121">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30f89-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="30f89-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="30f89-122">-Confirm</span></span>
<span data-ttu-id="30f89-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30f89-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f89-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f89-124">-WhatIf</span></span>
<span data-ttu-id="30f89-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30f89-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f89-126">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30f89-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f89-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30f89-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f89-128">CommonParameters</span></span>
<span data-ttu-id="30f89-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30f89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f89-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30f89-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f89-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30f89-131">INPUTS</span></span>

### <span data-ttu-id="30f89-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="30f89-132">None</span></span>
<span data-ttu-id="30f89-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="30f89-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30f89-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30f89-134">OUTPUTS</span></span>

### <span data-ttu-id="30f89-135">Microsoft. Azure. Commands. Keykasa. modeller. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="30f89-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="30f89-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30f89-136">NOTES</span></span>

## <span data-ttu-id="30f89-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30f89-137">RELATED LINKS</span></span>

[<span data-ttu-id="30f89-138">Get-Azanahtarvaultcertificateoperation</span><span class="sxs-lookup"><span data-stu-id="30f89-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="30f89-139">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="30f89-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

