---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://go.microsoft.com/fwlink/?LinkId=690303
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 737a99fa59530ca37d32e2ca1c2c7d7e609ed225
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764552"
---
# <span data-ttu-id="dc3d6-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dc3d6-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="dc3d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc3d6-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3d6-103">Anahtar Kasası içinde gizli kod oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc3d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc3d6-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc3d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc3d6-105">DESCRIPTION</span></span>
<span data-ttu-id="dc3d6-106">**Set-AzureKeyVaultSecret** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasına parola oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="dc3d6-107">Gizlilik yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="dc3d6-108">Gizlilik zaten varsa, bu cmdlet bu gizliliğin yeni bir sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="dc3d6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc3d6-109">EXAMPLES</span></span>

### <span data-ttu-id="dc3d6-110">Örnek 1: varsayılan öznitelikleri kullanarak gizli değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="dc3d6-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="dc3d6-111">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="dc3d6-112">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dc3d6-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="dc3d6-113">İkinci komut, contoso adlı anahtar kasasındaki gizli adlı parolanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="dc3d6-114">Gizli değer $Secret depolanan değer olur.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="dc3d6-115">Örnek 2: özel öznitelikler kullanarak gizli değerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="dc3d6-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="dc3d6-116">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="dc3d6-117">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dc3d6-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="dc3d6-118">Sonraki komutlar son kullanma tarihi, etiketleri ve bağlam türü için özel öznitelikleri tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="dc3d6-119">Son komutu, daha önce değişken olarak belirtilen değerleri kullanarak contoso adlı anahtar kasasındaki gizli adındaki gizli kod değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="dc3d6-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc3d6-120">PARAMETERS</span></span>

### <span data-ttu-id="dc3d6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="dc3d6-121">-Confirm</span></span>
<span data-ttu-id="dc3d6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc3d6-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dc3d6-123">-ContentType</span></span>
<span data-ttu-id="dc3d6-124">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="dc3d6-125">Var olan içerik türünü silmek için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="dc3d6-126">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="dc3d6-126">-Disable</span></span>
<span data-ttu-id="dc3d6-127">Bu cmdlet 'in parolayı devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="dc3d6-128">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="dc3d6-128">-Expires</span></span>
<span data-ttu-id="dc3d6-129">Bu cmdlet 'in güncelleştirdiği gizli için **Tarih saat**</span><span class="sxs-lookup"><span data-stu-id="dc3d6-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="dc3d6-130">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="dc3d6-131">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="dc3d6-132">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dc3d6-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="dc3d6-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="dc3d6-133">-Name</span></span>
<span data-ttu-id="dc3d6-134">Değiştirilecek gizli kod adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="dc3d6-135">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="dc3d6-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="dc3d6-136">-NotBefore</span></span>
<span data-ttu-id="dc3d6-137">Parolayı bir **Tarih saat** nesnesi olarak, parolanın kullanılmadığı bir tarih olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="dc3d6-138">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-138">This parameter uses UTC.</span></span> <span data-ttu-id="dc3d6-139">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="dc3d6-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="dc3d6-140">-SecretValue</span></span>
<span data-ttu-id="dc3d6-141">Bir **SecureString** nesnesi olarak gizlilik değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="dc3d6-142">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="dc3d6-143">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dc3d6-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc3d6-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dc3d6-144">-Tag</span></span>
<span data-ttu-id="dc3d6-145">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dc3d6-146">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="dc3d6-146">For example:</span></span>

<span data-ttu-id="dc3d6-147">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="dc3d6-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dc3d6-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dc3d6-148">-VaultName</span></span>
<span data-ttu-id="dc3d6-149">Bu gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="dc3d6-150">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="dc3d6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc3d6-151">-WhatIf</span></span>
<span data-ttu-id="dc3d6-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc3d6-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc3d6-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3d6-154">-DefaultProfile</span></span>
<span data-ttu-id="dc3d6-155">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3d6-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3d6-156">CommonParameters</span></span>
<span data-ttu-id="dc3d6-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc3d6-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3d6-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc3d6-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3d6-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc3d6-159">INPUTS</span></span>

## <span data-ttu-id="dc3d6-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc3d6-160">OUTPUTS</span></span>

### <span data-ttu-id="dc3d6-161">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="dc3d6-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="dc3d6-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc3d6-162">NOTES</span></span>

## <span data-ttu-id="dc3d6-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc3d6-163">RELATED LINKS</span></span>

[<span data-ttu-id="dc3d6-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dc3d6-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="dc3d6-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dc3d6-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
