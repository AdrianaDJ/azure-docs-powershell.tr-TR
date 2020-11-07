---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 14b66299fb0321448b7e121cfced0a29f69518ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751624"
---
# <span data-ttu-id="6c654-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c654-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="6c654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c654-102">SYNOPSIS</span></span>
<span data-ttu-id="6c654-103">Anahtar Kasası içinde gizli kod oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6c654-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="6c654-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c654-104">SYNTAX</span></span>

### <span data-ttu-id="6c654-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c654-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c654-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c654-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c654-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c654-107">DESCRIPTION</span></span>
<span data-ttu-id="6c654-108">**Set-Azanahtarvaultsecret** cmdlet 'ı, Azure Anahtar Kasası 'ndaki bir anahtar kasasına parola oluşturur veya bu parolayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6c654-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="6c654-109">Gizlilik yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c654-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="6c654-110">Gizlilik zaten varsa, bu cmdlet bu gizliliğin yeni bir sürümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c654-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="6c654-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c654-111">EXAMPLES</span></span>

### <span data-ttu-id="6c654-112">Örnek 1: varsayılan öznitelikleri kullanarak gizli değeri değiştirme</span><span class="sxs-lookup"><span data-stu-id="6c654-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

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

<span data-ttu-id="6c654-113">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c654-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6c654-114">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6c654-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6c654-115">İkinci komut, contoso adlı anahtar kasasındaki gizli adlı parolanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6c654-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="6c654-116">Gizli değer $Secret depolanan değer olur.</span><span class="sxs-lookup"><span data-stu-id="6c654-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="6c654-117">Örnek 2: özel öznitelikler kullanarak gizli değerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="6c654-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

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

<span data-ttu-id="6c654-118">İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Secret değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6c654-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="6c654-119">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6c654-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="6c654-120">Sonraki komutlar son kullanma tarihi, etiketleri ve bağlam türü için özel öznitelikleri tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="6c654-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="6c654-121">Son komutu, daha önce değişken olarak belirtilen değerleri kullanarak contoso adlı anahtar kasasındaki gizli adındaki gizli kod değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6c654-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="6c654-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c654-122">PARAMETERS</span></span>

### <span data-ttu-id="6c654-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6c654-123">-ContentType</span></span>
<span data-ttu-id="6c654-124">Parolanın içerik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c654-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="6c654-125">Var olan içerik türünü silmek için boş bir dize belirtin.</span><span class="sxs-lookup"><span data-stu-id="6c654-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="6c654-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c654-126">-DefaultProfile</span></span>
<span data-ttu-id="6c654-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6c654-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c654-128">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="6c654-128">-Disable</span></span>
<span data-ttu-id="6c654-129">Bu cmdlet 'in parolayı devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c654-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="6c654-130">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="6c654-130">-Expires</span></span>
<span data-ttu-id="6c654-131">Bu cmdlet 'in güncelleştirdiği gizli için **Tarih saat**</span><span class="sxs-lookup"><span data-stu-id="6c654-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="6c654-132">Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c654-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="6c654-133">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c654-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="6c654-134">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6c654-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="6c654-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c654-135">-InputObject</span></span>
<span data-ttu-id="6c654-136">Gizli nesne</span><span class="sxs-lookup"><span data-stu-id="6c654-136">Secret object</span></span>

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

### <span data-ttu-id="6c654-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c654-137">-Name</span></span>
<span data-ttu-id="6c654-138">Değiştirilecek gizli kod adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c654-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="6c654-139">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c654-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="6c654-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="6c654-140">-NotBefore</span></span>
<span data-ttu-id="6c654-141">Parolayı bir **Tarih saat** nesnesi olarak, parolanın kullanılmadığı bir tarih olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c654-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="6c654-142">Bu parametre UTC kullanır.</span><span class="sxs-lookup"><span data-stu-id="6c654-142">This parameter uses UTC.</span></span> <span data-ttu-id="6c654-143">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c654-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="6c654-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="6c654-144">-SecretValue</span></span>
<span data-ttu-id="6c654-145">Bir **SecureString** nesnesi olarak gizlilik değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c654-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="6c654-146">**SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6c654-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="6c654-147">Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="6c654-147">For more information, type `Get-Help
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

### <span data-ttu-id="6c654-148">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6c654-148">-Tag</span></span>
<span data-ttu-id="6c654-149">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6c654-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6c654-150">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6c654-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6c654-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6c654-151">-VaultName</span></span>
<span data-ttu-id="6c654-152">Bu gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c654-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="6c654-153">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c654-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="6c654-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="6c654-154">-Confirm</span></span>
<span data-ttu-id="6c654-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6c654-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c654-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c654-156">-WhatIf</span></span>
<span data-ttu-id="6c654-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6c654-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c654-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6c654-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c654-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c654-159">CommonParameters</span></span>
<span data-ttu-id="6c654-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c654-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c654-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c654-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c654-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c654-162">INPUTS</span></span>

### <span data-ttu-id="6c654-163">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="6c654-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6c654-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c654-164">OUTPUTS</span></span>

### <span data-ttu-id="6c654-165">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c654-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6c654-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c654-166">NOTES</span></span>

## <span data-ttu-id="6c654-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c654-167">RELATED LINKS</span></span>

[<span data-ttu-id="6c654-168">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="6c654-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="6c654-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6c654-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
