---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultKeyAttribute.md
ms.openlocfilehash: 4b9799a0d2433b513b801a95ffd5c408bf8bdbf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590457"
---
# <span data-ttu-id="9fa51-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="9fa51-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="9fa51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fa51-102">SYNOPSIS</span></span>
<span data-ttu-id="9fa51-103">Anahtar kasasındaki bir anahtarın özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fa51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fa51-104">SYNTAX</span></span>

### <span data-ttu-id="9fa51-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fa51-105">Default (Default)</span></span>
```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fa51-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa51-106">InputObject</span></span>
```
Set-AzureKeyVaultKeyAttribute [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fa51-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fa51-107">DESCRIPTION</span></span>
<span data-ttu-id="9fa51-108">**Set-AzureKeyVaultKeyAttribute** cmdlet 'i anahtar kasasındaki bir anahtarın düzenlenebilir özniteliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="9fa51-108">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="9fa51-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fa51-109">EXAMPLES</span></span>

### <span data-ttu-id="9fa51-110">Örnek 1: etkinleştirmek için anahtarı değiştirme ve son kullanma tarihi ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="9fa51-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="9fa51-111">İlk komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fa51-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9fa51-112">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="9fa51-113">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9fa51-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="9fa51-114">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9fa51-114">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9fa51-115">İkinci komut, yüksek önem düzeyi ve hesap oluşturma etiket değerlerini depolamak için bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fa51-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="9fa51-116">Son komutu ITSoftware adındaki bir anahtarı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="9fa51-117">Komut, anahtarı belirler, kullanım süresi sonunu $Expires depolanan saate göre ayarlar ve $Tags depolanan etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9fa51-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="9fa51-118">Örnek 2: tüm etiketleri silmek için anahtarı değiştirme</span><span class="sxs-lookup"><span data-stu-id="9fa51-118">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="9fa51-119">Bu komut, bir anahtarın ıtsoftware adındaki belirli bir sürümünün tüm etiketlerini siler.</span><span class="sxs-lookup"><span data-stu-id="9fa51-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="9fa51-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fa51-120">PARAMETERS</span></span>

### <span data-ttu-id="9fa51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fa51-121">-DefaultProfile</span></span>
<span data-ttu-id="9fa51-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9fa51-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fa51-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="9fa51-123">-Enable</span></span>
<span data-ttu-id="9fa51-124">Bir tuşun etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-124">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="9fa51-125">Anahtarı $True değeri etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-125">A value of $True enables the key.</span></span> <span data-ttu-id="9fa51-126">$False değeri devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="9fa51-126">A value of $False disables the key.</span></span> <span data-ttu-id="9fa51-127">Bu parametreyi belirtmezseniz, bu cmdlet anahtarın durumunu değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="9fa51-127">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fa51-128">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="9fa51-128">-Expires</span></span>
<span data-ttu-id="9fa51-129">Bu cmdlet 'in güncelleştirdiği anahtar için **DateTime** nesnesi olarak süre sonu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-129">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="9fa51-130">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="9fa51-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9fa51-131">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fa51-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9fa51-132">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9fa51-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="9fa51-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fa51-133">-InputObject</span></span>
<span data-ttu-id="9fa51-134">Anahtar nesnesi</span><span class="sxs-lookup"><span data-stu-id="9fa51-134">Key object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa51-135">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="9fa51-135">-KeyOps</span></span>
<span data-ttu-id="9fa51-136">Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-136">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="9fa51-137">Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-137">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="9fa51-138">Bu parametre için kabul edilebilir değerler, JSON Web anahtar belirtiminde tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-138">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="9fa51-139">Bu değerler (büyük/küçük harf duyarlı):</span><span class="sxs-lookup"><span data-stu-id="9fa51-139">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="9fa51-140">şifre</span><span class="sxs-lookup"><span data-stu-id="9fa51-140">encrypt</span></span>
- <span data-ttu-id="9fa51-141">çözmeye</span><span class="sxs-lookup"><span data-stu-id="9fa51-141">decrypt</span></span>
- <span data-ttu-id="9fa51-142">02</span><span class="sxs-lookup"><span data-stu-id="9fa51-142">wrap</span></span>
- <span data-ttu-id="9fa51-143">kaydırmamak</span><span class="sxs-lookup"><span data-stu-id="9fa51-143">unwrap</span></span>
- <span data-ttu-id="9fa51-144">ISS</span><span class="sxs-lookup"><span data-stu-id="9fa51-144">sign</span></span>
- <span data-ttu-id="9fa51-145">ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="9fa51-145">verify</span></span>
- <span data-ttu-id="9fa51-146">yedeğinin</span><span class="sxs-lookup"><span data-stu-id="9fa51-146">backup</span></span>
- <span data-ttu-id="9fa51-147">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="9fa51-147">restore</span></span>

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

### <span data-ttu-id="9fa51-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fa51-148">-Name</span></span>
<span data-ttu-id="9fa51-149">Güncelleştirilecek anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-149">Specifies the name of the key to update.</span></span> <span data-ttu-id="9fa51-150">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fa51-150">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa51-151">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9fa51-151">-NotBefore</span></span>
<span data-ttu-id="9fa51-152">Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-152">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="9fa51-153">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="9fa51-153">This parameter uses UTC.</span></span>
<span data-ttu-id="9fa51-154">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9fa51-154">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="9fa51-155">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9fa51-155">-PassThru</span></span>
<span data-ttu-id="9fa51-156">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9fa51-156">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9fa51-157">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9fa51-157">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9fa51-158">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9fa51-158">-Tag</span></span>
<span data-ttu-id="9fa51-159">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="9fa51-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9fa51-160">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="9fa51-160">For example:</span></span>

<span data-ttu-id="9fa51-161">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9fa51-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9fa51-162">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9fa51-162">-VaultName</span></span>
<span data-ttu-id="9fa51-163">Bu cmdlet 'in anahtarı değiştirdiği Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-163">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="9fa51-164">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fa51-164">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="9fa51-165">-Version</span><span class="sxs-lookup"><span data-stu-id="9fa51-165">-Version</span></span>
<span data-ttu-id="9fa51-166">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-166">Specifies the key version.</span></span>
<span data-ttu-id="9fa51-167">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fa51-167">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fa51-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fa51-168">-Confirm</span></span>
<span data-ttu-id="9fa51-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fa51-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fa51-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fa51-170">-WhatIf</span></span>
<span data-ttu-id="9fa51-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fa51-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fa51-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fa51-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fa51-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fa51-173">CommonParameters</span></span>
<span data-ttu-id="9fa51-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fa51-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fa51-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fa51-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fa51-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fa51-176">INPUTS</span></span>

### <span data-ttu-id="9fa51-177">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9fa51-177">None</span></span>
<span data-ttu-id="9fa51-178">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9fa51-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9fa51-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fa51-179">OUTPUTS</span></span>

### <span data-ttu-id="9fa51-180">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9fa51-180">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="9fa51-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fa51-181">NOTES</span></span>

## <span data-ttu-id="9fa51-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fa51-182">RELATED LINKS</span></span>

[<span data-ttu-id="9fa51-183">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9fa51-183">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="9fa51-184">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9fa51-184">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="9fa51-185">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9fa51-185">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
