---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319885"
---
# <span data-ttu-id="06082-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="06082-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="06082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06082-102">SYNOPSIS</span></span>
<span data-ttu-id="06082-103">Anahtar kasasına silinen anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="06082-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="06082-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06082-104">SYNTAX</span></span>

### <span data-ttu-id="06082-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06082-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06082-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="06082-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06082-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="06082-107">DESCRIPTION</span></span>
<span data-ttu-id="06082-108">**Undo-Azanahtarvaultkeykaldırmada** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="06082-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="06082-109">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="06082-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="06082-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="06082-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="06082-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06082-111">EXAMPLES</span></span>

### <span data-ttu-id="06082-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06082-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="06082-113">Bu komut, önceden silinen ' MyKey ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="06082-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="06082-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06082-114">PARAMETERS</span></span>

### <span data-ttu-id="06082-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06082-115">-DefaultProfile</span></span>
<span data-ttu-id="06082-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="06082-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06082-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06082-117">-InputObject</span></span>
<span data-ttu-id="06082-118">Anahtar nesne silindi</span><span class="sxs-lookup"><span data-stu-id="06082-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06082-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="06082-119">-Name</span></span>
<span data-ttu-id="06082-120">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="06082-120">Key name.</span></span>
<span data-ttu-id="06082-121">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06082-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="06082-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="06082-122">-VaultName</span></span>
<span data-ttu-id="06082-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="06082-123">Vault name.</span></span>
<span data-ttu-id="06082-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06082-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="06082-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="06082-125">-Confirm</span></span>
<span data-ttu-id="06082-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06082-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06082-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06082-127">-WhatIf</span></span>
<span data-ttu-id="06082-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06082-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06082-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06082-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06082-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06082-130">CommonParameters</span></span>
<span data-ttu-id="06082-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06082-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06082-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="06082-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06082-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06082-133">INPUTS</span></span>

### <span data-ttu-id="06082-134">Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem</span><span class="sxs-lookup"><span data-stu-id="06082-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="06082-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06082-135">OUTPUTS</span></span>

### <span data-ttu-id="06082-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="06082-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="06082-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06082-137">NOTES</span></span>

## <span data-ttu-id="06082-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06082-138">RELATED LINKS</span></span>

[<span data-ttu-id="06082-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="06082-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="06082-140">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="06082-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="06082-141">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="06082-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

