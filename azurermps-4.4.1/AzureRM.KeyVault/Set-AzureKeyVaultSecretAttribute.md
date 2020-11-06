---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://go.microsoft.com/fwlink/?LinkId=690305
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: 9d9bd8a14b3a24d6001a7f1c2663b05a1e427f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594249"
---
# <span data-ttu-id="f5358-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="f5358-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="f5358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5358-102">SYNOPSIS</span></span>
<span data-ttu-id="f5358-103">Anahtar kasasındaki gizli öznitelikleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f5358-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5358-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5358-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5358-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5358-105">DESCRIPTION</span></span>
<span data-ttu-id="f5358-106">**Set-AzureKeyVaultSecretAttribute** cmdlet 'i anahtar kasasındaki bir gizli kod öğesinin düzenlenebilir özniteliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="f5358-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f5358-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5358-107">EXAMPLES</span></span>

### <span data-ttu-id="f5358-108">Örnek 1: parolayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="f5358-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="f5358-109">İlk dört komut son kullanma tarihi, Notöncesi tarihi, etiketleri ve bağlam türü özniteliklerini tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="f5358-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="f5358-110">Son komutu, depolanan değişkenleri kullanarak, Contosokasası adlı anahtar kasasına ık adlı parola ile ilgili öznitelikleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f5358-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="f5358-111">Örnek 2: gizli için etiketleri ve içerik türünü silme</span><span class="sxs-lookup"><span data-stu-id="f5358-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="f5358-112">Bu komut, contoso adlı anahtar kasasına HR adlı parola adlı gizli sürümün etiketlerini ve içerik türünü siler.</span><span class="sxs-lookup"><span data-stu-id="f5358-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="f5358-113">Örnek 3: adı bununla başlayan gizli kod sürümlerini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f5358-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="f5358-114">İlk komut $Vault değişkeninde contoso dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="f5358-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="f5358-115">İkinci komut, $Prefix değişkeninde dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="f5358-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="f5358-116">Üçüncü komut, Get-AzureKeyVaultSecret cmdlet 'ini kullanarak belirtilen anahtar kasasındaki gizlilikleri alır ve bu gizlilikleri **WHERE-Object** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f5358-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="f5358-117">**WHERE-Object** cmdlet 'i, adlarla başlayan adlarla ilgili gizli kod dizelerini süzer.</span><span class="sxs-lookup"><span data-stu-id="f5358-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="f5358-118">Komut, filtreyle eşleşen gizli kod dizelerini devre dışı bırakan Set-AzureKeyVaultSecretAttribute cmdlet 'ine göre yöneltme içerir.</span><span class="sxs-lookup"><span data-stu-id="f5358-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="f5358-119">Örnek 4: tüm gizli sürümleri için ContentType 'ı ayarlama</span><span class="sxs-lookup"><span data-stu-id="f5358-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="f5358-120">İlk üç komut, *Vaultname* , *Name* ve *ContentType* parametrelerinde kullanılacak dize değişkenlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f5358-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="f5358-121">Dördüncü komut, Get-AzureKeyVaultKey cmdlet 'ini kullanarak belirtilen tuşları alır ve içerik türlerini XML olarak ayarlamak için anahtarları Set-AzureKeyVaultSecretAttribute cmdlet 'ine kullanır.</span><span class="sxs-lookup"><span data-stu-id="f5358-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="f5358-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5358-122">PARAMETERS</span></span>

### <span data-ttu-id="f5358-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5358-123">-Confirm</span></span>
<span data-ttu-id="f5358-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5358-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5358-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f5358-125">-ContentType</span></span>
<span data-ttu-id="f5358-126">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="f5358-127">Bu parametreyi belirtmezseniz, geçerli parolanın içerik türünde bir değişiklik olmaz.</span><span class="sxs-lookup"><span data-stu-id="f5358-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="f5358-128">Var olan içerik türünü kaldırmak için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="f5358-128">To remove the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="f5358-129">-Enable</span></span>
<span data-ttu-id="f5358-130">Parolayı etkinleştirip etkinleştirmeyeceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5358-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="f5358-131">Parolayı etkinleştirmek için $False veya parolayı etkinleştirmek için $True belirtin.</span><span class="sxs-lookup"><span data-stu-id="f5358-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="f5358-132">Bu parametreyi belirtmezseniz, geçerli gizliliğin etkin veya devre dışı durumunda olan bir değişiklik yoktur.</span><span class="sxs-lookup"><span data-stu-id="f5358-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-133">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="f5358-133">-Expires</span></span>
<span data-ttu-id="f5358-134">Gizli bir tarih ve saat değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-134">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5358-135">-Name</span></span>
<span data-ttu-id="f5358-136">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-136">Specifies the name of a secret.</span></span> <span data-ttu-id="f5358-137">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5358-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f5358-138">-NotBefore</span></span>
<span data-ttu-id="f5358-139">Parolanın kullanılmadığı en evrensel saat (UTC) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="f5358-140">Bu parametreyi belirtmezseniz, geçerli gizliliğin NotBefore özniteliğindeki bir değişiklik yoktur.</span><span class="sxs-lookup"><span data-stu-id="f5358-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-141">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f5358-141">-PassThru</span></span>
<span data-ttu-id="f5358-142">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f5358-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5358-143">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f5358-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5358-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f5358-144">-Tag</span></span>
<span data-ttu-id="f5358-145">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="f5358-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5358-146">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="f5358-146">For example:</span></span>

<span data-ttu-id="f5358-147">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="f5358-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f5358-148">-VaultName</span></span>
<span data-ttu-id="f5358-149">Değiştirilecek Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="f5358-150">Bu cmdlet, bu parametrenin belirttiği adı ve seçili olan ortamı belirten bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5358-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-151">-Version</span><span class="sxs-lookup"><span data-stu-id="f5358-151">-Version</span></span>
<span data-ttu-id="f5358-152">Gizli sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5358-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="f5358-153">Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5358-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5358-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5358-154">-WhatIf</span></span>
<span data-ttu-id="f5358-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5358-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5358-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5358-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5358-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5358-157">-DefaultProfile</span></span>
<span data-ttu-id="f5358-158">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5358-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5358-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5358-159">CommonParameters</span></span>
<span data-ttu-id="f5358-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5358-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5358-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5358-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5358-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5358-162">INPUTS</span></span>

## <span data-ttu-id="f5358-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5358-163">OUTPUTS</span></span>

### <span data-ttu-id="f5358-164">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="f5358-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="f5358-165">Geçiş belirtildiyse Microsoft. Azure. Commands. Keykasa. model. gizli nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="f5358-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="f5358-166">Aksi takdirde hiçbir şey geri döner.</span><span class="sxs-lookup"><span data-stu-id="f5358-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="f5358-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5358-167">NOTES</span></span>

## <span data-ttu-id="f5358-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5358-168">RELATED LINKS</span></span>

[<span data-ttu-id="f5358-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5358-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="f5358-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f5358-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="f5358-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f5358-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
