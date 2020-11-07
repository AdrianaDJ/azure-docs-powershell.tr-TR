---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936640"
---
# <span data-ttu-id="ee012-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="ee012-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="ee012-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee012-102">SYNOPSIS</span></span>
<span data-ttu-id="ee012-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="ee012-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="ee012-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee012-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee012-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee012-105">DESCRIPTION</span></span>
<span data-ttu-id="ee012-106">**Undo-Azanahtarvaultsecretkaldýrma** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="ee012-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="ee012-107">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ee012-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="ee012-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ee012-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ee012-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee012-109">EXAMPLES</span></span>

### <span data-ttu-id="ee012-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee012-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="ee012-111">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="ee012-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ee012-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee012-112">PARAMETERS</span></span>

### <span data-ttu-id="ee012-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee012-113">-DefaultProfile</span></span>
<span data-ttu-id="ee012-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee012-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee012-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee012-115">-Name</span></span>
<span data-ttu-id="ee012-116">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="ee012-116">Secret name.</span></span>
<span data-ttu-id="ee012-117">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee012-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="ee012-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ee012-118">-VaultName</span></span>
<span data-ttu-id="ee012-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="ee012-119">Vault name.</span></span>
<span data-ttu-id="ee012-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee012-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ee012-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee012-121">-Confirm</span></span>
<span data-ttu-id="ee012-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee012-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee012-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee012-123">-WhatIf</span></span>
<span data-ttu-id="ee012-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee012-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee012-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee012-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee012-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee012-126">CommonParameters</span></span>
<span data-ttu-id="ee012-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee012-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee012-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee012-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee012-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee012-129">INPUTS</span></span>

### <span data-ttu-id="ee012-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ee012-130">System.String</span></span>

## <span data-ttu-id="ee012-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee012-131">OUTPUTS</span></span>

### <span data-ttu-id="ee012-132">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="ee012-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="ee012-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee012-133">NOTES</span></span>

## <span data-ttu-id="ee012-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee012-134">RELATED LINKS</span></span>

[<span data-ttu-id="ee012-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ee012-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="ee012-136">Add-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="ee012-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="ee012-137">Get-Azanahtarvaultsecret</span><span class="sxs-lookup"><span data-stu-id="ee012-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
