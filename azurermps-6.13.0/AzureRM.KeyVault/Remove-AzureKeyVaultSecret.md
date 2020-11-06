---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590229"
---
# <span data-ttu-id="06251-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="06251-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="06251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06251-102">SYNOPSIS</span></span>
<span data-ttu-id="06251-103">Anahtar kasasındaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="06251-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06251-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06251-104">SYNTAX</span></span>

### <span data-ttu-id="06251-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06251-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06251-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="06251-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06251-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="06251-107">DESCRIPTION</span></span>
<span data-ttu-id="06251-108">Remove-AzureKeyVaultSecret cmdlet 'i anahtar kasadaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="06251-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="06251-109">Parola yanlışlıkla silindiyse, parola, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzureKeyVaultSecretRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="06251-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="06251-110">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="06251-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="06251-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06251-111">EXAMPLES</span></span>

### <span data-ttu-id="06251-112">Örnek 1: anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="06251-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="06251-113">Bu komut, contoso. ' adlı anahtar kasasından gizli adlandırılmış FinanceSecret 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06251-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="06251-114">Örnek 2: Kullanıcı onayı olmadan bir anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="06251-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="06251-115">Bu komut, contoso adlı anahtar kasasından gizli adlandırılmış Finans\gizli adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06251-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="06251-116">Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="06251-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="06251-117">Örnek 3: anahtar kasasından kalıcı olarak silinen parolayı</span><span class="sxs-lookup"><span data-stu-id="06251-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="06251-118">Bu komut, contoso ile kalıcı olarak adlandırılan anahtar kasasından gizli adlandırılmış Finans\gizli adını temizler.</span><span class="sxs-lookup"><span data-stu-id="06251-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="06251-119">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="06251-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="06251-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06251-120">PARAMETERS</span></span>

### <span data-ttu-id="06251-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06251-121">-DefaultProfile</span></span>
<span data-ttu-id="06251-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="06251-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06251-123">-Force</span><span class="sxs-lookup"><span data-stu-id="06251-123">-Force</span></span>
<span data-ttu-id="06251-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="06251-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06251-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06251-125">-InputObject</span></span>
<span data-ttu-id="06251-126">Anahtar Kasası gizli nesnesi</span><span class="sxs-lookup"><span data-stu-id="06251-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06251-127">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="06251-127">-InRemovedState</span></span>
<span data-ttu-id="06251-128">Varsa, önceden silinmiş gizli kod dizesini kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="06251-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="06251-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="06251-129">-Name</span></span>
<span data-ttu-id="06251-130">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06251-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="06251-131">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06251-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06251-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="06251-132">-PassThru</span></span>
<span data-ttu-id="06251-133">Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. modeller. Secret** nesnesi döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="06251-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="06251-134">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="06251-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="06251-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="06251-135">-VaultName</span></span>
<span data-ttu-id="06251-136">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06251-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="06251-137">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06251-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="06251-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="06251-138">-Confirm</span></span>
<span data-ttu-id="06251-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06251-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06251-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06251-140">-WhatIf</span></span>
<span data-ttu-id="06251-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06251-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06251-142">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06251-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06251-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06251-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06251-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06251-144">CommonParameters</span></span>
<span data-ttu-id="06251-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06251-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06251-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06251-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06251-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06251-147">INPUTS</span></span>

### <span data-ttu-id="06251-148">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="06251-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="06251-149">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06251-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="06251-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06251-150">OUTPUTS</span></span>

### <span data-ttu-id="06251-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="06251-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="06251-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06251-152">NOTES</span></span>

## <span data-ttu-id="06251-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06251-153">RELATED LINKS</span></span>

[<span data-ttu-id="06251-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="06251-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="06251-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="06251-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="06251-156">Geri al-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="06251-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

