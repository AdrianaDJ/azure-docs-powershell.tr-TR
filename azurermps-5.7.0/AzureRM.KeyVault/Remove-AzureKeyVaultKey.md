---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589764"
---
# <span data-ttu-id="fc6a7-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc6a7-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="fc6a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6a7-103">Anahtar kasasındaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc6a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc6a7-104">SYNTAX</span></span>

### <span data-ttu-id="fc6a7-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc6a7-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc6a7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc6a7-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc6a7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc6a7-107">DESCRIPTION</span></span>
<span data-ttu-id="fc6a7-108">Remove-AzureKeyVaultKey cmdlet 'i anahtar kasadaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="fc6a7-109">Anahtar yanlışlıkla silinmişse anahtar, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzureKeyVaultKeyRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="fc6a7-110">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="fc6a7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc6a7-111">EXAMPLES</span></span>

### <span data-ttu-id="fc6a7-112">Örnek 1: anahtar kasasından anahtar kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc6a7-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="fc6a7-113">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="fc6a7-114">Örnek 2: Kullanıcı onayı olmadan bir anahtarı kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc6a7-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="fc6a7-115">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="fc6a7-116">Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="fc6a7-117">Örnek 3: silinen anahtarı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="fc6a7-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="fc6a7-118">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı temizler.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="fc6a7-119">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="fc6a7-120">Örnek 4: ardışık düzen işlecini kullanarak anahtarları kaldırma</span><span class="sxs-lookup"><span data-stu-id="fc6a7-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="fc6a7-121">Bu komut contoso adlı anahtar kasasındaki tüm anahtarları alır ve ardışık düzen işlecini kullanarak bunları **nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fc6a7-122">Bu cmdlet geçerli cmdlet 'e **Enabled** özniteliği için $false değeri olan anahtarları geçirir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="fc6a7-123">Bu cmdlet bu tuşları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="fc6a7-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc6a7-124">PARAMETERS</span></span>

### <span data-ttu-id="fc6a7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6a7-125">-DefaultProfile</span></span>
<span data-ttu-id="fc6a7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc6a7-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc6a7-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fc6a7-127">-Force</span></span>
<span data-ttu-id="fc6a7-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc6a7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc6a7-129">-InputObject</span></span>
<span data-ttu-id="fc6a7-130">AnahtarPaketi nesnesi</span><span class="sxs-lookup"><span data-stu-id="fc6a7-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6a7-131">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="fc6a7-131">-InRemovedState</span></span>
<span data-ttu-id="fc6a7-132">Önceden silinen anahtarı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="fc6a7-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc6a7-133">-Name</span></span>
<span data-ttu-id="fc6a7-134">Kaldırılacak anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="fc6a7-135">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6a7-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc6a7-136">-PassThru</span></span>
<span data-ttu-id="fc6a7-137">Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** nesnesi döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="fc6a7-138">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc6a7-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc6a7-139">-VaultName</span></span>
<span data-ttu-id="fc6a7-140">Anahtarın kaldırılacağı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="fc6a7-141">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc6a7-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc6a7-142">-Confirm</span></span>
<span data-ttu-id="fc6a7-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc6a7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc6a7-144">-WhatIf</span></span>
<span data-ttu-id="fc6a7-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc6a7-146">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc6a7-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc6a7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6a7-148">CommonParameters</span></span>
<span data-ttu-id="fc6a7-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6a7-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc6a7-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6a7-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc6a7-151">INPUTS</span></span>

### <span data-ttu-id="fc6a7-152">Dizisi</span><span class="sxs-lookup"><span data-stu-id="fc6a7-152">String</span></span>

## <span data-ttu-id="fc6a7-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc6a7-153">OUTPUTS</span></span>

### <span data-ttu-id="fc6a7-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc6a7-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="fc6a7-155">Bu cmdlet yalnızca *geçiş parametresini belirttiğinizde* bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc6a7-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="fc6a7-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc6a7-156">NOTES</span></span>

## <span data-ttu-id="fc6a7-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc6a7-157">RELATED LINKS</span></span>

[<span data-ttu-id="fc6a7-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc6a7-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="fc6a7-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fc6a7-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="fc6a7-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="fc6a7-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="fc6a7-161">Geri al-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fc6a7-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

