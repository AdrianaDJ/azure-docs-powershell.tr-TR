---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: c363f32b8c28b2e6f83f4e065c677926800d04b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764653"
---
# <span data-ttu-id="aefb9-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aefb9-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="aefb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aefb9-102">SYNOPSIS</span></span>
<span data-ttu-id="aefb9-103">Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasasına anahtar aktarır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aefb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aefb9-104">SYNTAX</span></span>

### <span data-ttu-id="aefb9-105">Interactivecoluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aefb9-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefb9-106">Interactiveımport</span><span class="sxs-lookup"><span data-stu-id="aefb9-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefb9-107">Inputobjectcreate</span><span class="sxs-lookup"><span data-stu-id="aefb9-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefb9-108">Inputobjectimport</span><span class="sxs-lookup"><span data-stu-id="aefb9-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefb9-109">Resourceıdcreate</span><span class="sxs-lookup"><span data-stu-id="aefb9-109">ResourceIdCreate</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aefb9-110">Resourceidmport</span><span class="sxs-lookup"><span data-stu-id="aefb9-110">ResourceIdImport</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aefb9-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="aefb9-111">DESCRIPTION</span></span>
<span data-ttu-id="aefb9-112">**Add-AzureKeyVaultKey** cmdlet 'ı Azure Anahtar Kasası 'ndaki bir Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasaya bir anahtar aktarır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-112">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="aefb9-113">Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:</span><span class="sxs-lookup"><span data-stu-id="aefb9-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="aefb9-114">Anahtar Kasası hizmetinde donanım güvenlik modülünde (HSM) bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aefb9-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="aefb9-115">Temel kasa hizmetinde yazılımda bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="aefb9-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="aefb9-116">Anahtar Kasası hizmetinde kendi donanım güvenlik modülünden (HSM) bir anahtarı içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="aefb9-117">Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="aefb9-118">Bilgisayarınızdaki. pfx dosyasındaki bir anahtarı Anahtar Kasası hizmetindeki donanım güvenlik modüllerine (HSMs) aktarın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="aefb9-119">Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="aefb9-120">Anahtar kasasındaki varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="aefb9-121">Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="aefb9-122">Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, Anahtar Kasası REST API belgelerinde [anahtarlar ve gizlilikler hakkında](https://go.microsoft.com/fwlink/?linkid=518560) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="aefb9-123">Not: bir anahtarı kendi donanım güvenlik modülünden içeri aktarmak Için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="aefb9-124">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="aefb9-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="aefb9-125">En iyi uygulama olarak, Backup-AzureKeyVaultKey cmdlet 'ini kullanarak, oluşturulduktan veya güncelleştirildikten sonra anahtarınızı yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="aefb9-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="aefb9-126">Silmeyi geri alma işlevi yapılmaz, bu nedenle anahtarınızı yanlışlıkla sildiğiniz veya silerseniz ve ardından fikir olarak değiştirirseniz, geri yükleyebileceğiniz bir yedeğiniz yoksa anahtar kurtarılamaz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="aefb9-127">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aefb9-127">EXAMPLES</span></span>

### <span data-ttu-id="aefb9-128">Örnek 1: anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="aefb9-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="aefb9-129">Bu komut, contoso adlı Anahtar Kasası 'nda ıtsoftware adlı bir yazılım korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="aefb9-130">Örnek 2: HSM korumalı anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="aefb9-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="aefb9-131">Bu komut, contoso adlı anahtar kasasına bir HSM korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="aefb9-132">Örnek 3: varsayılan olmayan değerlerle anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="aefb9-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="aefb9-133">İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="aefb9-134">İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="aefb9-135">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="aefb9-136">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="aefb9-137">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="aefb9-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="aefb9-138">Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="aefb9-139">Bu nesne geçerli UTC zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-139">That object specifies current UTC time.</span></span> <span data-ttu-id="aefb9-140">Komut bu tarihi $NotBefore değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="aefb9-141">Final komutu, bir HSM korumalı anahtar olan Ithsmvarsayıladı adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="aefb9-142">Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="aefb9-143">Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="aefb9-144">Yeni anahtar devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="aefb9-144">The new key is disabled.</span></span> <span data-ttu-id="aefb9-145">**Set-AzureKeyVaultKey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-145">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="aefb9-146">Örnek 4: HSM korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="aefb9-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="aefb9-147">Bu komut, *Keyfilepath* parametresinin belirttiği konumdan ityok adındaki anahtarı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="aefb9-148">İçeri aktarılan anahtar, HSM korumalı bir anahtardır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="aefb9-149">Kendi donanım güvenlik modülünden anahtar içeri aktarmak için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="aefb9-150">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="aefb9-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="aefb9-151">Örnek 5: Yazılım korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="aefb9-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="aefb9-152">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="aefb9-153">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="aefb9-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="aefb9-154">İkinci komut contoso tuş Kasası 'nda bir yazılım parolası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="aefb9-155">Komut, anahtarın konumunu ve $Password depolanan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="aefb9-156">Örnek 6: anahtarı Içeri aktarma ve öznitelikleri atama</span><span class="sxs-lookup"><span data-stu-id="aefb9-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="aefb9-157">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="aefb9-158">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur ve bu nesneyi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="aefb9-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="aefb9-159">Üçüncü komut yüksek önem düzeyi ve etiket ayarlamak için $tags değişkenini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="aefb9-160">Son komutu, anahtarı belirtilen konumdan HSM anahtarı olarak içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="aefb9-161">Komut $Password içinde depolanan $Expires ve parola ile saklanan son kullanma süresini belirtir ve $tags depolanan etiketleri uygular.</span><span class="sxs-lookup"><span data-stu-id="aefb9-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="aefb9-162">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aefb9-162">PARAMETERS</span></span>

### <span data-ttu-id="aefb9-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aefb9-163">-DefaultProfile</span></span>
<span data-ttu-id="aefb9-164">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aefb9-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aefb9-165">-Hedef</span><span class="sxs-lookup"><span data-stu-id="aefb9-165">-Destination</span></span>
<span data-ttu-id="aefb9-166">Anahtarın anahtar kasası hizmetine yazılım korumalı anahtar mı yoksa HSM korumalı anahtar mı ekleneceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="aefb9-167">Geçerli değerler: HSM ve yazılım.</span><span class="sxs-lookup"><span data-stu-id="aefb9-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="aefb9-168">Not: hedef olarak HSM 'yi kullanmak Için, HSMs 'yi destekleyen bir Anahtar Kasası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="aefb9-169">Azure Anahtar Kasası hizmet katmanları ve özellikleri hakkında daha fazla bilgi için, [Azure Anahtar Kasası fiyatlandırma web sitesine](https://go.microsoft.com/fwlink/?linkid=512521)bakın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="aefb9-170">Yeni bir anahtar oluşturduğunuzda bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="aefb9-171">Anahtarı anahtar *FilePath* parametresini kullanarak içeri aktarırsanız, bu parametre isteğe bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="aefb9-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="aefb9-172">Bu parametreyi belirtmezseniz ve bu cmdlet. bYok dosya adı uzantısına sahip bir anahtar aldığında, bu anahtarı HSM korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="aefb9-173">Cmdlet bu anahtarı yazılım korumalı anahtar olarak alamaz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="aefb9-174">Bu parametreyi belirtmezseniz ve bu cmdlet. pfx dosya adı uzantısına sahip bir anahtar aldığında, anahtarı yazılım korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-175">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="aefb9-175">-Disable</span></span>
<span data-ttu-id="aefb9-176">Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="aefb9-177">Anahtarı kullanma girişimleri başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="aefb9-178">Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="aefb9-179">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="aefb9-179">-Expires</span></span>
<span data-ttu-id="aefb9-180">Bu cmdlet 'in eklediği anahtar için, **TarihSaat** nesnesi olarak sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="aefb9-181">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="aefb9-182">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="aefb9-183">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="aefb9-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="aefb9-184">Bu parametreyi belirtmezseniz, anahtar sona ermez.</span><span class="sxs-lookup"><span data-stu-id="aefb9-184">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aefb9-185">-InputObject</span></span>
<span data-ttu-id="aefb9-186">Kasa.</span><span class="sxs-lookup"><span data-stu-id="aefb9-186">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-187">-Anahtardosyasıparolası</span><span class="sxs-lookup"><span data-stu-id="aefb9-187">-KeyFilePassword</span></span>
<span data-ttu-id="aefb9-188">Alınan dosyanın parolasını **SecureString** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="aefb9-189">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="aefb9-190">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="aefb9-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="aefb9-191">Dosya adı uzantısı. pfx olan dosyayı içeri aktarmak için bu parolayı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="aefb9-192">-KeyFilePath</span></span>
<span data-ttu-id="aefb9-193">Bu cmdlet 'in içeri aktardığından kullanılan anahtar malzemesini içeren yerel dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="aefb9-194">Geçerli dosya adı uzantıları. bYok ve. pfx.</span><span class="sxs-lookup"><span data-stu-id="aefb9-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="aefb9-195">Dosya bir. bYok dosyası ise, içeri aktarma sonrasında anahtar HSMs tarafından otomatik olarak korunur ve bu varsayılanı geçersiz kılamazsınız.</span><span class="sxs-lookup"><span data-stu-id="aefb9-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="aefb9-196">Dosya. pfx dosyası ise, içeri aktarma işleminden sonra anahtar yazılım tarafından otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="aefb9-197">Bu varsayılanı geçersiz kılmak için, anahtar HSM korumalı olacak şekilde *hedef* parametreyi HSM 'ye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="aefb9-198">Bu parametreyi belirttiğinizde, *hedef* parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-199">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="aefb9-199">-KeyOps</span></span>
<span data-ttu-id="aefb9-200">Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="aefb9-201">Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="aefb9-202">Bu parametre için kabul edilebilir değerler, [JSON Web anahtarı (JWK) belirtiminde](https://go.microsoft.com/fwlink/?LinkID=613300)tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir:</span><span class="sxs-lookup"><span data-stu-id="aefb9-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="aefb9-203">Şifre</span><span class="sxs-lookup"><span data-stu-id="aefb9-203">Encrypt</span></span>
- <span data-ttu-id="aefb9-204">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="aefb9-204">Decrypt</span></span>
- <span data-ttu-id="aefb9-205">02</span><span class="sxs-lookup"><span data-stu-id="aefb9-205">Wrap</span></span>
- <span data-ttu-id="aefb9-206">Kaydırmamak</span><span class="sxs-lookup"><span data-stu-id="aefb9-206">Unwrap</span></span>
- <span data-ttu-id="aefb9-207">ISS</span><span class="sxs-lookup"><span data-stu-id="aefb9-207">Sign</span></span>
- <span data-ttu-id="aefb9-208">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="aefb9-208">Verify</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-209">-Ad</span><span class="sxs-lookup"><span data-stu-id="aefb9-209">-Name</span></span>
<span data-ttu-id="aefb9-210">Anahtar kasasına eklenecek anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="aefb9-211">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="aefb9-212">Ad, yalnızca 0-9, a-z, A-Z ve-(kesik çizgi simgesi) içeren 1 ila 63 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="aefb9-213">-NotBefore</span></span>
<span data-ttu-id="aefb9-214">Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="aefb9-215">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-215">This parameter uses UTC.</span></span> <span data-ttu-id="aefb9-216">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aefb9-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="aefb9-217">Bu parametreyi belirtmezseniz, tuş hemen kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-217">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-218">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aefb9-218">-ResourceId</span></span>
<span data-ttu-id="aefb9-219">Kasa kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="aefb9-219">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-220">-Boyut</span><span class="sxs-lookup"><span data-stu-id="aefb9-220">-Size</span></span>
<span data-ttu-id="aefb9-221">RSA anahtar boyutu, bit cinsinden.</span><span class="sxs-lookup"><span data-stu-id="aefb9-221">RSA key size, in bits.</span></span> <span data-ttu-id="aefb9-222">Belirtilmezse, hizmet güvenli bir varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="aefb9-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-223">Etiketli</span><span class="sxs-lookup"><span data-stu-id="aefb9-223">-Tag</span></span>
<span data-ttu-id="aefb9-224">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="aefb9-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aefb9-225">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="aefb9-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aefb9-226">-VaultName</span></span>
<span data-ttu-id="aefb9-227">Bu cmdlet 'in anahtarı eklediği Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="aefb9-228">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aefb9-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-229">-Onay</span><span class="sxs-lookup"><span data-stu-id="aefb9-229">-Confirm</span></span>
<span data-ttu-id="aefb9-230">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aefb9-230">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aefb9-231">-WhatIf</span></span>
<span data-ttu-id="aefb9-232">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aefb9-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aefb9-233">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aefb9-233">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aefb9-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aefb9-234">CommonParameters</span></span>
<span data-ttu-id="aefb9-235">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aefb9-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aefb9-236">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aefb9-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aefb9-237">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aefb9-237">INPUTS</span></span>

### <span data-ttu-id="aefb9-238">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="aefb9-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="aefb9-239">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aefb9-239">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="aefb9-240">System. String</span><span class="sxs-lookup"><span data-stu-id="aefb9-240">System.String</span></span>

## <span data-ttu-id="aefb9-241">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aefb9-241">OUTPUTS</span></span>

### <span data-ttu-id="aefb9-242">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aefb9-242">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="aefb9-243">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aefb9-243">NOTES</span></span>

## <span data-ttu-id="aefb9-244">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aefb9-244">RELATED LINKS</span></span>

[<span data-ttu-id="aefb9-245">Yedekleme-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aefb9-245">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="aefb9-246">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aefb9-246">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="aefb9-247">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="aefb9-247">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="aefb9-248">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="aefb9-248">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
