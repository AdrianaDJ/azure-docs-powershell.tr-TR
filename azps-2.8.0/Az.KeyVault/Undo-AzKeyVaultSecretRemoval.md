---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 26bf7b91b330032e05f96f425cb21908fc3df55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751608"
---
# <span data-ttu-id="9c0cc-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="9c0cc-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="9c0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0cc-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="9c0cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c0cc-104">SYNTAX</span></span>

### <span data-ttu-id="9c0cc-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c0cc-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c0cc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9c0cc-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c0cc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c0cc-107">DESCRIPTION</span></span>
<span data-ttu-id="9c0cc-108">**Undo-Azanahtarvaultsecretkaldýrma** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="9c0cc-109">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="9c0cc-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="9c0cc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c0cc-111">EXAMPLES</span></span>

### <span data-ttu-id="9c0cc-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c0cc-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="9c0cc-113">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="9c0cc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c0cc-114">PARAMETERS</span></span>

### <span data-ttu-id="9c0cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0cc-115">-DefaultProfile</span></span>
<span data-ttu-id="9c0cc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9c0cc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c0cc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c0cc-117">-InputObject</span></span>
<span data-ttu-id="9c0cc-118">Silinen gizli nesne</span><span class="sxs-lookup"><span data-stu-id="9c0cc-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c0cc-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c0cc-119">-Name</span></span>
<span data-ttu-id="9c0cc-120">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-120">Secret name.</span></span>
<span data-ttu-id="9c0cc-121">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="9c0cc-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9c0cc-122">-VaultName</span></span>
<span data-ttu-id="9c0cc-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-123">Vault name.</span></span>
<span data-ttu-id="9c0cc-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9c0cc-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c0cc-125">-Confirm</span></span>
<span data-ttu-id="9c0cc-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c0cc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c0cc-127">-WhatIf</span></span>
<span data-ttu-id="9c0cc-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c0cc-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c0cc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0cc-130">CommonParameters</span></span>
<span data-ttu-id="9c0cc-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c0cc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0cc-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c0cc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0cc-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c0cc-133">INPUTS</span></span>

### <span data-ttu-id="9c0cc-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="9c0cc-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="9c0cc-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c0cc-135">OUTPUTS</span></span>

### <span data-ttu-id="9c0cc-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9c0cc-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="9c0cc-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c0cc-137">NOTES</span></span>

## <span data-ttu-id="9c0cc-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c0cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="9c0cc-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9c0cc-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="9c0cc-140">Add-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="9c0cc-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="9c0cc-141">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="9c0cc-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
