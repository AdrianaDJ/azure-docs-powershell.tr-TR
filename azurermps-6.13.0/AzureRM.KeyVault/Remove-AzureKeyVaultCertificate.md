---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 8498ea769f8f9a3f7107cb7dd883e79633b9aff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762606"
---
# <span data-ttu-id="47ba3-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47ba3-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="47ba3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47ba3-102">SYNOPSIS</span></span>
<span data-ttu-id="47ba3-103">Anahtar kasasından sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47ba3-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47ba3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47ba3-104">SYNTAX</span></span>

### <span data-ttu-id="47ba3-105">ByVaultNameAndName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47ba3-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47ba3-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="47ba3-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47ba3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="47ba3-107">DESCRIPTION</span></span>
<span data-ttu-id="47ba3-108">**Remove-AzureKeyVaultCertificate** cmdlet 'i anahtar kasadan sertifikayı çıkarır.</span><span class="sxs-lookup"><span data-stu-id="47ba3-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="47ba3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47ba3-109">EXAMPLES</span></span>

### <span data-ttu-id="47ba3-110">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="47ba3-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

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

<span data-ttu-id="47ba3-111">Bu komut, SelfSigned01 adındaki anahtar kasasına ContosoKV01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47ba3-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="47ba3-112">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="47ba3-113">Bu nedenle, cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="47ba3-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="47ba3-114">Örnek 2: silinen sertifikayı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="47ba3-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="47ba3-115">Bu komut, ' contoso ' adlı anahtar kasasından ' MyCert ' adlı sertifikayı kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47ba3-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="47ba3-116">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası 'nda önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="47ba3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47ba3-117">PARAMETERS</span></span>

### <span data-ttu-id="47ba3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ba3-118">-DefaultProfile</span></span>
<span data-ttu-id="47ba3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47ba3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47ba3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="47ba3-120">-Force</span></span>
<span data-ttu-id="47ba3-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="47ba3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47ba3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47ba3-122">-InputObject</span></span>
<span data-ttu-id="47ba3-123">Sertifika nesnesi.</span><span class="sxs-lookup"><span data-stu-id="47ba3-123">Certificate Object.</span></span>

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

### <span data-ttu-id="47ba3-124">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="47ba3-124">-InRemovedState</span></span>
<span data-ttu-id="47ba3-125">Varsa, önceden silinmiş sertifikayı kalıcı olarak kaldırır</span><span class="sxs-lookup"><span data-stu-id="47ba3-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="47ba3-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="47ba3-126">-Name</span></span>
<span data-ttu-id="47ba3-127">Bu cmdlet 'in bir anahtar kasasından kaldırdığı sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="47ba3-128">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir sertifikanın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47ba3-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="47ba3-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="47ba3-129">-PassThru</span></span>
<span data-ttu-id="47ba3-130">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="47ba3-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="47ba3-131">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="47ba3-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="47ba3-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="47ba3-132">-VaultName</span></span>
<span data-ttu-id="47ba3-133">Bu cmdlet 'in sertifikayı kaldırdığı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="47ba3-134">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47ba3-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="47ba3-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="47ba3-135">-Confirm</span></span>
<span data-ttu-id="47ba3-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47ba3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ba3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ba3-137">-WhatIf</span></span>
<span data-ttu-id="47ba3-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ba3-139">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47ba3-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ba3-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47ba3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ba3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ba3-141">CommonParameters</span></span>
<span data-ttu-id="47ba3-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47ba3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ba3-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47ba3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ba3-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47ba3-144">INPUTS</span></span>

### <span data-ttu-id="47ba3-145">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="47ba3-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="47ba3-146">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="47ba3-146">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="47ba3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47ba3-147">OUTPUTS</span></span>

### <span data-ttu-id="47ba3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47ba3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="47ba3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47ba3-149">NOTES</span></span>

## <span data-ttu-id="47ba3-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47ba3-150">RELATED LINKS</span></span>

[<span data-ttu-id="47ba3-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47ba3-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="47ba3-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47ba3-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="47ba3-153">İçeri aktarma-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47ba3-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="47ba3-154">Geri al-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="47ba3-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)