---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsmKey.md
ms.openlocfilehash: 79d01f96fe776432f650d827b16ba83f48b84ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279038"
---
# <span data-ttu-id="e0dc8-101">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-101">Update-AzManagedHsmKey</span></span>

## <span data-ttu-id="e0dc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0dc8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dc8-103">Yönetilen HSM 'de bir anahtarın özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-103">Updates the attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="e0dc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0dc8-104">SYNTAX</span></span>

### <span data-ttu-id="e0dc8-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0dc8-105">Default (Default)</span></span>
```
Update-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0dc8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e0dc8-106">InputObject</span></span>
```
Update-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0dc8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0dc8-107">DESCRIPTION</span></span>
<span data-ttu-id="e0dc8-108">**Update-AzManagedHsmKey** cmdlet 'i, YÖNETILEN bir HSM 'de bir anahtarın düzenlenebilir özniteliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-108">The **Update-AzManagedHsmKey** cmdlet updates the editable attributes of a key in a managed HSM.</span></span>

## <span data-ttu-id="e0dc8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0dc8-109">EXAMPLES</span></span>

### <span data-ttu-id="e0dc8-110">Örnek 1: etkinleştirmek için anahtarı değiştirme ve son kullanma tarihi ve etiketleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="e0dc8-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzManagedHsmKey -HsmName testmhsm -Name testkey001 -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 49b74a39dab605bd336628dc094dc31b
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/49b74a39dab605bd336628dc094dc31b
Enabled        : True
Expires        : 10/14/2022 9:46:55 AM
Not Before     :
Created        : 10/14/2020 3:39:16 AM
Updated        : 10/14/2020 9:47:06 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="e0dc8-111">İlk komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="e0dc8-112">Bu nesne gelecek yıl iki yıl belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="e0dc8-113">Komut bu tarihi $Expires değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="e0dc8-114">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e0dc8-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="e0dc8-115">İkinci komut, yüksek önem düzeyi ve hesap oluşturma etiket değerlerini depolamak için bir değişken oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="e0dc8-116">Son komut testkey001 adlı bir anahtarı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-116">The final command modifies a key named testkey001.</span></span> <span data-ttu-id="e0dc8-117">Komut, anahtarı belirler, kullanım süresi sonunu $Expires depolanan saate göre ayarlar ve $Tags depolanan etiketleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

## <span data-ttu-id="e0dc8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0dc8-118">PARAMETERS</span></span>

### <span data-ttu-id="e0dc8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dc8-119">-DefaultProfile</span></span>
<span data-ttu-id="e0dc8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0dc8-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="e0dc8-121">-Enable</span></span>
<span data-ttu-id="e0dc8-122">True değeri anahtarın ve yanlış bir değerin bir değerinin daha azını azaltır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-122">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="e0dc8-123">Belirtilmezse, var olan etkin/devre dışı durumu değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-123">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="e0dc8-124">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="e0dc8-124">-Expires</span></span>
<span data-ttu-id="e0dc8-125">UTC zamanında bir anahtarın kullanım süresi sonu.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-125">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="e0dc8-126">Belirtilmezse, anahtarın varolan son kullanma tarihi değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-126">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="e0dc8-127">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e0dc8-127">-HsmName</span></span>
<span data-ttu-id="e0dc8-128">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-128">HSM name.</span></span> <span data-ttu-id="e0dc8-129">Cmdlet, yönetilen bir HSM 'in FQDN 'sini ad ve şu anda seçili olan ortama göre oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-129">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e0dc8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0dc8-130">-InputObject</span></span>
<span data-ttu-id="e0dc8-131">Anahtar nesnesi</span><span class="sxs-lookup"><span data-stu-id="e0dc8-131">Key object</span></span>

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

### <span data-ttu-id="e0dc8-132">-Keyolar</span><span class="sxs-lookup"><span data-stu-id="e0dc8-132">-KeyOps</span></span>
<span data-ttu-id="e0dc8-133">Anahtarla gerçekleştirilebileceği işlemler.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-133">The operations that can be performed with the key.</span></span>
<span data-ttu-id="e0dc8-134">Belirtilmezse, anahtarın varolan anahtar işlemleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-134">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="e0dc8-135">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0dc8-135">-Name</span></span>
<span data-ttu-id="e0dc8-136">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-136">Key name.</span></span>
<span data-ttu-id="e0dc8-137">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan ve anahtar adından bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-137">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="e0dc8-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="e0dc8-138">-NotBefore</span></span>
<span data-ttu-id="e0dc8-139">Tuşun kullanılmadığı UTC saati.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-139">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="e0dc8-140">Belirtilmezse, anahtarın önceki öznitelik özniteliği değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-140">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="e0dc8-141">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e0dc8-141">-PassThru</span></span>
<span data-ttu-id="e0dc8-142">Cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e0dc8-143">Bu anahtar belirtilmişse, güncelleştirilmiş anahtar paketi nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-143">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="e0dc8-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e0dc8-144">-Tag</span></span>
<span data-ttu-id="e0dc8-145">Hashtable anahtar etiketleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-145">A hashtable represents key tags.</span></span>
<span data-ttu-id="e0dc8-146">Belirtilmezse, anahtarın var olan etiketleri değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-146">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="e0dc8-147">-Version</span><span class="sxs-lookup"><span data-stu-id="e0dc8-147">-Version</span></span>
<span data-ttu-id="e0dc8-148">Anahtar sürümü.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-148">Key version.</span></span>
<span data-ttu-id="e0dc8-149">Cmdlet yönetilen HSM adından, şu anda seçili olan ortamdan, anahtar adıyla anahtar sürümünden bir anahtarın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-149">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="e0dc8-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0dc8-150">-Confirm</span></span>
<span data-ttu-id="e0dc8-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0dc8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0dc8-152">-WhatIf</span></span>
<span data-ttu-id="e0dc8-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0dc8-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0dc8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dc8-155">CommonParameters</span></span>
<span data-ttu-id="e0dc8-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dc8-157">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e0dc8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dc8-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0dc8-158">INPUTS</span></span>

### <span data-ttu-id="e0dc8-159">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="e0dc8-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="e0dc8-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0dc8-160">OUTPUTS</span></span>

### <span data-ttu-id="e0dc8-161">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="e0dc8-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0dc8-162">NOTES</span></span>

## <span data-ttu-id="e0dc8-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0dc8-163">RELATED LINKS</span></span>

[<span data-ttu-id="e0dc8-164">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-164">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="e0dc8-165">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-165">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="e0dc8-166">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-166">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="e0dc8-167">Geri al-Azmanagedhsmanahtarkaldırma</span><span class="sxs-lookup"><span data-stu-id="e0dc8-167">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="e0dc8-168">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-168">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="e0dc8-169">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="e0dc8-169">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)