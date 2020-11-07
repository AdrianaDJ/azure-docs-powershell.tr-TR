---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: b2e7264b5c0f54f18e295a86f9abb1cbd51dc4b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935785"
---
# <span data-ttu-id="8c794-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="8c794-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="8c794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c794-102">SYNOPSIS</span></span>
<span data-ttu-id="8c794-103">Anahtar kasasından sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c794-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="8c794-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c794-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c794-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c794-105">DESCRIPTION</span></span>
<span data-ttu-id="8c794-106">**Remove-AzKeyVaultCertificate** cmdlet 'i anahtar kasasından sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="8c794-106">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="8c794-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c794-107">EXAMPLES</span></span>

### <span data-ttu-id="8c794-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8c794-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="8c794-109">Bu komut, SelfSigned01 adındaki anahtar kasasına ContosoKV01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c794-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="8c794-110">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c794-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8c794-111">Bu nedenle, cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="8c794-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8c794-112">Örnek 3: silinen sertifikayı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="8c794-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="8c794-113">Bu komut, ' contoso ' adlı anahtar kasasından ' MyCert ' adlı sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8c794-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="8c794-114">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası 'nda önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="8c794-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="8c794-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c794-115">PARAMETERS</span></span>

### <span data-ttu-id="8c794-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c794-116">-DefaultProfile</span></span>
<span data-ttu-id="8c794-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8c794-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c794-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8c794-118">-Force</span></span>
<span data-ttu-id="8c794-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8c794-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c794-120">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="8c794-120">-InRemovedState</span></span>
<span data-ttu-id="8c794-121">Varsa, önceden silinmiş sertifikayı kalıcı olarak kaldırır</span><span class="sxs-lookup"><span data-stu-id="8c794-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="8c794-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c794-122">-Name</span></span>
<span data-ttu-id="8c794-123">Bu cmdlet 'in bir anahtar kasasından kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c794-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="8c794-124">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir sertifikanın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c794-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c794-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8c794-125">-PassThru</span></span>
<span data-ttu-id="8c794-126">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8c794-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c794-127">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8c794-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c794-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8c794-128">-VaultName</span></span>
<span data-ttu-id="8c794-129">Bu cmdlet 'in sertifikayı kaldırdığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c794-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="8c794-130">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c794-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="8c794-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c794-131">-Confirm</span></span>
<span data-ttu-id="8c794-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c794-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c794-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c794-133">-WhatIf</span></span>
<span data-ttu-id="8c794-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c794-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c794-135">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c794-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c794-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c794-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c794-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c794-137">CommonParameters</span></span>
<span data-ttu-id="8c794-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c794-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c794-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c794-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c794-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c794-140">INPUTS</span></span>

### <span data-ttu-id="8c794-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8c794-141">None</span></span>
<span data-ttu-id="8c794-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8c794-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c794-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c794-143">OUTPUTS</span></span>

### <span data-ttu-id="8c794-144">Microsoft. Azure. Commands. Keykasa. modeller. Certificatedemeti</span><span class="sxs-lookup"><span data-stu-id="8c794-144">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="8c794-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c794-145">NOTES</span></span>

## <span data-ttu-id="8c794-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c794-146">RELATED LINKS</span></span>

[<span data-ttu-id="8c794-147">Add-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="8c794-147">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="8c794-148">Get-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="8c794-148">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="8c794-149">Import-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="8c794-149">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="8c794-150">Geri al-Azanahtarvaultcertificateremoval</span><span class="sxs-lookup"><span data-stu-id="8c794-150">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
