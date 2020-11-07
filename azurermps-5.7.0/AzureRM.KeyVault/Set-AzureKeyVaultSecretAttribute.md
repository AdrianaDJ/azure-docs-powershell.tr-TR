---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764705"
---
# <span data-ttu-id="46453-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="46453-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="46453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46453-102">SYNOPSIS</span></span>
<span data-ttu-id="46453-103">Anahtar kasasındaki gizli öznitelikleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="46453-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46453-104">SYNTAX</span></span>

### <span data-ttu-id="46453-105">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="46453-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46453-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="46453-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46453-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="46453-107">DESCRIPTION</span></span>
<span data-ttu-id="46453-108">**Set-AzureKeyVaultSecretAttribute** cmdlet 'i anahtar kasasındaki bir gizli kod öğesinin düzenlenebilir özniteliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="46453-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="46453-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46453-109">EXAMPLES</span></span>

### <span data-ttu-id="46453-110">Örnek 1: parolayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="46453-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="46453-111">İlk dört komut son kullanma tarihi, Notöncesi tarihi, etiketleri ve bağlam türü özniteliklerini tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="46453-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="46453-112">Son komutu, depolanan değişkenleri kullanarak, Contosokasası adlı anahtar kasasına ık adlı parola ile ilgili öznitelikleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46453-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="46453-113">Örnek 2: gizli için etiketleri ve içerik türünü silme</span><span class="sxs-lookup"><span data-stu-id="46453-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="46453-114">Bu komut, contoso adlı anahtar kasasına HR adlı parola adlı gizli sürümün etiketlerini ve içerik türünü siler.</span><span class="sxs-lookup"><span data-stu-id="46453-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="46453-115">Örnek 3: adı bununla başlayan gizli kod sürümlerini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="46453-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="46453-116">İlk komut $Vault değişkeninde contoso dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="46453-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="46453-117">İkinci komut, $Prefix değişkeninde dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="46453-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="46453-118">Üçüncü komut, Get-AzureKeyVaultSecret cmdlet 'ini kullanarak belirtilen anahtar kasasındaki gizlilikleri alır ve bu gizlilikleri **WHERE-Object** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="46453-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="46453-119">**WHERE-Object** cmdlet 'i, adlarla başlayan adlarla ilgili gizli kod dizelerini süzer.</span><span class="sxs-lookup"><span data-stu-id="46453-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="46453-120">Komut, filtreyle eşleşen gizli kod dizelerini devre dışı bırakan Set-AzureKeyVaultSecretAttribute cmdlet 'ine göre yöneltme içerir.</span><span class="sxs-lookup"><span data-stu-id="46453-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="46453-121">Örnek 4: tüm gizli sürümleri için ContentType 'ı ayarlama</span><span class="sxs-lookup"><span data-stu-id="46453-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="46453-122">İlk üç komut, *Vaultname* , *Name* ve *ContentType* parametrelerinde kullanılacak dize değişkenlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="46453-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="46453-123">Dördüncü komut, Get-AzureKeyVaultKey cmdlet 'ini kullanarak belirtilen tuşları alır ve içerik türlerini XML olarak ayarlamak için anahtarları Set-AzureKeyVaultSecretAttribute cmdlet 'ine kullanır.</span><span class="sxs-lookup"><span data-stu-id="46453-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="46453-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46453-124">PARAMETERS</span></span>

### <span data-ttu-id="46453-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="46453-125">-ContentType</span></span>
<span data-ttu-id="46453-126">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="46453-127">Bu parametreyi belirtmezseniz, geçerli parolanın içerik türünde bir değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="46453-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="46453-128">Var olan içerik türünü kaldırmak için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="46453-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46453-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46453-129">-DefaultProfile</span></span>
<span data-ttu-id="46453-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="46453-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46453-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="46453-131">-Enable</span></span>
<span data-ttu-id="46453-132">Parolayı etkinleştirip etkinleştirmeyeceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="46453-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="46453-133">Parolayı etkinleştirmek için $False veya parolayı etkinleştirmek için $True belirtin.</span><span class="sxs-lookup"><span data-stu-id="46453-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="46453-134">Bu parametreyi belirtmezseniz, geçerli gizliliğin etkin veya devre dışı durumunda olan bir değişiklik yoktur.</span><span class="sxs-lookup"><span data-stu-id="46453-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="46453-135">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="46453-135">-Expires</span></span>
<span data-ttu-id="46453-136">Gizli bir tarih ve saat değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-136">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="46453-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46453-137">-InputObject</span></span>
<span data-ttu-id="46453-138">Gizli nesne</span><span class="sxs-lookup"><span data-stu-id="46453-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46453-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="46453-139">-Name</span></span>
<span data-ttu-id="46453-140">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-140">Specifies the name of a secret.</span></span> <span data-ttu-id="46453-141">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46453-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46453-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="46453-142">-NotBefore</span></span>
<span data-ttu-id="46453-143">Parolanın kullanılmadığı en evrensel saat (UTC) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="46453-144">Bu parametreyi belirtmezseniz, geçerli gizliliğin NotBefore özniteliğindeki bir değişiklik yoktur.</span><span class="sxs-lookup"><span data-stu-id="46453-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="46453-145">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="46453-145">-PassThru</span></span>
<span data-ttu-id="46453-146">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="46453-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="46453-147">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="46453-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46453-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="46453-148">-Tag</span></span>
<span data-ttu-id="46453-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="46453-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46453-150">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="46453-150">For example:</span></span>

<span data-ttu-id="46453-151">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="46453-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46453-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="46453-152">-VaultName</span></span>
<span data-ttu-id="46453-153">Değiştirilecek Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="46453-154">Bu cmdlet, bu parametrenin belirttiği adı ve seçili olan ortamı belirten bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46453-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="46453-155">-Version</span><span class="sxs-lookup"><span data-stu-id="46453-155">-Version</span></span>
<span data-ttu-id="46453-156">Gizli sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="46453-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="46453-157">Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="46453-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46453-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="46453-158">-Confirm</span></span>
<span data-ttu-id="46453-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46453-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46453-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46453-160">-WhatIf</span></span>
<span data-ttu-id="46453-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46453-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46453-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46453-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46453-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46453-163">CommonParameters</span></span>
<span data-ttu-id="46453-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46453-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46453-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46453-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46453-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46453-166">INPUTS</span></span>

### <span data-ttu-id="46453-167">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="46453-167">None</span></span>
<span data-ttu-id="46453-168">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="46453-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="46453-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46453-169">OUTPUTS</span></span>

### <span data-ttu-id="46453-170">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="46453-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="46453-171">Geçiş belirtildiyse Microsoft. Azure. Commands. Keykasa. model. gizli nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="46453-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="46453-172">Aksi takdirde hiçbir şey geri döner.</span><span class="sxs-lookup"><span data-stu-id="46453-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="46453-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46453-173">NOTES</span></span>

## <span data-ttu-id="46453-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46453-174">RELATED LINKS</span></span>

[<span data-ttu-id="46453-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="46453-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="46453-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="46453-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="46453-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="46453-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
