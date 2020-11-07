---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763722"
---
# <span data-ttu-id="847c2-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="847c2-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="847c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="847c2-102">SYNOPSIS</span></span>
<span data-ttu-id="847c2-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="847c2-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="847c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="847c2-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="847c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="847c2-105">DESCRIPTION</span></span>
<span data-ttu-id="847c2-106">**Undo-AzureKeyVaultSecretRemoval** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="847c2-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="847c2-107">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="847c2-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="847c2-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="847c2-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="847c2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="847c2-109">EXAMPLES</span></span>

### <span data-ttu-id="847c2-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="847c2-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="847c2-111">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="847c2-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="847c2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="847c2-112">PARAMETERS</span></span>

### <span data-ttu-id="847c2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="847c2-113">-Name</span></span>
<span data-ttu-id="847c2-114">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="847c2-114">Secret name.</span></span>
<span data-ttu-id="847c2-115">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="847c2-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="847c2-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="847c2-116">-VaultName</span></span>
<span data-ttu-id="847c2-117">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="847c2-117">Vault name.</span></span>
<span data-ttu-id="847c2-118">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="847c2-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="847c2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="847c2-119">-Confirm</span></span>
<span data-ttu-id="847c2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="847c2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="847c2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="847c2-121">-WhatIf</span></span>
<span data-ttu-id="847c2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="847c2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="847c2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="847c2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="847c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="847c2-124">-DefaultProfile</span></span>
<span data-ttu-id="847c2-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="847c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="847c2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="847c2-126">CommonParameters</span></span>
<span data-ttu-id="847c2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="847c2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="847c2-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="847c2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="847c2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="847c2-129">INPUTS</span></span>

### <span data-ttu-id="847c2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="847c2-130">System.String</span></span>

## <span data-ttu-id="847c2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="847c2-131">OUTPUTS</span></span>

### <span data-ttu-id="847c2-132">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="847c2-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="847c2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="847c2-133">NOTES</span></span>

## <span data-ttu-id="847c2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="847c2-134">RELATED LINKS</span></span>

[<span data-ttu-id="847c2-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="847c2-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="847c2-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="847c2-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="847c2-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="847c2-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
