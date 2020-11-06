---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589766"
---
# <span data-ttu-id="aeddd-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="aeddd-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="aeddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeddd-102">SYNOPSIS</span></span>
<span data-ttu-id="aeddd-103">Anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="aeddd-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aeddd-104">SYNTAX</span></span>

### <span data-ttu-id="aeddd-105">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="aeddd-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeddd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="aeddd-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeddd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aeddd-107">DESCRIPTION</span></span>
<span data-ttu-id="aeddd-108">**Remove-AzureKeyVaultCertificateOperation** cmdlet 'i bir anahtar kasasından sertifika işlemini siler.</span><span class="sxs-lookup"><span data-stu-id="aeddd-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="aeddd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aeddd-109">EXAMPLES</span></span>

### <span data-ttu-id="aeddd-110">Örnek 1: sertifika işlemini kaldırma</span><span class="sxs-lookup"><span data-stu-id="aeddd-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="aeddd-111">Bu komut, TestCert01 adındaki sertifika işlemini, onay istemeden ContosoKV01 anahtar kasasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aeddd-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="aeddd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aeddd-112">PARAMETERS</span></span>

### <span data-ttu-id="aeddd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeddd-113">-DefaultProfile</span></span>
<span data-ttu-id="aeddd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aeddd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeddd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aeddd-115">-Force</span></span>
<span data-ttu-id="aeddd-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="aeddd-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aeddd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aeddd-117">-InputObject</span></span>
<span data-ttu-id="aeddd-118">İşlem nesnesi</span><span class="sxs-lookup"><span data-stu-id="aeddd-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aeddd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="aeddd-119">-Name</span></span>
<span data-ttu-id="aeddd-120">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeddd-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeddd-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="aeddd-121">-PassThru</span></span>
<span data-ttu-id="aeddd-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="aeddd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aeddd-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="aeddd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aeddd-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aeddd-124">-VaultName</span></span>
<span data-ttu-id="aeddd-125">Bir Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aeddd-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeddd-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="aeddd-126">-Confirm</span></span>
<span data-ttu-id="aeddd-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aeddd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeddd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeddd-128">-WhatIf</span></span>
<span data-ttu-id="aeddd-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeddd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeddd-130">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aeddd-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeddd-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aeddd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeddd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeddd-132">CommonParameters</span></span>
<span data-ttu-id="aeddd-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aeddd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeddd-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeddd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeddd-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aeddd-135">INPUTS</span></span>

### <span data-ttu-id="aeddd-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aeddd-136">None</span></span>
<span data-ttu-id="aeddd-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="aeddd-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aeddd-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aeddd-138">OUTPUTS</span></span>

### <span data-ttu-id="aeddd-139">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="aeddd-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="aeddd-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aeddd-140">NOTES</span></span>

## <span data-ttu-id="aeddd-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aeddd-141">RELATED LINKS</span></span>

[<span data-ttu-id="aeddd-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="aeddd-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="aeddd-143">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="aeddd-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

