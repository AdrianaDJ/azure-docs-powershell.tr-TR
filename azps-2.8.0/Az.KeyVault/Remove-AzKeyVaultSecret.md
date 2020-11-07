---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: 2c52d6cbd5a3e027baf41959d28816f63062b046
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751639"
---
# <span data-ttu-id="ab03c-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ab03c-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ab03c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab03c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab03c-103">Anahtar kasasındaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="ab03c-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="ab03c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab03c-104">SYNTAX</span></span>

### <span data-ttu-id="ab03c-105">ByVaultName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab03c-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab03c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab03c-106">ByInputObject</span></span>
```
Remove-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab03c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab03c-107">DESCRIPTION</span></span>
<span data-ttu-id="ab03c-108">Remove-AzKeyVaultSecret cmdlet 'i anahtar kasadaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="ab03c-108">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="ab03c-109">Parola yanlışlıkla silindiyse, parola, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzKeyVaultSecretRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="ab03c-110">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="ab03c-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="ab03c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab03c-111">EXAMPLES</span></span>

### <span data-ttu-id="ab03c-112">Örnek 1: anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ab03c-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

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

<span data-ttu-id="ab03c-113">Bu komut, contoso. ' adlı anahtar kasasından gizli adlandırılmış FinanceSecret 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab03c-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="ab03c-114">Örnek 2: Kullanıcı onayı olmadan bir anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ab03c-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

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

<span data-ttu-id="ab03c-115">Bu komut, contoso adlı anahtar kasasından gizli adlandırılmış Finans\gizli adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab03c-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="ab03c-116">Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="ab03c-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="ab03c-117">Örnek 3: anahtar kasasından kalıcı olarak silinen parolayı</span><span class="sxs-lookup"><span data-stu-id="ab03c-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="ab03c-118">Bu komut, contoso ile kalıcı olarak adlandırılan anahtar kasasından gizli adlandırılmış Finans\gizli adını temizler.</span><span class="sxs-lookup"><span data-stu-id="ab03c-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="ab03c-119">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="ab03c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab03c-120">PARAMETERS</span></span>

### <span data-ttu-id="ab03c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab03c-121">-DefaultProfile</span></span>
<span data-ttu-id="ab03c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ab03c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab03c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ab03c-123">-Force</span></span>
<span data-ttu-id="ab03c-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ab03c-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab03c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab03c-125">-InputObject</span></span>
<span data-ttu-id="ab03c-126">Anahtar Kasası gizli nesnesi</span><span class="sxs-lookup"><span data-stu-id="ab03c-126">Key Vault Secret Object</span></span>

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

### <span data-ttu-id="ab03c-127">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="ab03c-127">-InRemovedState</span></span>
<span data-ttu-id="ab03c-128">Varsa, önceden silinmiş gizli kod dizesini kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab03c-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="ab03c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab03c-129">-Name</span></span>
<span data-ttu-id="ab03c-130">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="ab03c-131">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab03c-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="ab03c-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ab03c-132">-PassThru</span></span>
<span data-ttu-id="ab03c-133">Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. modeller. Secret** nesnesi döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="ab03c-134">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ab03c-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ab03c-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ab03c-135">-VaultName</span></span>
<span data-ttu-id="ab03c-136">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="ab03c-137">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ab03c-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="ab03c-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab03c-138">-Confirm</span></span>
<span data-ttu-id="ab03c-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab03c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab03c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab03c-140">-WhatIf</span></span>
<span data-ttu-id="ab03c-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab03c-142">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab03c-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab03c-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab03c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab03c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab03c-144">CommonParameters</span></span>
<span data-ttu-id="ab03c-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab03c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab03c-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab03c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab03c-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab03c-147">INPUTS</span></span>

### <span data-ttu-id="ab03c-148">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="ab03c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="ab03c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab03c-149">OUTPUTS</span></span>

### <span data-ttu-id="ab03c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ab03c-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="ab03c-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab03c-151">NOTES</span></span>

## <span data-ttu-id="ab03c-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab03c-152">RELATED LINKS</span></span>

[<span data-ttu-id="ab03c-153">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="ab03c-153">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="ab03c-154">Set-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="ab03c-154">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="ab03c-155">Geri al-Azanahtarvaultsecretkaldırmada</span><span class="sxs-lookup"><span data-stu-id="ab03c-155">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

