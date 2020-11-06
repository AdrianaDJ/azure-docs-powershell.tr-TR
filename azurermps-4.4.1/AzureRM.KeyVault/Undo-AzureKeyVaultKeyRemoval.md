---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594242"
---
# <span data-ttu-id="2af61-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2af61-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="2af61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2af61-102">SYNOPSIS</span></span>
<span data-ttu-id="2af61-103">Anahtar kasasına silinen anahtarı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2af61-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2af61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2af61-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2af61-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2af61-105">DESCRIPTION</span></span>
<span data-ttu-id="2af61-106">**Undo-AzureKeyVaultKeyRemoval** cmdlet 'i önceden silinmiş bir anahtarı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2af61-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="2af61-107">Kurtarılan anahtar etkin olacak ve tüm normal anahtar işlemlerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2af61-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="2af61-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2af61-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2af61-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2af61-109">EXAMPLES</span></span>

### <span data-ttu-id="2af61-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2af61-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="2af61-111">Bu komut, önceden silinen ' MyKey ' anahtarını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2af61-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2af61-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2af61-112">PARAMETERS</span></span>

### <span data-ttu-id="2af61-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="2af61-113">-Name</span></span>
<span data-ttu-id="2af61-114">Anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="2af61-114">Key name.</span></span>
<span data-ttu-id="2af61-115">Cmdlet, kasa adından bir anahtarın FQDN 'sini, şu anda seçili olan ortamı ve anahtar adını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af61-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af61-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2af61-116">-VaultName</span></span>
<span data-ttu-id="2af61-117">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2af61-117">Vault name.</span></span>
<span data-ttu-id="2af61-118">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2af61-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2af61-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="2af61-119">-Confirm</span></span>
<span data-ttu-id="2af61-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2af61-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2af61-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2af61-121">-WhatIf</span></span>
<span data-ttu-id="2af61-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2af61-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2af61-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2af61-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2af61-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2af61-124">-DefaultProfile</span></span>
<span data-ttu-id="2af61-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2af61-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2af61-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2af61-126">CommonParameters</span></span>
<span data-ttu-id="2af61-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2af61-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2af61-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2af61-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2af61-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2af61-129">INPUTS</span></span>

### <span data-ttu-id="2af61-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2af61-130">System.String</span></span>

## <span data-ttu-id="2af61-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2af61-131">OUTPUTS</span></span>

### <span data-ttu-id="2af61-132">Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti</span><span class="sxs-lookup"><span data-stu-id="2af61-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="2af61-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2af61-133">NOTES</span></span>

## <span data-ttu-id="2af61-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2af61-134">RELATED LINKS</span></span>

[<span data-ttu-id="2af61-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2af61-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="2af61-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2af61-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="2af61-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2af61-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

