---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
ms.openlocfilehash: a557676d35eb167438f29c36a729ee652a45d591
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939365"
---
# <span data-ttu-id="455fb-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="455fb-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="455fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="455fb-102">SYNOPSIS</span></span>
<span data-ttu-id="455fb-103">Silinmiş Anahtar Kasası 'nı etkin bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="455fb-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="455fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="455fb-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="455fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="455fb-105">DESCRIPTION</span></span>
<span data-ttu-id="455fb-106">**Undo-Azurermkeyvaultkaldırmada** cmdlet 'i önceden silinmiş bir Anahtar Kasası kurtarır.</span><span class="sxs-lookup"><span data-stu-id="455fb-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="455fb-107">Kurtarılan kasa kurtarma sonrasında etkin olur</span><span class="sxs-lookup"><span data-stu-id="455fb-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="455fb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="455fb-108">EXAMPLES</span></span>

### <span data-ttu-id="455fb-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="455fb-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="455fb-110">Bu komut, daha önce eastus2 bölgesinden ve ' MyResourceGroup ' kaynak grubundan silinen Anahtar Kasası 'nı etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="455fb-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="455fb-111">Ayrıca etiketleri yeni etiketle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="455fb-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="455fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="455fb-112">PARAMETERS</span></span>

### <span data-ttu-id="455fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="455fb-113">-DefaultProfile</span></span>
<span data-ttu-id="455fb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="455fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="455fb-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="455fb-115">-Location</span></span>
<span data-ttu-id="455fb-116">Silinmiş kasa özgün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="455fb-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="455fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="455fb-118">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="455fb-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455fb-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="455fb-119">-Tag</span></span>
<span data-ttu-id="455fb-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="455fb-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="455fb-121">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="455fb-121">For example:</span></span>

<span data-ttu-id="455fb-122">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="455fb-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="455fb-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="455fb-123">-VaultName</span></span>
<span data-ttu-id="455fb-124">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="455fb-124">Vault name.</span></span>
<span data-ttu-id="455fb-125">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="455fb-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="455fb-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="455fb-126">-Confirm</span></span>
<span data-ttu-id="455fb-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="455fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="455fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="455fb-128">-WhatIf</span></span>
<span data-ttu-id="455fb-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="455fb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="455fb-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="455fb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="455fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="455fb-131">CommonParameters</span></span>
<span data-ttu-id="455fb-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="455fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="455fb-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="455fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="455fb-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="455fb-134">INPUTS</span></span>

### <span data-ttu-id="455fb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="455fb-135">System.String</span></span>
<span data-ttu-id="455fb-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="455fb-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="455fb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="455fb-137">OUTPUTS</span></span>

### <span data-ttu-id="455fb-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="455fb-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="455fb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="455fb-139">NOTES</span></span>

## <span data-ttu-id="455fb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="455fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="455fb-141">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="455fb-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="455fb-142">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="455fb-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="455fb-143">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="455fb-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
