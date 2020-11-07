---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764449"
---
# <span data-ttu-id="fc872-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="fc872-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="fc872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc872-102">SYNOPSIS</span></span>
<span data-ttu-id="fc872-103">Silinmiş Anahtar Kasası 'nı etkin bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fc872-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc872-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc872-104">SYNTAX</span></span>

### <span data-ttu-id="fc872-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc872-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc872-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fc872-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc872-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc872-107">DESCRIPTION</span></span>
<span data-ttu-id="fc872-108">**Undo-Azurermkeyvaultkaldırmada** cmdlet 'i önceden silinmiş bir Anahtar Kasası kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fc872-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="fc872-109">Kurtarılan kasa kurtarma sonrasında etkin olur</span><span class="sxs-lookup"><span data-stu-id="fc872-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="fc872-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc872-110">EXAMPLES</span></span>

### <span data-ttu-id="fc872-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc872-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="fc872-112">Bu komut, daha önce eastus2 bölgesinden ve ' MyResourceGroup ' kaynak grubundan silinen Anahtar Kasası 'nı etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="fc872-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="fc872-113">Ayrıca etiketleri yeni etiketle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="fc872-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="fc872-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc872-114">PARAMETERS</span></span>

### <span data-ttu-id="fc872-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc872-115">-DefaultProfile</span></span>
<span data-ttu-id="fc872-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc872-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc872-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc872-117">-InputObject</span></span>
<span data-ttu-id="fc872-118">Silinmiş kasa nesnesi</span><span class="sxs-lookup"><span data-stu-id="fc872-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc872-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="fc872-119">-Location</span></span>
<span data-ttu-id="fc872-120">Silinmiş kasa özgün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc872-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc872-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc872-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc872-122">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc872-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="fc872-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fc872-123">-Tag</span></span>
<span data-ttu-id="fc872-124">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fc872-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fc872-125">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fc872-125">For example:</span></span>

<span data-ttu-id="fc872-126">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fc872-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fc872-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fc872-127">-VaultName</span></span>
<span data-ttu-id="fc872-128">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="fc872-128">Vault name.</span></span>
<span data-ttu-id="fc872-129">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc872-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fc872-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc872-130">-Confirm</span></span>
<span data-ttu-id="fc872-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc872-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc872-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc872-132">-WhatIf</span></span>
<span data-ttu-id="fc872-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc872-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc872-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc872-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc872-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc872-135">CommonParameters</span></span>
<span data-ttu-id="fc872-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc872-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc872-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc872-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc872-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc872-138">INPUTS</span></span>

### <span data-ttu-id="fc872-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fc872-139">System.String</span></span>
<span data-ttu-id="fc872-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc872-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc872-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc872-141">OUTPUTS</span></span>

### <span data-ttu-id="fc872-142">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="fc872-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fc872-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc872-143">NOTES</span></span>

## <span data-ttu-id="fc872-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc872-144">RELATED LINKS</span></span>

[<span data-ttu-id="fc872-145">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fc872-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="fc872-146">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fc872-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="fc872-147">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fc872-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
