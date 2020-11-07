---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 1eca5a380dc71a5bd801c21bb7e7f556fcff0d35
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937738"
---
# <span data-ttu-id="9fdb9-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="9fdb9-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="9fdb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fdb9-102">SYNOPSIS</span></span>
<span data-ttu-id="9fdb9-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="9fdb9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fdb9-104">SYNTAX</span></span>

### <span data-ttu-id="9fdb9-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fdb9-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fdb9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9fdb9-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fdb9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fdb9-107">DESCRIPTION</span></span>
<span data-ttu-id="9fdb9-108">**Undo-Azanahtarvaultsecretkaldýrma** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="9fdb9-109">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="9fdb9-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="9fdb9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fdb9-111">EXAMPLES</span></span>

### <span data-ttu-id="9fdb9-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9fdb9-112">Example 1</span></span>
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

<span data-ttu-id="9fdb9-113">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="9fdb9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fdb9-114">PARAMETERS</span></span>

### <span data-ttu-id="9fdb9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fdb9-115">-DefaultProfile</span></span>
<span data-ttu-id="9fdb9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9fdb9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fdb9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fdb9-117">-InputObject</span></span>
<span data-ttu-id="9fdb9-118">Silinen gizli nesne</span><span class="sxs-lookup"><span data-stu-id="9fdb9-118">Deleted secret object</span></span>

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

### <span data-ttu-id="9fdb9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fdb9-119">-Name</span></span>
<span data-ttu-id="9fdb9-120">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-120">Secret name.</span></span>
<span data-ttu-id="9fdb9-121">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="9fdb9-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9fdb9-122">-VaultName</span></span>
<span data-ttu-id="9fdb9-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-123">Vault name.</span></span>
<span data-ttu-id="9fdb9-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9fdb9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fdb9-125">-Confirm</span></span>
<span data-ttu-id="9fdb9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fdb9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fdb9-127">-WhatIf</span></span>
<span data-ttu-id="9fdb9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fdb9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fdb9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fdb9-130">CommonParameters</span></span>
<span data-ttu-id="9fdb9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fdb9-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9fdb9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fdb9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fdb9-133">INPUTS</span></span>

### <span data-ttu-id="9fdb9-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultsecretidentityıtem</span><span class="sxs-lookup"><span data-stu-id="9fdb9-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="9fdb9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fdb9-135">OUTPUTS</span></span>

### <span data-ttu-id="9fdb9-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9fdb9-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="9fdb9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fdb9-137">NOTES</span></span>

## <span data-ttu-id="9fdb9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fdb9-138">RELATED LINKS</span></span>

[<span data-ttu-id="9fdb9-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9fdb9-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="9fdb9-140">Add-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="9fdb9-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="9fdb9-141">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="9fdb9-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
