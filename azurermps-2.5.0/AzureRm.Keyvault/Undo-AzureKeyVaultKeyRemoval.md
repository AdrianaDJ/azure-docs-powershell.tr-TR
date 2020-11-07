---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939368"
---
# <span data-ttu-id="48471-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="48471-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="48471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48471-102">SYNOPSIS</span></span>
<span data-ttu-id="48471-103">Anahtar kasasına silinen anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="48471-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48471-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48471-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48471-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48471-105">DESCRIPTION</span></span>
<span data-ttu-id="48471-106">**Undo-AzureKeyVaultKeyRemoval** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="48471-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="48471-107">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="48471-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="48471-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="48471-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="48471-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48471-109">EXAMPLES</span></span>

### <span data-ttu-id="48471-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48471-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="48471-111">Bu komut, önceden silinen ' MyKey ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="48471-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="48471-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48471-112">PARAMETERS</span></span>

### <span data-ttu-id="48471-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48471-113">-DefaultProfile</span></span>
<span data-ttu-id="48471-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="48471-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48471-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="48471-115">-Name</span></span>
<span data-ttu-id="48471-116">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="48471-116">Key name.</span></span>
<span data-ttu-id="48471-117">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48471-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="48471-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="48471-118">-VaultName</span></span>
<span data-ttu-id="48471-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="48471-119">Vault name.</span></span>
<span data-ttu-id="48471-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48471-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="48471-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="48471-121">-Confirm</span></span>
<span data-ttu-id="48471-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48471-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48471-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48471-123">-WhatIf</span></span>
<span data-ttu-id="48471-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48471-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48471-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48471-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48471-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48471-126">CommonParameters</span></span>
<span data-ttu-id="48471-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48471-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48471-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48471-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48471-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48471-129">INPUTS</span></span>

### <span data-ttu-id="48471-130">System. String</span><span class="sxs-lookup"><span data-stu-id="48471-130">System.String</span></span>

## <span data-ttu-id="48471-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48471-131">OUTPUTS</span></span>

### <span data-ttu-id="48471-132">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="48471-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="48471-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48471-133">NOTES</span></span>

## <span data-ttu-id="48471-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48471-134">RELATED LINKS</span></span>

[<span data-ttu-id="48471-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48471-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="48471-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48471-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="48471-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="48471-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

