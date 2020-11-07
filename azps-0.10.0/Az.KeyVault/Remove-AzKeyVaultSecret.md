---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935769"
---
# <span data-ttu-id="87056-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="87056-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="87056-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87056-102">SYNOPSIS</span></span>
<span data-ttu-id="87056-103">Anahtar kasasındaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="87056-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="87056-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="87056-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87056-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="87056-105">DESCRIPTION</span></span>
<span data-ttu-id="87056-106">Remove-AzKeyVaultSecret cmdlet 'i anahtar kasadaki parolayı siler.</span><span class="sxs-lookup"><span data-stu-id="87056-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="87056-107">Parola yanlışlıkla silindiyse, parola, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzKeyVaultSecretRemoval kullanılarak kurtarılabilir.</span><span class="sxs-lookup"><span data-stu-id="87056-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="87056-108">Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.</span><span class="sxs-lookup"><span data-stu-id="87056-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="87056-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="87056-109">EXAMPLES</span></span>

### <span data-ttu-id="87056-110">Örnek 1: anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="87056-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="87056-111">Bu komut, contoso. ' adlı anahtar kasasından gizli adlandırılmış FinanceSecret 'i kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87056-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="87056-112">Örnek 2: Kullanıcı onayı olmadan bir anahtar kasasından parolayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="87056-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="87056-113">Bu komut, contoso adlı anahtar kasasından gizli adlandırılmış Finans\gizli adını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87056-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="87056-114">Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="87056-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="87056-115">Örnek 3: anahtar kasasından kalıcı olarak silinen parolayı</span><span class="sxs-lookup"><span data-stu-id="87056-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="87056-116">Bu komut, contoso ile kalıcı olarak adlandırılan anahtar kasasından gizli adlandırılmış Finans\gizli adını temizler.</span><span class="sxs-lookup"><span data-stu-id="87056-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="87056-117">Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.</span><span class="sxs-lookup"><span data-stu-id="87056-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="87056-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="87056-118">PARAMETERS</span></span>

### <span data-ttu-id="87056-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87056-119">-DefaultProfile</span></span>
<span data-ttu-id="87056-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="87056-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87056-121">-Force</span><span class="sxs-lookup"><span data-stu-id="87056-121">-Force</span></span>
<span data-ttu-id="87056-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="87056-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87056-123">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="87056-123">-InRemovedState</span></span>
<span data-ttu-id="87056-124">Varsa, önceden silinmiş gizli kod dizesini kalıcı olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="87056-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="87056-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="87056-125">-Name</span></span>
<span data-ttu-id="87056-126">Parolanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87056-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="87056-127">Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87056-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87056-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="87056-128">-PassThru</span></span>
<span data-ttu-id="87056-129">Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. modeller. Secret** nesnesi döndürmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87056-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="87056-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="87056-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="87056-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="87056-131">-VaultName</span></span>
<span data-ttu-id="87056-132">Gizliliğin ait olduğu Anahtar Kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="87056-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="87056-133">Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="87056-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="87056-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="87056-134">-Confirm</span></span>
<span data-ttu-id="87056-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="87056-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87056-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87056-136">-WhatIf</span></span>
<span data-ttu-id="87056-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87056-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87056-138">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="87056-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87056-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="87056-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87056-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87056-140">CommonParameters</span></span>
<span data-ttu-id="87056-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="87056-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87056-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87056-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87056-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="87056-143">INPUTS</span></span>

### <span data-ttu-id="87056-144">Dizisi</span><span class="sxs-lookup"><span data-stu-id="87056-144">String</span></span>

## <span data-ttu-id="87056-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="87056-145">OUTPUTS</span></span>

### <span data-ttu-id="87056-146">Microsoft. Azure. Commands. Keykasa. modeller. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="87056-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="87056-147">Bu cmdlet yalnızca *geçiş parametresini belirttiğinizde* bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="87056-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="87056-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="87056-148">NOTES</span></span>

## <span data-ttu-id="87056-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="87056-149">RELATED LINKS</span></span>

[<span data-ttu-id="87056-150">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="87056-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="87056-151">Set-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="87056-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="87056-152">Geri al-Azanahtarvaultsecretkaldırmada</span><span class="sxs-lookup"><span data-stu-id="87056-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

