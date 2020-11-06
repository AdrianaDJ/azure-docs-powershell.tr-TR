---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: c91bc951ef06f2e591893f0959120cac3700b070
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590225"
---
# <span data-ttu-id="61f3e-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="61f3e-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="61f3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="61f3e-103">Anahtar Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="61f3e-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61f3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61f3e-104">SYNTAX</span></span>

### <span data-ttu-id="61f3e-105">ByAvailableVault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61f3e-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f3e-106">Bydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="61f3e-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f3e-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="61f3e-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f3e-108">Inputobjectbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="61f3e-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f3e-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="61f3e-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61f3e-110">Resourceıdbydeletedkasası</span><span class="sxs-lookup"><span data-stu-id="61f3e-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f3e-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="61f3e-111">DESCRIPTION</span></span>
<span data-ttu-id="61f3e-112">**Remove-Azurermkeykasası** cmdlet 'i, belirtilen anahtar kasası siler.</span><span class="sxs-lookup"><span data-stu-id="61f3e-112">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="61f3e-113">Bu örnekte yer alan tüm anahtarları ve gizlilikleri de siler.</span><span class="sxs-lookup"><span data-stu-id="61f3e-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="61f3e-114">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="61f3e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61f3e-115">EXAMPLES</span></span>

### <span data-ttu-id="61f3e-116">Örnek 1: Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="61f3e-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="61f3e-117">Bu komut, Contoso03Vault adındaki Anahtar Kasası 'nı geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61f3e-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="61f3e-118">Örnek 2: belirtilen kaynak grubundan bir Anahtar Kasası kaldırma</span><span class="sxs-lookup"><span data-stu-id="61f3e-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="61f3e-119">Bu komut, adlandırılmış kaynak grubundan Contoso03Vault adındaki Anahtar Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61f3e-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="61f3e-120">Kaynak grubu adını belirtmezseniz cmdlet, geçerli aboneliğinizde silinecek adlandırılmış Anahtar Kasası arar.</span><span class="sxs-lookup"><span data-stu-id="61f3e-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="61f3e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61f3e-121">PARAMETERS</span></span>

### <span data-ttu-id="61f3e-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="61f3e-122">-AsJob</span></span>
<span data-ttu-id="61f3e-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="61f3e-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61f3e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f3e-124">-DefaultProfile</span></span>
<span data-ttu-id="61f3e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="61f3e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61f3e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="61f3e-126">-Force</span></span>
<span data-ttu-id="61f3e-127">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="61f3e-128">Varsayılan olarak, bu cmdlet Anahtar Kasası silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61f3e-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="61f3e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61f3e-129">-InputObject</span></span>
<span data-ttu-id="61f3e-130">Silinecek anahtar kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="61f3e-130">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-131">-Inremovevseçstate</span><span class="sxs-lookup"><span data-stu-id="61f3e-131">-InRemovedState</span></span>
<span data-ttu-id="61f3e-132">Önceden silinmiş kasayı kalıcı olarak kaldırın.</span><span class="sxs-lookup"><span data-stu-id="61f3e-132">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-133">-Konum</span><span class="sxs-lookup"><span data-stu-id="61f3e-133">-Location</span></span>
<span data-ttu-id="61f3e-134">Silinmiş kasanın konumu.</span><span class="sxs-lookup"><span data-stu-id="61f3e-134">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="61f3e-135">-PassThru</span></span>
<span data-ttu-id="61f3e-136">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="61f3e-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="61f3e-137">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="61f3e-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="61f3e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f3e-138">-ResourceGroupName</span></span>
<span data-ttu-id="61f3e-139">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-139">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="61f3e-140">-ResourceId</span></span>
<span data-ttu-id="61f3e-141">Tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="61f3e-141">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="61f3e-142">-VaultName</span></span>
<span data-ttu-id="61f3e-143">Kaldırılacak anahtar kasası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f3e-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="61f3e-144">-Confirm</span></span>
<span data-ttu-id="61f3e-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61f3e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f3e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f3e-146">-WhatIf</span></span>
<span data-ttu-id="61f3e-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f3e-148">Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f3e-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f3e-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61f3e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f3e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f3e-150">CommonParameters</span></span>
<span data-ttu-id="61f3e-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61f3e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f3e-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61f3e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f3e-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61f3e-153">INPUTS</span></span>

### <span data-ttu-id="61f3e-154">Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa</span><span class="sxs-lookup"><span data-stu-id="61f3e-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="61f3e-155">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="61f3e-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="61f3e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="61f3e-156">System.String</span></span>

## <span data-ttu-id="61f3e-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61f3e-157">OUTPUTS</span></span>

### <span data-ttu-id="61f3e-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="61f3e-158">System.Boolean</span></span>

## <span data-ttu-id="61f3e-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61f3e-159">NOTES</span></span>

## <span data-ttu-id="61f3e-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61f3e-160">RELATED LINKS</span></span>

[<span data-ttu-id="61f3e-161">Get-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="61f3e-161">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="61f3e-162">Yeni-Azurermkeykasası</span><span class="sxs-lookup"><span data-stu-id="61f3e-162">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
