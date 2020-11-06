---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 820406a3fe4bebfd0b2a972bb8676bbd483f7080
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588100"
---
# <span data-ttu-id="c8f0c-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8f0c-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="c8f0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f0c-103">Anahtar Kasası içinde gizli kod oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8f0c-104">SYNTAX</span></span>

### <span data-ttu-id="c8f0c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8f0c-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8f0c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c8f0c-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f0c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8f0c-107">DESCRIPTION</span></span>
<span data-ttu-id="c8f0c-108">**Set-AzureKeyVaultSecret** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasına parola oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="c8f0c-109">Gizlilik yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="c8f0c-110">Gizlilik zaten varsa, bu cmdlet bu gizliliğin yeni bir sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="c8f0c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8f0c-111">EXAMPLES</span></span>

### <span data-ttu-id="c8f0c-112">Örnek 1: varsayılan öznitelikleri kullanarak gizli değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="c8f0c-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="c8f0c-113">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="c8f0c-114">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="c8f0c-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="c8f0c-115">İkinci komut, contoso adlı anahtar kasasındaki gizli adlı parolanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="c8f0c-116">Gizli değer $Secret depolanan değer olur.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="c8f0c-117">Örnek 2: özel öznitelikler kullanarak gizli değerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c8f0c-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="c8f0c-118">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="c8f0c-119">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="c8f0c-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="c8f0c-120">Sonraki komutlar son kullanma tarihi, etiketleri ve bağlam türü için özel öznitelikleri tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="c8f0c-121">Son komutu, daha önce değişken olarak belirtilen değerleri kullanarak contoso adlı anahtar kasasındaki gizli adındaki gizli kod değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="c8f0c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8f0c-122">PARAMETERS</span></span>

### <span data-ttu-id="c8f0c-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="c8f0c-123">-ContentType</span></span>
<span data-ttu-id="c8f0c-124">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="c8f0c-125">Var olan içerik türünü silmek için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f0c-126">-DefaultProfile</span></span>
<span data-ttu-id="c8f0c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8f0c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8f0c-128">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="c8f0c-128">-Disable</span></span>
<span data-ttu-id="c8f0c-129">Bu cmdlet 'in parolayı devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="c8f0c-130">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="c8f0c-130">-Expires</span></span>
<span data-ttu-id="c8f0c-131">Bu cmdlet 'in güncelleştirdiği gizli için **Tarih saat**</span><span class="sxs-lookup"><span data-stu-id="c8f0c-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="c8f0c-132">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c8f0c-133">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="c8f0c-134">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c8f0c-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="c8f0c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8f0c-135">-InputObject</span></span>
<span data-ttu-id="c8f0c-136">Gizli nesne</span><span class="sxs-lookup"><span data-stu-id="c8f0c-136">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0c-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8f0c-137">-Name</span></span>
<span data-ttu-id="c8f0c-138">Değiştirilecek gizli kod adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="c8f0c-139">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0c-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="c8f0c-140">-NotBefore</span></span>
<span data-ttu-id="c8f0c-141">Parolayı bir **Tarih saat** nesnesi olarak, parolanın kullanılmadığı bir tarih olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="c8f0c-142">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-142">This parameter uses UTC.</span></span> <span data-ttu-id="c8f0c-143">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="c8f0c-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="c8f0c-144">-SecretValue</span></span>
<span data-ttu-id="c8f0c-145">Bir **SecureString** nesnesi olarak gizlilik değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="c8f0c-146">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="c8f0c-147">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="c8f0c-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0c-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c8f0c-148">-Tag</span></span>
<span data-ttu-id="c8f0c-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c8f0c-150">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c8f0c-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c8f0c-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c8f0c-151">-VaultName</span></span>
<span data-ttu-id="c8f0c-152">Bu gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="c8f0c-153">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8f0c-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="c8f0c-154">-Confirm</span></span>
<span data-ttu-id="c8f0c-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8f0c-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f0c-156">-WhatIf</span></span>
<span data-ttu-id="c8f0c-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8f0c-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8f0c-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f0c-159">CommonParameters</span></span>
<span data-ttu-id="c8f0c-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8f0c-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f0c-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f0c-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f0c-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8f0c-162">INPUTS</span></span>

### <span data-ttu-id="c8f0c-163">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="c8f0c-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="c8f0c-164">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8f0c-164">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c8f0c-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8f0c-165">OUTPUTS</span></span>

### <span data-ttu-id="c8f0c-166">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8f0c-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="c8f0c-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8f0c-167">NOTES</span></span>

## <span data-ttu-id="c8f0c-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8f0c-168">RELATED LINKS</span></span>

[<span data-ttu-id="c8f0c-169">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8f0c-169">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="c8f0c-170">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c8f0c-170">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
