---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: cae763eedd98a98c7e09855a295791ddc96d5339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096627"
---
# <span data-ttu-id="43919-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43919-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="43919-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43919-102">SYNOPSIS</span></span>
<span data-ttu-id="43919-103">Anahtar kasasındaki bir anahtarın özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="43919-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="43919-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43919-104">SYNTAX</span></span>

### <span data-ttu-id="43919-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43919-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43919-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="43919-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43919-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="43919-107">DESCRIPTION</span></span>
<span data-ttu-id="43919-108">**Update-Azanahtarvaultkey** cmdlet 'i anahtar kasasındaki bir anahtarın düzenlenebilir özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="43919-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="43919-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43919-109">EXAMPLES</span></span>

### <span data-ttu-id="43919-110">Örnek 1: etkinleştirmek için anahtarı değiştirme ve son kullanma tarihi ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="43919-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="43919-111">İlk komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43919-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="43919-112">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="43919-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="43919-113">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="43919-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="43919-114">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="43919-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="43919-115">İkinci komut, yüksek önem düzeyi ve hesap oluşturma etiket değerlerini depolamak için bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43919-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="43919-116">Son komutu ITSoftware adındaki bir anahtarı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="43919-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="43919-117">Komut, anahtarı belirler, kullanım süresi sonunu $Expires depolanan saate göre ayarlar ve $Tags depolanan etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="43919-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="43919-118">Örnek 2: tüm etiketleri silmek için anahtarı değiştirme</span><span class="sxs-lookup"><span data-stu-id="43919-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="43919-119">Bu komut, bir anahtarın ıtsoftware adındaki belirli bir sürümünün tüm etiketlerini siler.</span><span class="sxs-lookup"><span data-stu-id="43919-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="43919-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43919-120">PARAMETERS</span></span>

### <span data-ttu-id="43919-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43919-121">-DefaultProfile</span></span>
<span data-ttu-id="43919-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43919-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43919-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="43919-123">-Enable</span></span>
<span data-ttu-id="43919-124">True değeri anahtarın ve yanlış bir değerin bir değerinin daha azını azaltır.</span><span class="sxs-lookup"><span data-stu-id="43919-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="43919-125">Belirtilmezse, var olan etkin/devre dışı durumu değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="43919-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="43919-126">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="43919-126">-Expires</span></span>
<span data-ttu-id="43919-127">UTC zamanında bir anahtarın kullanım süresi sonu.</span><span class="sxs-lookup"><span data-stu-id="43919-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="43919-128">Belirtilmezse, anahtarın varolan son kullanma tarihi değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="43919-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="43919-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43919-129">-InputObject</span></span>
<span data-ttu-id="43919-130">Anahtar nesnesi</span><span class="sxs-lookup"><span data-stu-id="43919-130">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43919-131">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="43919-131">-KeyOps</span></span>
<span data-ttu-id="43919-132">Anahtarla gerçekleştirilebileceği işlemler.</span><span class="sxs-lookup"><span data-stu-id="43919-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="43919-133">Belirtilmezse, anahtarın varolan anahtar işlemleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="43919-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43919-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="43919-134">-Name</span></span>
<span data-ttu-id="43919-135">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="43919-135">Key name.</span></span>
<span data-ttu-id="43919-136">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43919-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43919-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="43919-137">-NotBefore</span></span>
<span data-ttu-id="43919-138">Tuşun kullanılmadığı UTC saati.</span><span class="sxs-lookup"><span data-stu-id="43919-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="43919-139">Belirtilmezse, anahtarın önceki öznitelik özniteliği değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="43919-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="43919-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="43919-140">-PassThru</span></span>
<span data-ttu-id="43919-141">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="43919-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="43919-142">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar paketi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="43919-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="43919-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="43919-143">-Tag</span></span>
<span data-ttu-id="43919-144">Hashtable anahtar etiketleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="43919-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="43919-145">Belirtilmezse, anahtarın var olan etiketleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="43919-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="43919-146">-VaultName</span><span class="sxs-lookup"><span data-stu-id="43919-146">-VaultName</span></span>
<span data-ttu-id="43919-147">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="43919-147">Vault name.</span></span>
<span data-ttu-id="43919-148">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43919-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="43919-149">-Version</span><span class="sxs-lookup"><span data-stu-id="43919-149">-Version</span></span>
<span data-ttu-id="43919-150">Anahtar sürümü.</span><span class="sxs-lookup"><span data-stu-id="43919-150">Key version.</span></span>
<span data-ttu-id="43919-151">Cmdlet, kasa adından bir anahtar FQDN, şu anda seçili olan ortam, anahtar adı ve anahtar sürümü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="43919-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43919-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="43919-152">-Confirm</span></span>
<span data-ttu-id="43919-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="43919-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43919-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43919-154">-WhatIf</span></span>
<span data-ttu-id="43919-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43919-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43919-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="43919-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43919-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43919-157">CommonParameters</span></span>
<span data-ttu-id="43919-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43919-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43919-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="43919-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43919-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43919-160">INPUTS</span></span>

### <span data-ttu-id="43919-161">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="43919-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="43919-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43919-162">OUTPUTS</span></span>

### <span data-ttu-id="43919-163">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="43919-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="43919-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43919-164">NOTES</span></span>

## <span data-ttu-id="43919-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43919-165">RELATED LINKS</span></span>
