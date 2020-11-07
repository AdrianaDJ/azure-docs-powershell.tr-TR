---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 911ea06fdfa9d4d90f8c9935e3e98c026c70cce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938833"
---
# <span data-ttu-id="8e0a4-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e0a4-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="8e0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0a4-103">Anahtar kasasındaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e0a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e0a4-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e0a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e0a4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e0a4-106">Remove-AzureKeyVaultKey cmdlet 'i anahtar kasadaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-106">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="8e0a4-107">Anahtar yanlışlıkla silinmişse anahtar, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzureKeyVaultKeyRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-107">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="8e0a4-108">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="8e0a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e0a4-109">EXAMPLES</span></span>

### <span data-ttu-id="8e0a4-110">Örnek 1: anahtar kasasından anahtar kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e0a4-110">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="8e0a4-111">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-111">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="8e0a4-112">Örnek 2: Kullanıcı onayı olmadan bir anahtarı kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e0a4-112">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="8e0a4-113">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="8e0a4-114">Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="8e0a4-115">Örnek 3: silinen anahtarı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="8e0a4-115">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="8e0a4-116">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı temizler.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-116">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="8e0a4-117">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="8e0a4-118">Örnek 4: ardışık düzen işlecini kullanarak anahtarları kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e0a4-118">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="8e0a4-119">Bu komut contoso adlı anahtar kasasındaki tüm anahtarları alır ve ardışık düzen işlecini kullanarak bunları **nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-119">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e0a4-120">Bu cmdlet geçerli cmdlet 'e **Enabled** özniteliği için $false değeri olan anahtarları geçirir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-120">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="8e0a4-121">Bu cmdlet bu tuşları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-121">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="8e0a4-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e0a4-122">PARAMETERS</span></span>

### <span data-ttu-id="8e0a4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e0a4-123">-DefaultProfile</span></span>
<span data-ttu-id="8e0a4-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8e0a4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e0a4-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8e0a4-125">-Force</span></span>
<span data-ttu-id="8e0a4-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e0a4-127">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="8e0a4-127">-InRemovedState</span></span>
<span data-ttu-id="8e0a4-128">Önceden silinen anahtarı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-128">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="8e0a4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e0a4-129">-Name</span></span>
<span data-ttu-id="8e0a4-130">Kaldırılacak anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-130">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="8e0a4-131">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-131">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0a4-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8e0a4-132">-PassThru</span></span>
<span data-ttu-id="8e0a4-133">Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** nesnesi döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="8e0a4-134">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8e0a4-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8e0a4-135">-VaultName</span></span>
<span data-ttu-id="8e0a4-136">Anahtarın kaldırılacağı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-136">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="8e0a4-137">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e0a4-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e0a4-138">-Confirm</span></span>
<span data-ttu-id="8e0a4-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e0a4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e0a4-140">-WhatIf</span></span>
<span data-ttu-id="8e0a4-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e0a4-142">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e0a4-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e0a4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0a4-144">CommonParameters</span></span>
<span data-ttu-id="8e0a4-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0a4-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e0a4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0a4-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e0a4-147">INPUTS</span></span>

### <span data-ttu-id="8e0a4-148">Dizisi</span><span class="sxs-lookup"><span data-stu-id="8e0a4-148">String</span></span>

## <span data-ttu-id="8e0a4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e0a4-149">OUTPUTS</span></span>

### <span data-ttu-id="8e0a4-150">Microsoft. Azure. Commands. Keykasa. modeller. Deletedkeydemeti</span><span class="sxs-lookup"><span data-stu-id="8e0a4-150">Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>
<span data-ttu-id="8e0a4-151">Bu cmdlet yalnızca *geçiş parametresini belirttiğinizde* bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e0a4-151">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="8e0a4-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e0a4-152">NOTES</span></span>

## <span data-ttu-id="8e0a4-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e0a4-153">RELATED LINKS</span></span>

[<span data-ttu-id="8e0a4-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e0a4-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="8e0a4-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8e0a4-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="8e0a4-156">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="8e0a4-156">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="8e0a4-157">Geri al-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8e0a4-157">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

