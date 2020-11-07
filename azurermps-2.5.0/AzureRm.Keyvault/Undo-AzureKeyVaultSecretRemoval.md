---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
ms.openlocfilehash: a025dc40a666f643a3e7e232a22451e73f3e60bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939366"
---
# <span data-ttu-id="7eed5-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="7eed5-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="7eed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eed5-102">SYNOPSIS</span></span>
<span data-ttu-id="7eed5-103">Anahtar kasasındaki silinmiş bir parolayı etkin bir duruma kurtarır.</span><span class="sxs-lookup"><span data-stu-id="7eed5-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eed5-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eed5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eed5-105">DESCRIPTION</span></span>
<span data-ttu-id="7eed5-106">**Undo-AzureKeyVaultSecretRemoval** cmdlet 'i önceden silinmiş bir parolayı kurtarır.</span><span class="sxs-lookup"><span data-stu-id="7eed5-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="7eed5-107">Kurtarılan parola etkin olur ve tüm normal gizli işlemler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7eed5-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="7eed5-108">Bu işlemi gerçekleştirebilmek için arayan ' Recover ' iznine sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7eed5-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="7eed5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eed5-109">EXAMPLES</span></span>

### <span data-ttu-id="7eed5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7eed5-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="7eed5-111">Bu komut, önceden silinen gizli ' MySecret ' parolasını etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="7eed5-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="7eed5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eed5-112">PARAMETERS</span></span>

### <span data-ttu-id="7eed5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eed5-113">-DefaultProfile</span></span>
<span data-ttu-id="7eed5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7eed5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7eed5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7eed5-115">-Name</span></span>
<span data-ttu-id="7eed5-116">Gizli ad.</span><span class="sxs-lookup"><span data-stu-id="7eed5-116">Secret name.</span></span>
<span data-ttu-id="7eed5-117">Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7eed5-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="7eed5-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7eed5-118">-VaultName</span></span>
<span data-ttu-id="7eed5-119">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="7eed5-119">Vault name.</span></span>
<span data-ttu-id="7eed5-120">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7eed5-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7eed5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="7eed5-121">-Confirm</span></span>
<span data-ttu-id="7eed5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7eed5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eed5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eed5-123">-WhatIf</span></span>
<span data-ttu-id="7eed5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7eed5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eed5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7eed5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eed5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eed5-126">CommonParameters</span></span>
<span data-ttu-id="7eed5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eed5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eed5-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eed5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eed5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eed5-129">INPUTS</span></span>

### <span data-ttu-id="7eed5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7eed5-130">System.String</span></span>

## <span data-ttu-id="7eed5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eed5-131">OUTPUTS</span></span>

### <span data-ttu-id="7eed5-132">Microsoft. Azure. Commands. Keykasa. modeller. Secret</span><span class="sxs-lookup"><span data-stu-id="7eed5-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="7eed5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eed5-133">NOTES</span></span>

## <span data-ttu-id="7eed5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eed5-134">RELATED LINKS</span></span>

[<span data-ttu-id="7eed5-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7eed5-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)



[<span data-ttu-id="7eed5-136">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7eed5-136">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
