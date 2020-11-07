---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936662"
---
# <span data-ttu-id="523b7-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="523b7-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="523b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="523b7-102">SYNOPSIS</span></span>
<span data-ttu-id="523b7-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="523b7-103">Deletes a key vault.</span></span>

## <span data-ttu-id="523b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="523b7-104">SYNTAX</span></span>

### <span data-ttu-id="523b7-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="523b7-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="523b7-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="523b7-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="523b7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="523b7-107">DESCRIPTION</span></span>
<span data-ttu-id="523b7-108">**Remove-Azkeykasa** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="523b7-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="523b7-109">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="523b7-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="523b7-110">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="523b7-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="523b7-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="523b7-111">EXAMPLES</span></span>

### <span data-ttu-id="523b7-112">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="523b7-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="523b7-113">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="523b7-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="523b7-114">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="523b7-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="523b7-115">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="523b7-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="523b7-116">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="523b7-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="523b7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="523b7-117">PARAMETERS</span></span>

### <span data-ttu-id="523b7-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="523b7-118">-AsJob</span></span>
<span data-ttu-id="523b7-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="523b7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="523b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523b7-120">-DefaultProfile</span></span>
<span data-ttu-id="523b7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="523b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="523b7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="523b7-122">-Force</span></span>
<span data-ttu-id="523b7-123">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="523b7-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="523b7-124">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="523b7-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="523b7-125">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="523b7-125">-InRemovedState</span></span>
<span data-ttu-id="523b7-126">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="523b7-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523b7-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="523b7-127">-Location</span></span>
<span data-ttu-id="523b7-128">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="523b7-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="523b7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523b7-129">-ResourceGroupName</span></span>
<span data-ttu-id="523b7-130">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="523b7-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="523b7-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="523b7-131">-VaultName</span></span>
<span data-ttu-id="523b7-132">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="523b7-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="523b7-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="523b7-133">-Confirm</span></span>
<span data-ttu-id="523b7-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="523b7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523b7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523b7-135">-WhatIf</span></span>
<span data-ttu-id="523b7-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="523b7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523b7-137">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="523b7-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523b7-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="523b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523b7-139">CommonParameters</span></span>
<span data-ttu-id="523b7-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="523b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523b7-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523b7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523b7-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="523b7-142">INPUTS</span></span>

### <span data-ttu-id="523b7-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="523b7-143">None</span></span>
<span data-ttu-id="523b7-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="523b7-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="523b7-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="523b7-145">OUTPUTS</span></span>

## <span data-ttu-id="523b7-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="523b7-146">NOTES</span></span>

## <span data-ttu-id="523b7-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="523b7-147">RELATED LINKS</span></span>

[<span data-ttu-id="523b7-148">Get-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="523b7-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="523b7-149">Yeni-Aztuş Kasası</span><span class="sxs-lookup"><span data-stu-id="523b7-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
