---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: ff7e5a02899d806633e485f06f419a6f1f2082a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590914"
---
# <span data-ttu-id="62d4f-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="62d4f-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="62d4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="62d4f-103">Anahtar kasasındaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="62d4f-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62d4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62d4f-104">SYNTAX</span></span>

### <span data-ttu-id="62d4f-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62d4f-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d4f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="62d4f-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d4f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="62d4f-107">DESCRIPTION</span></span>
<span data-ttu-id="62d4f-108">Remove-AzureKeyVaultKey cmdlet 'i anahtar kasadaki bir anahtarı siler.</span><span class="sxs-lookup"><span data-stu-id="62d4f-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="62d4f-109">Anahtar yanlışlıkla silinmişse anahtar, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzureKeyVaultKeyRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="62d4f-110">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="62d4f-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="62d4f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62d4f-111">EXAMPLES</span></span>

### <span data-ttu-id="62d4f-112">Örnek 1: anahtar kasasından anahtar kaldırma</span><span class="sxs-lookup"><span data-stu-id="62d4f-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="62d4f-113">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d4f-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="62d4f-114">Örnek 2: Kullanıcı onayı olmadan bir anahtarı kaldırma</span><span class="sxs-lookup"><span data-stu-id="62d4f-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="62d4f-115">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d4f-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="62d4f-116">Komut *Force* parametresini belirtir ve bu nedenle cmdlet sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="62d4f-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="62d4f-117">Örnek 3: silinen anahtarı anahtar kasasından kalıcı olarak Temizleme</span><span class="sxs-lookup"><span data-stu-id="62d4f-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="62d4f-118">Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı temizler.</span><span class="sxs-lookup"><span data-stu-id="62d4f-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="62d4f-119">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="62d4f-120">Örnek 4: ardışık düzen işlecini kullanarak anahtarları kaldırma</span><span class="sxs-lookup"><span data-stu-id="62d4f-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="62d4f-121">Bu komut contoso adlı anahtar kasasındaki tüm anahtarları alır ve ardışık düzen işlecini kullanarak bunları **nesne** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="62d4f-122">Bu cmdlet geçerli cmdlet 'e **Enabled** özniteliği için $false değeri olan anahtarları geçirir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="62d4f-123">Bu cmdlet bu tuşları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d4f-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="62d4f-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62d4f-124">PARAMETERS</span></span>

### <span data-ttu-id="62d4f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d4f-125">-DefaultProfile</span></span>
<span data-ttu-id="62d4f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="62d4f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62d4f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="62d4f-127">-Force</span></span>
<span data-ttu-id="62d4f-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="62d4f-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62d4f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62d4f-129">-InputObject</span></span>
<span data-ttu-id="62d4f-130">AnahtarPaketi nesnesi</span><span class="sxs-lookup"><span data-stu-id="62d4f-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d4f-131">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="62d4f-131">-InRemovedState</span></span>
<span data-ttu-id="62d4f-132">Önceden silinen anahtarı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="62d4f-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="62d4f-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="62d4f-133">-Name</span></span>
<span data-ttu-id="62d4f-134">Kaldırılacak anahtarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="62d4f-135">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62d4f-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d4f-136">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="62d4f-136">-PassThru</span></span>
<span data-ttu-id="62d4f-137">Bu cmdlet 'in **Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey** nesnesini döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="62d4f-138">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="62d4f-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62d4f-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="62d4f-139">-VaultName</span></span>
<span data-ttu-id="62d4f-140">Anahtarın kaldırılacağı Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="62d4f-141">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62d4f-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d4f-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="62d4f-142">-Confirm</span></span>
<span data-ttu-id="62d4f-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62d4f-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d4f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d4f-144">-WhatIf</span></span>
<span data-ttu-id="62d4f-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d4f-146">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62d4f-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d4f-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62d4f-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d4f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d4f-148">CommonParameters</span></span>
<span data-ttu-id="62d4f-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62d4f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d4f-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62d4f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d4f-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62d4f-151">INPUTS</span></span>

### <span data-ttu-id="62d4f-152">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="62d4f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="62d4f-153">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="62d4f-153">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="62d4f-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62d4f-154">OUTPUTS</span></span>

### <span data-ttu-id="62d4f-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="62d4f-155">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="62d4f-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62d4f-156">NOTES</span></span>

## <span data-ttu-id="62d4f-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62d4f-157">RELATED LINKS</span></span>

[<span data-ttu-id="62d4f-158">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="62d4f-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="62d4f-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="62d4f-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="62d4f-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="62d4f-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="62d4f-161">Geri al-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="62d4f-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)
