---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936678"
---
# <span data-ttu-id="4bafc-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bafc-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="4bafc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bafc-102">SYNOPSIS</span></span>
<span data-ttu-id="4bafc-103">Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasasına anahtar aktarır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="4bafc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bafc-104">SYNTAX</span></span>

### <span data-ttu-id="4bafc-105">Oluştur (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bafc-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bafc-106">Aktarılacağı</span><span class="sxs-lookup"><span data-stu-id="4bafc-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bafc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bafc-107">DESCRIPTION</span></span>
<span data-ttu-id="4bafc-108">**Add-Azanahtarvaultkey** cmdlet 'ı Azure Anahtar Kasası 'ndaki bir Anahtar Kasası içinde bir anahtar oluşturur veya bir anahtarı anahtar kasasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="4bafc-109">Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:</span><span class="sxs-lookup"><span data-stu-id="4bafc-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="4bafc-110">Anahtar Kasası hizmetinde donanım güvenlik modülünde (HSM) bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4bafc-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="4bafc-111">Temel kasa hizmetinde yazılımda bir anahtar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4bafc-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="4bafc-112">Anahtar Kasası hizmetinde kendi donanım güvenlik modülünden (HSM) bir anahtarı içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="4bafc-113">Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="4bafc-114">Bilgisayarınızdaki. pfx dosyasındaki bir anahtarı Anahtar Kasası hizmetindeki donanım güvenlik modüllerine (HSMs) aktarın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="4bafc-115">Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="4bafc-116">Anahtar kasasındaki varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="4bafc-117">Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="4bafc-118">Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, Anahtar Kasası REST API belgelerinde [anahtarlar ve gizlilikler hakkında](http://go.microsoft.com/fwlink/?linkid=518560) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="4bafc-119">Not: bir anahtarı kendi donanım güvenlik modülünden içeri aktarmak Için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="4bafc-120">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="4bafc-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="4bafc-121">En iyi uygulama olarak, Backup-AzKeyVaultKey cmdlet 'ini kullanarak, oluşturulduktan veya güncelleştirildikten sonra anahtarınızı yedekleyin.</span><span class="sxs-lookup"><span data-stu-id="4bafc-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="4bafc-122">Silmeyi geri alma işlevi yapılmaz, bu nedenle anahtarınızı yanlışlıkla sildiğiniz veya silerseniz ve ardından fikir olarak değiştirirseniz, geri yükleyebileceğiniz bir yedeğiniz yoksa anahtar kurtarılamaz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="4bafc-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bafc-123">EXAMPLES</span></span>

### <span data-ttu-id="4bafc-124">Örnek 1: anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bafc-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="4bafc-125">Bu komut, contoso adlı Anahtar Kasası 'nda ıtsoftware adlı bir yazılım korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="4bafc-126">Örnek 2: HSM korumalı anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bafc-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="4bafc-127">Bu komut, contoso adlı anahtar kasasına bir HSM korumalı anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="4bafc-128">Örnek 3: varsayılan olmayan değerlerle anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4bafc-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="4bafc-129">İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="4bafc-130">İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="4bafc-131">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="4bafc-132">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="4bafc-133">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4bafc-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="4bafc-134">Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4bafc-135">Bu nesne geçerli UTC zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-135">That object specifies current UTC time.</span></span> <span data-ttu-id="4bafc-136">Komut bu tarihi $NotBefore değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="4bafc-137">Final komutu, bir HSM korumalı anahtar olan Ithsmvarsayıladı adlı bir anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="4bafc-138">Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="4bafc-139">Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="4bafc-140">Yeni anahtar devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="4bafc-140">The new key is disabled.</span></span> <span data-ttu-id="4bafc-141">**Set-Azanahtarvaultkey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="4bafc-142">Örnek 4: HSM korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="4bafc-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="4bafc-143">Bu komut, *Keyfilepath* parametresinin belirttiği konumdan ityok adındaki anahtarı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="4bafc-144">İçeri aktarılan anahtar, HSM korumalı bir anahtardır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="4bafc-145">Kendi donanım güvenlik modülünden anahtar içeri aktarmak için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="4bafc-146">Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="4bafc-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="4bafc-147">Örnek 5: Yazılım korumalı bir anahtarı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="4bafc-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="4bafc-148">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="4bafc-149">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4bafc-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="4bafc-150">İkinci komut contoso tuş Kasası 'nda bir yazılım parolası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="4bafc-151">Komut, anahtarın konumunu ve $Password depolanan parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="4bafc-152">Örnek 6: anahtarı Içeri aktarma ve öznitelikleri atama</span><span class="sxs-lookup"><span data-stu-id="4bafc-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="4bafc-153">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="4bafc-154">İkinci komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur ve bu nesneyi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4bafc-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="4bafc-155">Üçüncü komut yüksek önem düzeyi ve etiket ayarlamak için $tags değişkenini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="4bafc-156">Son komutu, anahtarı belirtilen konumdan HSM anahtarı olarak içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="4bafc-157">Komut $Password içinde depolanan $Expires ve parola ile saklanan son kullanma süresini belirtir ve $tags depolanan etiketleri uygular.</span><span class="sxs-lookup"><span data-stu-id="4bafc-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="4bafc-158">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bafc-158">PARAMETERS</span></span>

### <span data-ttu-id="4bafc-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bafc-159">-DefaultProfile</span></span>
<span data-ttu-id="4bafc-160">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4bafc-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bafc-161">-Hedef</span><span class="sxs-lookup"><span data-stu-id="4bafc-161">-Destination</span></span>
<span data-ttu-id="4bafc-162">Anahtarın anahtar kasası hizmetine yazılım korumalı anahtar mı yoksa HSM korumalı anahtar mı ekleneceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="4bafc-163">Geçerli değerler: HSM ve yazılım.</span><span class="sxs-lookup"><span data-stu-id="4bafc-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="4bafc-164">Not: hedef olarak HSM 'yi kullanmak Için, HSMs 'yi destekleyen bir Anahtar Kasası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="4bafc-165">Azure Anahtar Kasası hizmet katmanları ve özellikleri hakkında daha fazla bilgi için, [Azure Anahtar Kasası fiyatlandırma web sitesine](http://go.microsoft.com/fwlink/?linkid=512521)bakın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="4bafc-166">Yeni bir anahtar oluşturduğunuzda bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="4bafc-167">Anahtarı anahtar *FilePath* parametresini kullanarak içeri aktarırsanız, bu parametre isteğe bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="4bafc-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="4bafc-168">Bu parametreyi belirtmezseniz ve bu cmdlet. bYok dosya adı uzantısına sahip bir anahtar aldığında, bu anahtarı HSM korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="4bafc-169">Cmdlet bu anahtarı yazılım korumalı anahtar olarak alamaz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="4bafc-170">Bu parametreyi belirtmezseniz ve bu cmdlet. pfx dosya adı uzantısına sahip bir anahtar aldığında, anahtarı yazılım korumalı anahtar olarak alır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="4bafc-171">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="4bafc-171">-Disable</span></span>
<span data-ttu-id="4bafc-172">Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="4bafc-173">Anahtarı kullanma girişimleri başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="4bafc-174">Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="4bafc-175">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="4bafc-175">-Expires</span></span>
<span data-ttu-id="4bafc-176">Bu cmdlet 'in eklediği anahtar için, **TarihSaat** nesnesi olarak sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="4bafc-177">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="4bafc-178">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4bafc-179">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="4bafc-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="4bafc-180">Bu parametreyi belirtmezseniz, anahtar sona ermez.</span><span class="sxs-lookup"><span data-stu-id="4bafc-180">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="4bafc-181">-Anahtardosyasıparolası</span><span class="sxs-lookup"><span data-stu-id="4bafc-181">-KeyFilePassword</span></span>
<span data-ttu-id="4bafc-182">Alınan dosyanın parolasını **SecureString** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="4bafc-183">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="4bafc-184">Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4bafc-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="4bafc-185">Dosya adı uzantısı. pfx olan dosyayı içeri aktarmak için bu parolayı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="4bafc-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="4bafc-186">-KeyFilePath</span></span>
<span data-ttu-id="4bafc-187">Bu cmdlet 'in içeri aktardığından kullanılan anahtar malzemesini içeren yerel dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="4bafc-188">Geçerli dosya adı uzantıları. bYok ve. pfx.</span><span class="sxs-lookup"><span data-stu-id="4bafc-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="4bafc-189">Dosya bir. bYok dosyası ise, içeri aktarma sonrasında anahtar HSMs tarafından otomatik olarak korunur ve bu varsayılanı geçersiz kılamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4bafc-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="4bafc-190">Dosya. pfx dosyası ise, içeri aktarma işleminden sonra anahtar yazılım tarafından otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="4bafc-191">Bu varsayılanı geçersiz kılmak için, anahtar HSM korumalı olacak şekilde *hedef* parametreyi HSM 'ye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="4bafc-192">Bu parametreyi belirttiğinizde, *hedef* parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="4bafc-193">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="4bafc-193">-KeyOps</span></span>
<span data-ttu-id="4bafc-194">Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="4bafc-195">Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="4bafc-196">Bu parametre için kabul edilebilir değerler, [JSON Web anahtarı (JWK) belirtiminde](http://go.microsoft.com/fwlink/?LinkID=613300)tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir:</span><span class="sxs-lookup"><span data-stu-id="4bafc-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="4bafc-197">Şifre</span><span class="sxs-lookup"><span data-stu-id="4bafc-197">Encrypt</span></span>
- <span data-ttu-id="4bafc-198">Çözmeye</span><span class="sxs-lookup"><span data-stu-id="4bafc-198">Decrypt</span></span>
- <span data-ttu-id="4bafc-199">02</span><span class="sxs-lookup"><span data-stu-id="4bafc-199">Wrap</span></span>
- <span data-ttu-id="4bafc-200">Kaydırmamak</span><span class="sxs-lookup"><span data-stu-id="4bafc-200">Unwrap</span></span>
- <span data-ttu-id="4bafc-201">ISS</span><span class="sxs-lookup"><span data-stu-id="4bafc-201">Sign</span></span>
- <span data-ttu-id="4bafc-202">Ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="4bafc-202">Verify</span></span>

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

### <span data-ttu-id="4bafc-203">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bafc-203">-Name</span></span>
<span data-ttu-id="4bafc-204">Anahtar kasasına eklenecek anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="4bafc-205">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="4bafc-206">Ad, yalnızca 0-9, a-z, A-Z ve-(kesik çizgi simgesi) içeren 1 ila 63 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="4bafc-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="4bafc-207">-NotBefore</span></span>
<span data-ttu-id="4bafc-208">Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="4bafc-209">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="4bafc-209">This parameter uses UTC.</span></span> <span data-ttu-id="4bafc-210">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4bafc-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="4bafc-211">Bu parametreyi belirtmezseniz, tuş hemen kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-211">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="4bafc-212">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4bafc-212">-Tag</span></span>
<span data-ttu-id="4bafc-213">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4bafc-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4bafc-214">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4bafc-214">For example:</span></span>

<span data-ttu-id="4bafc-215">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4bafc-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4bafc-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4bafc-216">-VaultName</span></span>
<span data-ttu-id="4bafc-217">Bu cmdlet 'in anahtarı eklediği Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="4bafc-218">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4bafc-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="4bafc-219">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bafc-219">-Confirm</span></span>
<span data-ttu-id="4bafc-220">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bafc-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bafc-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bafc-221">-WhatIf</span></span>
<span data-ttu-id="4bafc-222">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bafc-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bafc-223">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bafc-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bafc-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bafc-224">CommonParameters</span></span>
<span data-ttu-id="4bafc-225">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bafc-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bafc-226">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bafc-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bafc-227">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bafc-227">INPUTS</span></span>

### <span data-ttu-id="4bafc-228">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4bafc-228">None</span></span>
<span data-ttu-id="4bafc-229">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4bafc-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bafc-230">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bafc-230">OUTPUTS</span></span>

### <span data-ttu-id="4bafc-231">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="4bafc-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="4bafc-232">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bafc-232">NOTES</span></span>

## <span data-ttu-id="4bafc-233">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bafc-233">RELATED LINKS</span></span>

[<span data-ttu-id="4bafc-234">Yedek-Aztuş Vaultkey</span><span class="sxs-lookup"><span data-stu-id="4bafc-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="4bafc-235">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="4bafc-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="4bafc-236">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4bafc-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="4bafc-237">Set-Azanahtarvaultkeyattribute</span><span class="sxs-lookup"><span data-stu-id="4bafc-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
