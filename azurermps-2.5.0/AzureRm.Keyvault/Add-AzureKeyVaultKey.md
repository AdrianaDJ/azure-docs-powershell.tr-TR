---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7af5afeac742bf9d256ac16470af0169170eb1e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938852"
---
# <span data-ttu-id="7611e-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7611e-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="7611e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7611e-102">SYNOPSIS</span></span>
<span data-ttu-id="7611e-103">Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasasına anahtar aktarır.</span><span class="sxs-lookup"><span data-stu-id="7611e-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7611e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7611e-104">SYNTAX</span></span>

### <span data-ttu-id="7611e-105">Oluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7611e-105">Create (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7611e-106">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="7611e-106">Import</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7611e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7611e-107">DESCRIPTION</span></span>
<span data-ttu-id="7611e-108">**Add-AzureKeyVaultKey** cmdlet 'ı Azure Anahtar Kasası 'ndaki bir Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasaya bir anahtar aktarır.</span><span class="sxs-lookup"><span data-stu-id="7611e-108">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="7611e-109">Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:</span><span class="sxs-lookup"><span data-stu-id="7611e-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="7611e-110">Anahtar Kasası hizmetinde donanım güvenlik modülünde (HSM) bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7611e-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="7611e-111">Temel kasa hizmetinde yazılımda bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7611e-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="7611e-112">Anahtar Kasası hizmetinde kendi donanım güvenlik modülünden (HSM) bir anahtarı içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="7611e-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="7611e-113">Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="7611e-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="7611e-114">Bilgisayarınızdaki. pfx dosyasındaki bir anahtarı Anahtar Kasası hizmetindeki donanım güvenlik modüllerine (HSMs) aktarın.</span><span class="sxs-lookup"><span data-stu-id="7611e-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="7611e-115">Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7611e-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="7611e-116">Anahtar kasasındaki varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7611e-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="7611e-117">Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7611e-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="7611e-118">Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, Anahtar Kasası REST API belgelerinde [anahtarlar ve gizlilikler hakkında](https://go.microsoft.com/fwlink/?linkid=518560) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7611e-118">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="7611e-119">Not: bir anahtarı kendi donanım güvenlik modülünden içeri aktarmak Için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7611e-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="7611e-120">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="7611e-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="7611e-121">En iyi uygulama olarak, Backup-AzureKeyVaultKey cmdlet 'ini kullanarak, oluşturulduktan veya güncelleştirildikten sonra anahtarınızı yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="7611e-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="7611e-122">Silmeyi geri alma işlevi yapılmaz, bu nedenle anahtarınızı yanlışlıkla sildiğiniz veya silerseniz ve ardından fikir olarak değiştirirseniz, geri yükleyebileceğiniz bir yedeğiniz yoksa anahtar kurtarılamaz.</span><span class="sxs-lookup"><span data-stu-id="7611e-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="7611e-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7611e-123">EXAMPLES</span></span>

### <span data-ttu-id="7611e-124">Örnek 1: anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="7611e-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="7611e-125">Bu komut, contoso adlı Anahtar Kasası 'nda ıtsoftware adlı bir yazılım korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="7611e-126">Örnek 2: HSM korumalı anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="7611e-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="7611e-127">Bu komut, contoso adlı anahtar kasasına bir HSM korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="7611e-128">Örnek 3: varsayılan olmayan değerlerle anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="7611e-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="7611e-129">İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="7611e-130">İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="7611e-131">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="7611e-132">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="7611e-133">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7611e-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="7611e-134">Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7611e-135">Bu nesne geçerli UTC zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-135">That object specifies current UTC time.</span></span> <span data-ttu-id="7611e-136">Komut bu tarihi $NotBefore değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="7611e-137">Final komutu, bir HSM korumalı anahtar olan Ithsmvarsayıladı adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="7611e-138">Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="7611e-139">Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="7611e-140">Yeni anahtar devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="7611e-140">The new key is disabled.</span></span> <span data-ttu-id="7611e-141">**Set-AzureKeyVaultKey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7611e-141">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="7611e-142">Örnek 4: HSM korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="7611e-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="7611e-143">Bu komut, *Keyfilepath* parametresinin belirttiği konumdan ityok adındaki anahtarı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="7611e-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="7611e-144">İçeri aktarılan anahtar, HSM korumalı bir anahtardır.</span><span class="sxs-lookup"><span data-stu-id="7611e-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="7611e-145">Kendi donanım güvenlik modülünden anahtar içeri aktarmak için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7611e-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="7611e-146">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="7611e-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="7611e-147">Örnek 5: Yazılım korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="7611e-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="7611e-148">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="7611e-149">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="7611e-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="7611e-150">İkinci komut contoso tuş Kasası 'nda bir yazılım parolası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="7611e-151">Komut, anahtarın konumunu ve $Password depolanan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="7611e-152">Örnek 6: anahtarı Içeri aktarma ve öznitelikleri atama</span><span class="sxs-lookup"><span data-stu-id="7611e-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="7611e-153">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="7611e-154">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur ve bu nesneyi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7611e-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="7611e-155">Üçüncü komut yüksek önem düzeyi ve etiket ayarlamak için $tags değişkenini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="7611e-156">Son komutu, anahtarı belirtilen konumdan HSM anahtarı olarak içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="7611e-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="7611e-157">Komut $Password içinde depolanan $Expires ve parola ile saklanan son kullanma süresini belirtir ve $tags depolanan etiketleri uygular.</span><span class="sxs-lookup"><span data-stu-id="7611e-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="7611e-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7611e-158">PARAMETERS</span></span>

### <span data-ttu-id="7611e-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7611e-159">-DefaultProfile</span></span>
<span data-ttu-id="7611e-160">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7611e-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7611e-161">-Hedef</span><span class="sxs-lookup"><span data-stu-id="7611e-161">-Destination</span></span>
<span data-ttu-id="7611e-162">Anahtarın anahtar kasası hizmetine yazılım korumalı anahtar mı yoksa HSM korumalı anahtar mı ekleneceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="7611e-163">Geçerli değerler: HSM ve yazılım.</span><span class="sxs-lookup"><span data-stu-id="7611e-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="7611e-164">Not: hedef olarak HSM 'yi kullanmak Için, HSMs 'yi destekleyen bir Anahtar Kasası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7611e-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="7611e-165">Azure Anahtar Kasası hizmet katmanları ve özellikleri hakkında daha fazla bilgi için, [Azure Anahtar Kasası fiyatlandırma web sitesine](https://go.microsoft.com/fwlink/?linkid=512521)bakın.</span><span class="sxs-lookup"><span data-stu-id="7611e-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="7611e-166">Yeni bir anahtar oluşturduğunuzda bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7611e-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="7611e-167">Anahtarı anahtar *FilePath* parametresini kullanarak içeri aktarırsanız, bu parametre isteğe bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="7611e-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="7611e-168">Bu parametreyi belirtmezseniz ve bu cmdlet. bYok dosya adı uzantısına sahip bir anahtar aldığında, bu anahtarı HSM korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="7611e-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="7611e-169">Cmdlet bu anahtarı yazılım korumalı anahtar olarak alamaz.</span><span class="sxs-lookup"><span data-stu-id="7611e-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="7611e-170">Bu parametreyi belirtmezseniz ve bu cmdlet. pfx dosya adı uzantısına sahip bir anahtar aldığında, anahtarı yazılım korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="7611e-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-171">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="7611e-171">-Disable</span></span>
<span data-ttu-id="7611e-172">Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7611e-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="7611e-173">Anahtarı kullanma girişimleri başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="7611e-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="7611e-174">Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="7611e-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="7611e-175">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="7611e-175">-Expires</span></span>
<span data-ttu-id="7611e-176">Bu cmdlet 'in eklediği anahtar için, **TarihSaat** nesnesi olarak sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="7611e-177">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="7611e-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7611e-178">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7611e-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7611e-179">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7611e-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="7611e-180">Bu parametreyi belirtmezseniz, anahtar sona ermez.</span><span class="sxs-lookup"><span data-stu-id="7611e-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-181">-Anahtardosyasıparolası</span><span class="sxs-lookup"><span data-stu-id="7611e-181">-KeyFilePassword</span></span>
<span data-ttu-id="7611e-182">Alınan dosyanın parolasını **SecureString** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="7611e-183">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7611e-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="7611e-184">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="7611e-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="7611e-185">Dosya adı uzantısı. pfx olan dosyayı içeri aktarmak için bu parolayı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7611e-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="7611e-186">-KeyFilePath</span></span>
<span data-ttu-id="7611e-187">Bu cmdlet 'in içeri aktardığından kullanılan anahtar malzemesini içeren yerel dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="7611e-188">Geçerli dosya adı uzantıları. bYok ve. pfx.</span><span class="sxs-lookup"><span data-stu-id="7611e-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="7611e-189">Dosya bir. bYok dosyası ise, içeri aktarma sonrasında anahtar HSMs tarafından otomatik olarak korunur ve bu varsayılanı geçersiz kılamazsınız.</span><span class="sxs-lookup"><span data-stu-id="7611e-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="7611e-190">Dosya. pfx dosyası ise, içeri aktarma işleminden sonra anahtar yazılım tarafından otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="7611e-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="7611e-191">Bu varsayılanı geçersiz kılmak için, anahtar HSM korumalı olacak şekilde *hedef* parametreyi HSM 'ye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7611e-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="7611e-192">Bu parametreyi belirttiğinizde, *hedef* parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7611e-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-193">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="7611e-193">-KeyOps</span></span>
<span data-ttu-id="7611e-194">Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="7611e-195">Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7611e-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="7611e-196">Bu parametre için kabul edilebilir değerler, [JSON Web anahtarı (JWK) belirtiminde](https://go.microsoft.com/fwlink/?LinkID=613300)tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir:</span><span class="sxs-lookup"><span data-stu-id="7611e-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="7611e-197">Şifre</span><span class="sxs-lookup"><span data-stu-id="7611e-197">Encrypt</span></span>
- <span data-ttu-id="7611e-198">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="7611e-198">Decrypt</span></span>
- <span data-ttu-id="7611e-199">02</span><span class="sxs-lookup"><span data-stu-id="7611e-199">Wrap</span></span>
- <span data-ttu-id="7611e-200">Kaydırmamak</span><span class="sxs-lookup"><span data-stu-id="7611e-200">Unwrap</span></span>
- <span data-ttu-id="7611e-201">ISS</span><span class="sxs-lookup"><span data-stu-id="7611e-201">Sign</span></span>
- <span data-ttu-id="7611e-202">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="7611e-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-203">-Ad</span><span class="sxs-lookup"><span data-stu-id="7611e-203">-Name</span></span>
<span data-ttu-id="7611e-204">Anahtar kasasına eklenecek anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="7611e-205">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="7611e-206">Ad, yalnızca 0-9, a-z, A-Z ve-(kesik çizgi simgesi) içeren 1 ila 63 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7611e-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="7611e-207">-NotBefore</span></span>
<span data-ttu-id="7611e-208">Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="7611e-209">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="7611e-209">This parameter uses UTC.</span></span> <span data-ttu-id="7611e-210">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7611e-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7611e-211">Bu parametreyi belirtmezseniz, tuş hemen kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7611e-211">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-212">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7611e-212">-Tag</span></span>
<span data-ttu-id="7611e-213">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7611e-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7611e-214">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7611e-214">For example:</span></span>

<span data-ttu-id="7611e-215">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7611e-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7611e-216">-VaultName</span></span>
<span data-ttu-id="7611e-217">Bu cmdlet 'in anahtarı eklediği Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7611e-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="7611e-218">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7611e-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="7611e-219">-Onay</span><span class="sxs-lookup"><span data-stu-id="7611e-219">-Confirm</span></span>
<span data-ttu-id="7611e-220">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7611e-220">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7611e-221">-WhatIf</span></span>
<span data-ttu-id="7611e-222">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7611e-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7611e-223">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7611e-223">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7611e-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7611e-224">CommonParameters</span></span>
<span data-ttu-id="7611e-225">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7611e-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7611e-226">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7611e-226">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7611e-227">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7611e-227">INPUTS</span></span>

## <span data-ttu-id="7611e-228">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7611e-228">OUTPUTS</span></span>

### <span data-ttu-id="7611e-229">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="7611e-229">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="7611e-230">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7611e-230">NOTES</span></span>

## <span data-ttu-id="7611e-231">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7611e-231">RELATED LINKS</span></span>

[<span data-ttu-id="7611e-232">Yedekleme-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7611e-232">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="7611e-233">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7611e-233">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="7611e-234">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7611e-234">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="7611e-235">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="7611e-235">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
