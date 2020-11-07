---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 9a0e40716623b4d0b11f661ce859a0ee8787e685
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916167"
---
# <span data-ttu-id="a52bb-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a52bb-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="a52bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a52bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a52bb-103">Anahtar kasasındaki gizli öznitelikleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a52bb-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="a52bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a52bb-104">SYNTAX</span></span>

### <span data-ttu-id="a52bb-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a52bb-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a52bb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a52bb-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a52bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a52bb-107">DESCRIPTION</span></span>
<span data-ttu-id="a52bb-108">**Update-Azanahtarvaultsecret** cmdlet 'i anahtar kasasındaki bir gizli kod öğesinin düzenlenebilir özniteliklerini günceller.</span><span class="sxs-lookup"><span data-stu-id="a52bb-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="a52bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a52bb-109">EXAMPLES</span></span>

### <span data-ttu-id="a52bb-110">Örnek 1: parolayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a52bb-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="a52bb-111">İlk dört komut son kullanma tarihi, Notöncesi tarihi, etiketleri ve bağlam türü özniteliklerini tanımlar ve öznitelikleri değişkenlere depolar.</span><span class="sxs-lookup"><span data-stu-id="a52bb-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="a52bb-112">Son komutu, depolanan değişkenleri kullanarak, Contosokasası adlı anahtar kasasına ık adlı parola ile ilgili öznitelikleri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a52bb-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="a52bb-113">Örnek 2: gizli için etiketleri ve içerik türünü silme</span><span class="sxs-lookup"><span data-stu-id="a52bb-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="a52bb-114">Bu komut, contoso adlı anahtar kasasına HR adlı parola adlı gizli sürümün etiketlerini ve içerik türünü siler.</span><span class="sxs-lookup"><span data-stu-id="a52bb-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="a52bb-115">Örnek 3: adı bununla başlayan gizli kod sürümlerini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="a52bb-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="a52bb-116">İlk komut $Vault değişkeninde contoso dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="a52bb-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="a52bb-117">İkinci komut, $Prefix değişkeninde dize değerini depolar.</span><span class="sxs-lookup"><span data-stu-id="a52bb-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="a52bb-118">Üçüncü komut, Get-AzKeyVaultSecret cmdlet 'ini kullanarak belirtilen anahtar kasasındaki gizlilikleri alır ve bu gizlilikleri **WHERE-Object** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="a52bb-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="a52bb-119">**WHERE-Object** cmdlet 'i, adlarla başlayan adlarla ilgili gizli kod dizelerini süzer.</span><span class="sxs-lookup"><span data-stu-id="a52bb-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="a52bb-120">Komut, filtreyle eşleşen gizli kod dizelerini devre dışı bırakan Update-AzKeyVaultSecret cmdlet 'ine göre yöneltme içerir.</span><span class="sxs-lookup"><span data-stu-id="a52bb-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="a52bb-121">Örnek 4: tüm gizli sürümleri için ContentType 'ı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a52bb-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="a52bb-122">İlk üç komut, *Vaultname* , *Name* ve *ContentType* parametrelerinde kullanılacak dize değişkenlerini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="a52bb-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="a52bb-123">Dördüncü komut, Get-AzKeyVaultKey cmdlet 'ini kullanarak belirtilen tuşları alır ve içerik türlerini XML olarak ayarlamak için anahtarları Update-AzKeyVaultSecret cmdlet 'ine kullanır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="a52bb-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a52bb-124">PARAMETERS</span></span>

### <span data-ttu-id="a52bb-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a52bb-125">-ContentType</span></span>
<span data-ttu-id="a52bb-126">Gizli içerik türü.</span><span class="sxs-lookup"><span data-stu-id="a52bb-126">Secret's content type.</span></span>
<span data-ttu-id="a52bb-127">Belirtilmezse, parola türünün varolan değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="a52bb-128">Boş dize belirterek var olan içerik türü değerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a52bb-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="a52bb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52bb-129">-DefaultProfile</span></span>
<span data-ttu-id="a52bb-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a52bb-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52bb-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="a52bb-131">-Enable</span></span>
<span data-ttu-id="a52bb-132">Varsa, değer true ise parolayı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a52bb-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="a52bb-133">Değer yanlışsa parolayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="a52bb-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="a52bb-134">Belirtilmezse, parolanın etkin/devre dışı durumu değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="a52bb-135">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="a52bb-135">-Expires</span></span>
<span data-ttu-id="a52bb-136">UTC zamanında bir parolanın son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="a52bb-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="a52bb-137">Belirtilmemişse, parola süre sonu değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="a52bb-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a52bb-138">-InputObject</span></span>
<span data-ttu-id="a52bb-139">Gizli nesne</span><span class="sxs-lookup"><span data-stu-id="a52bb-139">Secret object</span></span>

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

### <span data-ttu-id="a52bb-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="a52bb-140">-Name</span></span>
<span data-ttu-id="a52bb-141">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="a52bb-141">Secret name.</span></span>
<span data-ttu-id="a52bb-142">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a52bb-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="a52bb-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="a52bb-143">-NotBefore</span></span>
<span data-ttu-id="a52bb-144">Parolanın kullanılmadığı UTC saati.</span><span class="sxs-lookup"><span data-stu-id="a52bb-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="a52bb-145">Belirtilmezse, parolanın Notöncesi özniteliğinin mevcut değeri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="a52bb-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a52bb-146">-PassThru</span></span>
<span data-ttu-id="a52bb-147">Cmdlet, varsayılan olarak nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a52bb-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="a52bb-148">Bu anahtar belirtilmişse, gizli nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="a52bb-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="a52bb-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a52bb-149">-Tag</span></span>
<span data-ttu-id="a52bb-150">Gizli etiketleri temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="a52bb-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="a52bb-151">Belirtilmezse, parolanın var olan etiketleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="a52bb-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="a52bb-152">Boş bir Hashtable belirterek etiketi kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a52bb-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="a52bb-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a52bb-153">-VaultName</span></span>
<span data-ttu-id="a52bb-154">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="a52bb-154">Vault name.</span></span>
<span data-ttu-id="a52bb-155">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a52bb-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="a52bb-156">-Version</span><span class="sxs-lookup"><span data-stu-id="a52bb-156">-Version</span></span>
<span data-ttu-id="a52bb-157">Gizli sürüm.</span><span class="sxs-lookup"><span data-stu-id="a52bb-157">Secret version.</span></span>
<span data-ttu-id="a52bb-158">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı, gizli adı ve gizli sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a52bb-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a52bb-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="a52bb-159">-Confirm</span></span>
<span data-ttu-id="a52bb-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a52bb-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52bb-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52bb-161">-WhatIf</span></span>
<span data-ttu-id="a52bb-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a52bb-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52bb-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a52bb-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52bb-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52bb-164">CommonParameters</span></span>
<span data-ttu-id="a52bb-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a52bb-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52bb-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52bb-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52bb-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a52bb-167">INPUTS</span></span>

### <span data-ttu-id="a52bb-168">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="a52bb-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="a52bb-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a52bb-169">OUTPUTS</span></span>

### <span data-ttu-id="a52bb-170">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a52bb-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="a52bb-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a52bb-171">NOTES</span></span>

## <span data-ttu-id="a52bb-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a52bb-172">RELATED LINKS</span></span>
