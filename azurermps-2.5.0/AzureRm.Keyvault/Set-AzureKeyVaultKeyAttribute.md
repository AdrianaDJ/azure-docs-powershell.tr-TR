---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939546"
---
# <span data-ttu-id="728a5-101">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="728a5-101">Set-AzureKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="728a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="728a5-102">SYNOPSIS</span></span>
<span data-ttu-id="728a5-103">Anahtar kasasındaki bir anahtarın özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="728a5-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="728a5-104">SYNTAX</span></span>

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="728a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="728a5-105">DESCRIPTION</span></span>
<span data-ttu-id="728a5-106">**Set-AzureKeyVaultKeyAttribute** cmdlet 'i anahtar kasasındaki bir anahtarın düzenlenebilir özniteliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="728a5-106">The **Set-AzureKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="728a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="728a5-107">EXAMPLES</span></span>

### <span data-ttu-id="728a5-108">Örnek 1: etkinleştirmek için anahtarı değiştirme ve son kullanma tarihi ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="728a5-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="728a5-109">İlk komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="728a5-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="728a5-110">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="728a5-111">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="728a5-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="728a5-112">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="728a5-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="728a5-113">İkinci komut, yüksek önem düzeyi ve hesap oluşturma etiket değerlerini depolamak için bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="728a5-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="728a5-114">Son komutu ITSoftware adındaki bir anahtarı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="728a5-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="728a5-115">Komut, anahtarı belirler, kullanım süresi sonunu $Expires depolanan saate göre ayarlar ve $Tags depolanan etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="728a5-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="728a5-116">Örnek 2: tüm etiketleri silmek için anahtarı değiştirme</span><span class="sxs-lookup"><span data-stu-id="728a5-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="728a5-117">Bu komut, bir anahtarın ıtsoftware adındaki belirli bir sürümünün tüm etiketlerini siler.</span><span class="sxs-lookup"><span data-stu-id="728a5-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="728a5-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="728a5-118">PARAMETERS</span></span>

### <span data-ttu-id="728a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728a5-119">-DefaultProfile</span></span>
<span data-ttu-id="728a5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="728a5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="728a5-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="728a5-121">-Enable</span></span>
<span data-ttu-id="728a5-122">Bir tuşun etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="728a5-123">Anahtarı $True değeri etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="728a5-123">A value of $True enables the key.</span></span> <span data-ttu-id="728a5-124">$False değeri devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="728a5-124">A value of $False disables the key.</span></span> <span data-ttu-id="728a5-125">Bu parametreyi belirtmezseniz, bu cmdlet anahtarın durumunu değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="728a5-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

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

### <span data-ttu-id="728a5-126">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="728a5-126">-Expires</span></span>
<span data-ttu-id="728a5-127">Bu cmdlet 'in güncelleştirdiği anahtar için **DateTime** nesnesi olarak süre sonu belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="728a5-128">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="728a5-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="728a5-129">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="728a5-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="728a5-130">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="728a5-130">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="728a5-131">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="728a5-131">-KeyOps</span></span>
<span data-ttu-id="728a5-132">Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="728a5-133">Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="728a5-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="728a5-134">Bu parametre için kabul edilebilir değerler, JSON Web anahtar belirtiminde tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir.</span><span class="sxs-lookup"><span data-stu-id="728a5-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="728a5-135">Bu değerler (büyük/küçük harf duyarlı):</span><span class="sxs-lookup"><span data-stu-id="728a5-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="728a5-136">şifre</span><span class="sxs-lookup"><span data-stu-id="728a5-136">encrypt</span></span>
- <span data-ttu-id="728a5-137">çözmeye</span><span class="sxs-lookup"><span data-stu-id="728a5-137">decrypt</span></span>
- <span data-ttu-id="728a5-138">02</span><span class="sxs-lookup"><span data-stu-id="728a5-138">wrap</span></span>
- <span data-ttu-id="728a5-139">kaydırmamak</span><span class="sxs-lookup"><span data-stu-id="728a5-139">unwrap</span></span>
- <span data-ttu-id="728a5-140">ISS</span><span class="sxs-lookup"><span data-stu-id="728a5-140">sign</span></span>
- <span data-ttu-id="728a5-141">ayarlandığını</span><span class="sxs-lookup"><span data-stu-id="728a5-141">verify</span></span>
- <span data-ttu-id="728a5-142">yedeğinin</span><span class="sxs-lookup"><span data-stu-id="728a5-142">backup</span></span>
- <span data-ttu-id="728a5-143">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="728a5-143">restore</span></span>

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

### <span data-ttu-id="728a5-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="728a5-144">-Name</span></span>
<span data-ttu-id="728a5-145">Güncelleştirilecek anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="728a5-146">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="728a5-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="728a5-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="728a5-147">-NotBefore</span></span>
<span data-ttu-id="728a5-148">Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="728a5-149">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="728a5-149">This parameter uses UTC.</span></span>
<span data-ttu-id="728a5-150">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="728a5-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="728a5-151">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="728a5-151">-PassThru</span></span>
<span data-ttu-id="728a5-152">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="728a5-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="728a5-153">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="728a5-153">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="728a5-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="728a5-154">-Tag</span></span>
<span data-ttu-id="728a5-155">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="728a5-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="728a5-156">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="728a5-156">For example:</span></span>

<span data-ttu-id="728a5-157">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="728a5-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="728a5-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="728a5-158">-VaultName</span></span>
<span data-ttu-id="728a5-159">Bu cmdlet 'in anahtarı değiştirdiği Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="728a5-160">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="728a5-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="728a5-161">-Version</span><span class="sxs-lookup"><span data-stu-id="728a5-161">-Version</span></span>
<span data-ttu-id="728a5-162">Anahtar sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="728a5-162">Specifies the key version.</span></span>
<span data-ttu-id="728a5-163">Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="728a5-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="728a5-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="728a5-164">-Confirm</span></span>
<span data-ttu-id="728a5-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="728a5-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="728a5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="728a5-166">-WhatIf</span></span>
<span data-ttu-id="728a5-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="728a5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="728a5-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="728a5-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="728a5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728a5-169">CommonParameters</span></span>
<span data-ttu-id="728a5-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="728a5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728a5-171">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728a5-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728a5-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="728a5-172">INPUTS</span></span>

## <span data-ttu-id="728a5-173">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="728a5-173">OUTPUTS</span></span>

### <span data-ttu-id="728a5-174">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="728a5-174">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="728a5-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="728a5-175">NOTES</span></span>

## <span data-ttu-id="728a5-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="728a5-176">RELATED LINKS</span></span>

[<span data-ttu-id="728a5-177">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="728a5-177">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="728a5-178">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="728a5-178">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="728a5-179">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="728a5-179">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)
