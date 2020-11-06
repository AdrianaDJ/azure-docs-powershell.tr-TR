---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593482"
---
# <span data-ttu-id="cdac9-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cdac9-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="cdac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdac9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdac9-103">Anahtar kasasından sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdac9-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdac9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdac9-104">SYNTAX</span></span>

### <span data-ttu-id="cdac9-105">ByVaultNameAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdac9-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdac9-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cdac9-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdac9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdac9-107">DESCRIPTION</span></span>
<span data-ttu-id="cdac9-108">**Remove-AzureKeyVaultCertificate** cmdlet 'i anahtar kasadan sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="cdac9-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="cdac9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdac9-109">EXAMPLES</span></span>

### <span data-ttu-id="cdac9-110">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="cdac9-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="cdac9-111">Bu komut, SelfSigned01 adındaki anahtar kasasına ContosoKV01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdac9-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="cdac9-112">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cdac9-113">Bu nedenle, cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="cdac9-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="cdac9-114">Örnek 3: silinen sertifikayı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="cdac9-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="cdac9-115">Bu komut, ' contoso ' adlı anahtar kasasından ' MyCert ' adlı sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdac9-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="cdac9-116">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası 'nda önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="cdac9-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdac9-117">PARAMETERS</span></span>

### <span data-ttu-id="cdac9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdac9-118">-DefaultProfile</span></span>
<span data-ttu-id="cdac9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cdac9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cdac9-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cdac9-120">-Force</span></span>
<span data-ttu-id="cdac9-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cdac9-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdac9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdac9-122">-InputObject</span></span>
<span data-ttu-id="cdac9-123">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cdac9-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac9-124">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="cdac9-124">-InRemovedState</span></span>
<span data-ttu-id="cdac9-125">Varsa, önceden silinmiş sertifikayı kalıcı olarak kaldırır</span><span class="sxs-lookup"><span data-stu-id="cdac9-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="cdac9-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="cdac9-126">-Name</span></span>
<span data-ttu-id="cdac9-127">Bu cmdlet 'in bir anahtar kasasından kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="cdac9-128">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir sertifikanın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac9-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac9-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cdac9-129">-PassThru</span></span>
<span data-ttu-id="cdac9-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cdac9-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cdac9-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cdac9-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cdac9-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cdac9-132">-VaultName</span></span>
<span data-ttu-id="cdac9-133">Bu cmdlet 'in sertifikayı kaldırdığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="cdac9-134">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cdac9-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdac9-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="cdac9-135">-Confirm</span></span>
<span data-ttu-id="cdac9-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cdac9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdac9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdac9-137">-WhatIf</span></span>
<span data-ttu-id="cdac9-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdac9-139">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cdac9-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdac9-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cdac9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdac9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdac9-141">CommonParameters</span></span>
<span data-ttu-id="cdac9-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdac9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdac9-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdac9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdac9-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdac9-144">INPUTS</span></span>

### <span data-ttu-id="cdac9-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cdac9-145">None</span></span>
<span data-ttu-id="cdac9-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cdac9-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdac9-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdac9-147">OUTPUTS</span></span>

### <span data-ttu-id="cdac9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cdac9-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="cdac9-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdac9-149">NOTES</span></span>

## <span data-ttu-id="cdac9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdac9-150">RELATED LINKS</span></span>

[<span data-ttu-id="cdac9-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cdac9-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cdac9-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cdac9-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cdac9-153">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cdac9-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cdac9-154">Geri al-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="cdac9-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
