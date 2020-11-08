---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109984"
---
# <span data-ttu-id="e3b55-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e3b55-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="e3b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b55-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b55-103">Anahtar kasasından sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b55-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="e3b55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3b55-104">SYNTAX</span></span>

### <span data-ttu-id="e3b55-105">ByVaultNameAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e3b55-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b55-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e3b55-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b55-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3b55-107">DESCRIPTION</span></span>
<span data-ttu-id="e3b55-108">**Remove-AzKeyVaultCertificate** cmdlet 'i anahtar kasasından sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="e3b55-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="e3b55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3b55-109">EXAMPLES</span></span>

### <span data-ttu-id="e3b55-110">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="e3b55-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="e3b55-111">Bu komut, SelfSigned01 adındaki anahtar kasasına ContosoKV01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b55-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="e3b55-112">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e3b55-113">Bu nedenle, cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="e3b55-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="e3b55-114">Örnek 2: silinen sertifikayı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="e3b55-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="e3b55-115">Bu komut, ' contoso ' adlı anahtar kasasından ' MyCert ' adlı sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3b55-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="e3b55-116">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası 'nda önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="e3b55-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3b55-117">PARAMETERS</span></span>

### <span data-ttu-id="e3b55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b55-118">-DefaultProfile</span></span>
<span data-ttu-id="e3b55-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e3b55-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3b55-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e3b55-120">-Force</span></span>
<span data-ttu-id="e3b55-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e3b55-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3b55-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3b55-122">-InputObject</span></span>
<span data-ttu-id="e3b55-123">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e3b55-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b55-124">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="e3b55-124">-InRemovedState</span></span>
<span data-ttu-id="e3b55-125">Varsa, önceden silinmiş sertifikayı kalıcı olarak kaldırır</span><span class="sxs-lookup"><span data-stu-id="e3b55-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="e3b55-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3b55-126">-Name</span></span>
<span data-ttu-id="e3b55-127">Bu cmdlet 'in bir anahtar kasasından kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="e3b55-128">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir sertifikanın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3b55-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b55-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3b55-129">-PassThru</span></span>
<span data-ttu-id="e3b55-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3b55-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3b55-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e3b55-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3b55-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e3b55-132">-VaultName</span></span>
<span data-ttu-id="e3b55-133">Bu cmdlet 'in sertifikayı kaldırdığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="e3b55-134">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e3b55-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b55-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3b55-135">-Confirm</span></span>
<span data-ttu-id="e3b55-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3b55-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b55-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b55-137">-WhatIf</span></span>
<span data-ttu-id="e3b55-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b55-139">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3b55-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b55-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3b55-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b55-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b55-141">CommonParameters</span></span>
<span data-ttu-id="e3b55-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3b55-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b55-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e3b55-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b55-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3b55-144">INPUTS</span></span>

### <span data-ttu-id="e3b55-145">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="e3b55-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="e3b55-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3b55-146">OUTPUTS</span></span>

### <span data-ttu-id="e3b55-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="e3b55-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="e3b55-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3b55-148">NOTES</span></span>

## <span data-ttu-id="e3b55-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3b55-149">RELATED LINKS</span></span>

[<span data-ttu-id="e3b55-150">Add-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="e3b55-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="e3b55-151">Get-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="e3b55-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="e3b55-152">Import-Azanahtarvaultcertificate</span><span class="sxs-lookup"><span data-stu-id="e3b55-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="e3b55-153">Geri al-Azanahtarvaultcertificateremoval</span><span class="sxs-lookup"><span data-stu-id="e3b55-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
