---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936645"
---
# <span data-ttu-id="61830-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="61830-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="61830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61830-102">SYNOPSIS</span></span>
<span data-ttu-id="61830-103">Anahtar kasasına silinen anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="61830-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="61830-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61830-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61830-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61830-105">DESCRIPTION</span></span>
<span data-ttu-id="61830-106">**Undo-Azanahtarvaultkeykaldırmada** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="61830-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="61830-107">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="61830-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="61830-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="61830-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="61830-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61830-109">EXAMPLES</span></span>

### <span data-ttu-id="61830-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61830-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="61830-111">Bu komut, önceden silinen ' MyKey ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="61830-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="61830-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61830-112">PARAMETERS</span></span>

### <span data-ttu-id="61830-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61830-113">-DefaultProfile</span></span>
<span data-ttu-id="61830-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61830-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61830-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="61830-115">-Name</span></span>
<span data-ttu-id="61830-116">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="61830-116">Key name.</span></span>
<span data-ttu-id="61830-117">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61830-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="61830-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="61830-118">-VaultName</span></span>
<span data-ttu-id="61830-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="61830-119">Vault name.</span></span>
<span data-ttu-id="61830-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61830-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="61830-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="61830-121">-Confirm</span></span>
<span data-ttu-id="61830-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61830-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61830-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61830-123">-WhatIf</span></span>
<span data-ttu-id="61830-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61830-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61830-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61830-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61830-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61830-126">CommonParameters</span></span>
<span data-ttu-id="61830-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61830-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61830-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61830-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61830-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61830-129">INPUTS</span></span>

### <span data-ttu-id="61830-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61830-130">System.String</span></span>

## <span data-ttu-id="61830-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61830-131">OUTPUTS</span></span>

### <span data-ttu-id="61830-132">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="61830-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="61830-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61830-133">NOTES</span></span>

## <span data-ttu-id="61830-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61830-134">RELATED LINKS</span></span>

[<span data-ttu-id="61830-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="61830-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="61830-136">Add-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="61830-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="61830-137">Get-Azanahtarvaultkey</span><span class="sxs-lookup"><span data-stu-id="61830-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

