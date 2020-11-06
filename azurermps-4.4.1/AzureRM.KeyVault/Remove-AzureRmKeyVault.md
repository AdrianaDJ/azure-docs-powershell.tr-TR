---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593548"
---
# <span data-ttu-id="6d57d-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="6d57d-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="6d57d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d57d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d57d-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="6d57d-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d57d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d57d-104">SYNTAX</span></span>

### <span data-ttu-id="6d57d-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="6d57d-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d57d-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="6d57d-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d57d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d57d-107">DESCRIPTION</span></span>
<span data-ttu-id="6d57d-108">**Remove-Azurermkeykasası** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="6d57d-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="6d57d-109">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="6d57d-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="6d57d-110">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="6d57d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d57d-111">EXAMPLES</span></span>

### <span data-ttu-id="6d57d-112">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="6d57d-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="6d57d-113">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d57d-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="6d57d-114">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="6d57d-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="6d57d-115">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d57d-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="6d57d-116">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="6d57d-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="6d57d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d57d-117">PARAMETERS</span></span>

### <span data-ttu-id="6d57d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6d57d-118">-Force</span></span>
<span data-ttu-id="6d57d-119">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="6d57d-120">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d57d-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-121">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="6d57d-121">-InRemovedState</span></span>
<span data-ttu-id="6d57d-122">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6d57d-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="6d57d-123">-Location</span></span>
<span data-ttu-id="6d57d-124">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="6d57d-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d57d-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d57d-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6d57d-127">-VaultName</span></span>
<span data-ttu-id="6d57d-128">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-128">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="6d57d-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d57d-129">-Confirm</span></span>
<span data-ttu-id="6d57d-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d57d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d57d-131">-WhatIf</span></span>
<span data-ttu-id="6d57d-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d57d-133">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d57d-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d57d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d57d-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d57d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d57d-135">-DefaultProfile</span></span>
<span data-ttu-id="6d57d-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d57d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d57d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d57d-137">CommonParameters</span></span>
<span data-ttu-id="6d57d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d57d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d57d-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d57d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d57d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d57d-140">INPUTS</span></span>

## <span data-ttu-id="6d57d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d57d-141">OUTPUTS</span></span>

## <span data-ttu-id="6d57d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d57d-142">NOTES</span></span>

## <span data-ttu-id="6d57d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d57d-143">RELATED LINKS</span></span>

[<span data-ttu-id="6d57d-144">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="6d57d-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="6d57d-145">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="6d57d-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
