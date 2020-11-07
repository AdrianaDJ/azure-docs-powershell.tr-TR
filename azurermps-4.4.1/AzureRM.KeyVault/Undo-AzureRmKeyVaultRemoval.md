---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 57fdddfea449bbde18762afaed0c576c2b4d1db3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763721"
---
# <span data-ttu-id="2d2fc-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="2d2fc-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="2d2fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2fc-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2fc-103">Silinmiş Anahtar Kasası 'nı etkin bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d2fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d2fc-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2fc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d2fc-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2fc-106">**Undo-Azurermkeyvaultkaldırmada** cmdlet 'i önceden silinmiş bir Anahtar Kasası kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="2d2fc-107">Kurtarılan kasa kurtarma sonrasında etkin olur</span><span class="sxs-lookup"><span data-stu-id="2d2fc-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="2d2fc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d2fc-108">EXAMPLES</span></span>

### <span data-ttu-id="2d2fc-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2d2fc-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="2d2fc-110">Bu komut, daha önce eastus2 bölgesinden ve ' MyResourceGroup ' kaynak grubundan silinen Anahtar Kasası 'nı etkin ve kullanılabilir bir durumda kurtarır.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="2d2fc-111">Ayrıca etiketleri yeni etiketle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="2d2fc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d2fc-112">PARAMETERS</span></span>

### <span data-ttu-id="2d2fc-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="2d2fc-113">-Location</span></span>
<span data-ttu-id="2d2fc-114">Silinmiş kasa özgün Azure bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-114">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2fc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2fc-115">-ResourceGroupName</span></span>
<span data-ttu-id="2d2fc-116">Anahtar Kasası oluşturulacak varolan bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-116">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2fc-117">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2d2fc-117">-Tag</span></span>
<span data-ttu-id="2d2fc-118">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2d2fc-119">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2d2fc-119">For example:</span></span>

<span data-ttu-id="2d2fc-120">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2d2fc-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d2fc-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2d2fc-121">-VaultName</span></span>
<span data-ttu-id="2d2fc-122">Kasa adı.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-122">Vault name.</span></span>
<span data-ttu-id="2d2fc-123">Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-123">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2d2fc-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d2fc-124">-Confirm</span></span>
<span data-ttu-id="2d2fc-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2fc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2fc-126">-WhatIf</span></span>
<span data-ttu-id="2d2fc-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d2fc-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2fc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2fc-129">-DefaultProfile</span></span>
<span data-ttu-id="2d2fc-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d2fc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2fc-131">CommonParameters</span></span>
<span data-ttu-id="2d2fc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d2fc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2fc-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2fc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2fc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d2fc-134">INPUTS</span></span>

### <span data-ttu-id="2d2fc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2fc-135">System.String</span></span>
<span data-ttu-id="2d2fc-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d2fc-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d2fc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d2fc-137">OUTPUTS</span></span>

### <span data-ttu-id="2d2fc-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskasa</span><span class="sxs-lookup"><span data-stu-id="2d2fc-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="2d2fc-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d2fc-139">NOTES</span></span>

## <span data-ttu-id="2d2fc-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d2fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="2d2fc-141">Remove-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2d2fc-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="2d2fc-142">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2d2fc-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="2d2fc-143">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="2d2fc-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
