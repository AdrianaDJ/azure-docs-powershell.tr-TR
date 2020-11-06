---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591667"
---
# <span data-ttu-id="54fed-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="54fed-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="54fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54fed-102">SYNOPSIS</span></span>
<span data-ttu-id="54fed-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="54fed-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54fed-104">SYNTAX</span></span>

### <span data-ttu-id="54fed-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54fed-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54fed-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="54fed-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54fed-107">DESCRIPTION</span></span>
<span data-ttu-id="54fed-108">**Undo-AzureKeyVaultSecretRemoval** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="54fed-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="54fed-109">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="54fed-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="54fed-110">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="54fed-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="54fed-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54fed-111">EXAMPLES</span></span>

### <span data-ttu-id="54fed-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="54fed-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="54fed-113">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="54fed-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="54fed-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54fed-114">PARAMETERS</span></span>

### <span data-ttu-id="54fed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fed-115">-DefaultProfile</span></span>
<span data-ttu-id="54fed-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="54fed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54fed-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54fed-117">-InputObject</span></span>
<span data-ttu-id="54fed-118">Silinen gizli nesne</span><span class="sxs-lookup"><span data-stu-id="54fed-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54fed-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="54fed-119">-Name</span></span>
<span data-ttu-id="54fed-120">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="54fed-120">Secret name.</span></span>
<span data-ttu-id="54fed-121">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fed-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54fed-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="54fed-122">-VaultName</span></span>
<span data-ttu-id="54fed-123">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="54fed-123">Vault name.</span></span>
<span data-ttu-id="54fed-124">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="54fed-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="54fed-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="54fed-125">-Confirm</span></span>
<span data-ttu-id="54fed-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54fed-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fed-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fed-127">-WhatIf</span></span>
<span data-ttu-id="54fed-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54fed-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fed-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54fed-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fed-130">CommonParameters</span></span>
<span data-ttu-id="54fed-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54fed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fed-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fed-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fed-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54fed-133">INPUTS</span></span>

### <span data-ttu-id="54fed-134">System. String</span><span class="sxs-lookup"><span data-stu-id="54fed-134">System.String</span></span>

## <span data-ttu-id="54fed-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54fed-135">OUTPUTS</span></span>

### <span data-ttu-id="54fed-136">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54fed-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="54fed-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54fed-137">NOTES</span></span>

## <span data-ttu-id="54fed-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54fed-138">RELATED LINKS</span></span>

[<span data-ttu-id="54fed-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54fed-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="54fed-140">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54fed-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="54fed-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="54fed-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
