---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587548"
---
# <span data-ttu-id="055d5-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="055d5-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="055d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055d5-102">SYNOPSIS</span></span>
<span data-ttu-id="055d5-103">Anahtar kasasına silinen anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="055d5-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="055d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="055d5-104">SYNTAX</span></span>

### <span data-ttu-id="055d5-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="055d5-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="055d5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="055d5-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="055d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="055d5-107">DESCRIPTION</span></span>
<span data-ttu-id="055d5-108">**Undo-AzureKeyVaultKeyRemoval** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="055d5-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="055d5-109">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="055d5-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="055d5-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="055d5-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="055d5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="055d5-111">EXAMPLES</span></span>

### <span data-ttu-id="055d5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="055d5-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="055d5-113">Bu komut, önceden silinen ' MyKey ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="055d5-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="055d5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="055d5-114">PARAMETERS</span></span>

### <span data-ttu-id="055d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055d5-115">-DefaultProfile</span></span>
<span data-ttu-id="055d5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="055d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="055d5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="055d5-117">-InputObject</span></span>
<span data-ttu-id="055d5-118">Anahtar nesne silindi</span><span class="sxs-lookup"><span data-stu-id="055d5-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="055d5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="055d5-119">-Name</span></span>
<span data-ttu-id="055d5-120">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="055d5-120">Key name.</span></span>
<span data-ttu-id="055d5-121">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="055d5-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055d5-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="055d5-122">-VaultName</span></span>
<span data-ttu-id="055d5-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="055d5-123">Vault name.</span></span>
<span data-ttu-id="055d5-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="055d5-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="055d5-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="055d5-125">-Confirm</span></span>
<span data-ttu-id="055d5-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="055d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055d5-127">-WhatIf</span></span>
<span data-ttu-id="055d5-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="055d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="055d5-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="055d5-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="055d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055d5-130">CommonParameters</span></span>
<span data-ttu-id="055d5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="055d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055d5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="055d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055d5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="055d5-133">INPUTS</span></span>

### <span data-ttu-id="055d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="055d5-134">System.String</span></span>

## <span data-ttu-id="055d5-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="055d5-135">OUTPUTS</span></span>

### <span data-ttu-id="055d5-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="055d5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="055d5-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="055d5-137">NOTES</span></span>

## <span data-ttu-id="055d5-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="055d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="055d5-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="055d5-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="055d5-140">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="055d5-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="055d5-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="055d5-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

