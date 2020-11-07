---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: fd2483925e8ab14772a3bf34d4411748583a03c9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935765"
---
# <span data-ttu-id="6def4-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="6def4-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="6def4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6def4-102">SYNOPSIS</span></span>
<span data-ttu-id="6def4-103">Silinmiş Anahtar Kasası 'nı etkin bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6def4-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="6def4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6def4-104">SYNTAX</span></span>

```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6def4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6def4-105">DESCRIPTION</span></span>
<span data-ttu-id="6def4-106">**Undo-Azanahtarvaultkaldýrma** cmdlet 'i önceden silinmiş bir Anahtar Kasası kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6def4-106">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="6def4-107">Kurtarılan kasa kurtarma sonrasında etkin olur</span><span class="sxs-lookup"><span data-stu-id="6def4-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="6def4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6def4-108">EXAMPLES</span></span>

### <span data-ttu-id="6def4-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6def4-109">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="6def4-110">Bu komut, daha önce eastus2 bölgesinden ve ' MyResourceGroup ' kaynak grubundan silinen Anahtar Kasası 'nı etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="6def4-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="6def4-111">Ayrıca etiketleri yeni etiketle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6def4-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="6def4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6def4-112">PARAMETERS</span></span>

### <span data-ttu-id="6def4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6def4-113">-DefaultProfile</span></span>
<span data-ttu-id="6def4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6def4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6def4-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="6def4-115">-Location</span></span>
<span data-ttu-id="6def4-116">Silinmiş kasa özgün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6def4-116">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="6def4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6def4-117">-ResourceGroupName</span></span>
<span data-ttu-id="6def4-118">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6def4-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="6def4-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="6def4-119">-Tag</span></span>
<span data-ttu-id="6def4-120">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="6def4-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6def4-121">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="6def4-121">For example:</span></span>

<span data-ttu-id="6def4-122">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="6def4-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6def4-123">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6def4-123">-VaultName</span></span>
<span data-ttu-id="6def4-124">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="6def4-124">Vault name.</span></span>
<span data-ttu-id="6def4-125">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6def4-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6def4-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="6def4-126">-Confirm</span></span>
<span data-ttu-id="6def4-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6def4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6def4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6def4-128">-WhatIf</span></span>
<span data-ttu-id="6def4-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6def4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6def4-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6def4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6def4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6def4-131">CommonParameters</span></span>
<span data-ttu-id="6def4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6def4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6def4-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6def4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6def4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6def4-134">INPUTS</span></span>

### <span data-ttu-id="6def4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6def4-135">System.String</span></span>
<span data-ttu-id="6def4-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6def4-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6def4-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6def4-137">OUTPUTS</span></span>

### <span data-ttu-id="6def4-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="6def4-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="6def4-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6def4-139">NOTES</span></span>

## <span data-ttu-id="6def4-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6def4-140">RELATED LINKS</span></span>

[<span data-ttu-id="6def4-141">Remove-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="6def4-141">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="6def4-142">Yeni-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="6def4-142">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="6def4-143">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="6def4-143">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
