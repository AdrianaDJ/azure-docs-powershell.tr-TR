---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: c7968d915ab28dca6bf595e5339d2681962ecdea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764706"
---
# <span data-ttu-id="5100d-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5100d-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="5100d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5100d-102">SYNOPSIS</span></span>
<span data-ttu-id="5100d-103">Anahtar Kasası içinde gizli kod oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5100d-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5100d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5100d-104">SYNTAX</span></span>

### <span data-ttu-id="5100d-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5100d-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5100d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5100d-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5100d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5100d-107">DESCRIPTION</span></span>
<span data-ttu-id="5100d-108">**Set-AzureKeyVaultSecret** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasına parola oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5100d-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="5100d-109">Gizlilik yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5100d-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="5100d-110">Gizlilik zaten varsa, bu cmdlet bu gizliliğin yeni bir sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5100d-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="5100d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5100d-111">EXAMPLES</span></span>

### <span data-ttu-id="5100d-112">Örnek 1: varsayılan öznitelikleri kullanarak gizli değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="5100d-112">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="5100d-113">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5100d-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5100d-114">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5100d-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5100d-115">İkinci komut, contoso adlı anahtar kasasındaki gizli adlı parolanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5100d-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="5100d-116">Gizli değer $Secret depolanan değer olur.</span><span class="sxs-lookup"><span data-stu-id="5100d-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="5100d-117">Örnek 2: özel öznitelikler kullanarak gizli değerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5100d-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="5100d-118">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5100d-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5100d-119">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5100d-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5100d-120">Sonraki komutlar son kullanma tarihi, etiketleri ve bağlam türü için özel öznitelikleri tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="5100d-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="5100d-121">Son komutu, daha önce değişken olarak belirtilen değerleri kullanarak contoso adlı anahtar kasasındaki gizli adındaki gizli kod değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5100d-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="5100d-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5100d-122">PARAMETERS</span></span>

### <span data-ttu-id="5100d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5100d-123">-ContentType</span></span>
<span data-ttu-id="5100d-124">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5100d-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="5100d-125">Var olan içerik türünü silmek için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="5100d-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="5100d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5100d-126">-DefaultProfile</span></span>
<span data-ttu-id="5100d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5100d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5100d-128">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="5100d-128">-Disable</span></span>
<span data-ttu-id="5100d-129">Bu cmdlet 'in parolayı devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5100d-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="5100d-130">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="5100d-130">-Expires</span></span>
<span data-ttu-id="5100d-131">Bu cmdlet 'in güncelleştirdiği gizli için **Tarih saat**</span><span class="sxs-lookup"><span data-stu-id="5100d-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="5100d-132">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="5100d-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5100d-133">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5100d-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5100d-134">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5100d-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5100d-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5100d-135">-InputObject</span></span>
<span data-ttu-id="5100d-136">Gizli nesne</span><span class="sxs-lookup"><span data-stu-id="5100d-136">Secret object</span></span>

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

### <span data-ttu-id="5100d-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="5100d-137">-Name</span></span>
<span data-ttu-id="5100d-138">Değiştirilecek gizli kod adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5100d-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="5100d-139">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5100d-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="5100d-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5100d-140">-NotBefore</span></span>
<span data-ttu-id="5100d-141">Parolayı bir **Tarih saat** nesnesi olarak, parolanın kullanılmadığı bir tarih olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5100d-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="5100d-142">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="5100d-142">This parameter uses UTC.</span></span> <span data-ttu-id="5100d-143">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5100d-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="5100d-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="5100d-144">-SecretValue</span></span>
<span data-ttu-id="5100d-145">Bir **SecureString** nesnesi olarak gizlilik değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5100d-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="5100d-146">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5100d-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="5100d-147">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5100d-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5100d-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5100d-148">-Tag</span></span>
<span data-ttu-id="5100d-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5100d-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5100d-150">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="5100d-150">For example:</span></span>

<span data-ttu-id="5100d-151">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5100d-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5100d-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5100d-152">-VaultName</span></span>
<span data-ttu-id="5100d-153">Bu gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5100d-153">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="5100d-154">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5100d-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5100d-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="5100d-155">-Confirm</span></span>
<span data-ttu-id="5100d-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5100d-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5100d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5100d-157">-WhatIf</span></span>
<span data-ttu-id="5100d-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5100d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5100d-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5100d-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5100d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5100d-160">CommonParameters</span></span>
<span data-ttu-id="5100d-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5100d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5100d-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5100d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5100d-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5100d-163">INPUTS</span></span>

### <span data-ttu-id="5100d-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5100d-164">None</span></span>
<span data-ttu-id="5100d-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5100d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5100d-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5100d-166">OUTPUTS</span></span>

### <span data-ttu-id="5100d-167">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5100d-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="5100d-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5100d-168">NOTES</span></span>

## <span data-ttu-id="5100d-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5100d-169">RELATED LINKS</span></span>

[<span data-ttu-id="5100d-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5100d-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="5100d-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5100d-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
