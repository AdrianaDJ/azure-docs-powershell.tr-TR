---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762855"
---
# <span data-ttu-id="fd191-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd191-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="fd191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd191-102">SYNOPSIS</span></span>
<span data-ttu-id="fd191-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="fd191-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd191-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd191-104">SYNTAX</span></span>

### <span data-ttu-id="fd191-105">ByAvailableVault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd191-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="fd191-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="fd191-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd191-108">Inputobjectbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="fd191-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd191-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd191-109">DESCRIPTION</span></span>
<span data-ttu-id="fd191-110">**Remove-Azurermkeykasası** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="fd191-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="fd191-111">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="fd191-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="fd191-112">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="fd191-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="fd191-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd191-113">EXAMPLES</span></span>

### <span data-ttu-id="fd191-114">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="fd191-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="fd191-115">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd191-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="fd191-116">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="fd191-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="fd191-117">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd191-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="fd191-118">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="fd191-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="fd191-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd191-119">PARAMETERS</span></span>

### <span data-ttu-id="fd191-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="fd191-120">-AsJob</span></span>
<span data-ttu-id="fd191-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fd191-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd191-122">-DefaultProfile</span></span>
<span data-ttu-id="fd191-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd191-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd191-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fd191-124">-Force</span></span>
<span data-ttu-id="fd191-125">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd191-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="fd191-126">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd191-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd191-127">-InputObject</span></span>
<span data-ttu-id="fd191-128">Silinecek anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fd191-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-129">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="fd191-129">-InRemovedState</span></span>
<span data-ttu-id="fd191-130">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fd191-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-131">-Konum</span><span class="sxs-lookup"><span data-stu-id="fd191-131">-Location</span></span>
<span data-ttu-id="fd191-132">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="fd191-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fd191-133">-PassThru</span></span>
<span data-ttu-id="fd191-134">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="fd191-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fd191-135">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd191-135">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd191-136">-ResourceGroupName</span></span>
<span data-ttu-id="fd191-137">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd191-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd191-138">-VaultName</span></span>
<span data-ttu-id="fd191-139">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd191-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd191-140">-Confirm</span></span>
<span data-ttu-id="fd191-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd191-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd191-142">-WhatIf</span></span>
<span data-ttu-id="fd191-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd191-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd191-144">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd191-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd191-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd191-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd191-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd191-146">CommonParameters</span></span>
<span data-ttu-id="fd191-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd191-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd191-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd191-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd191-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd191-149">INPUTS</span></span>

### <span data-ttu-id="fd191-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fd191-150">None</span></span>
<span data-ttu-id="fd191-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fd191-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd191-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd191-152">OUTPUTS</span></span>

### <span data-ttu-id="fd191-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd191-153">System.Boolean</span></span>

## <span data-ttu-id="fd191-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd191-154">NOTES</span></span>

## <span data-ttu-id="fd191-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd191-155">RELATED LINKS</span></span>

[<span data-ttu-id="fd191-156">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fd191-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fd191-157">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="fd191-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
