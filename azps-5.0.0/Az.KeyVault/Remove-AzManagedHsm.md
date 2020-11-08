---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275294"
---
# <span data-ttu-id="9f33c-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f33c-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="9f33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f33c-102">SYNOPSIS</span></span>
<span data-ttu-id="9f33c-103">Yönetilen HSM 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="9f33c-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="9f33c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f33c-104">SYNTAX</span></span>

### <span data-ttu-id="9f33c-105">RemoveManagedHsmByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f33c-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f33c-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f33c-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f33c-107">Removemanagedhsmbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9f33c-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f33c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f33c-108">DESCRIPTION</span></span>
<span data-ttu-id="9f33c-109">**Remove-AzManagedHsm** cmdlet 'i BELIRTILEN yönetilen HSM 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="9f33c-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="9f33c-110">Bu örnekte yer alan tüm anahtarları da siler.</span><span class="sxs-lookup"><span data-stu-id="9f33c-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="9f33c-111">Bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirtmek için, daha iyi performans için gerekir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="9f33c-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f33c-112">EXAMPLES</span></span>

### <span data-ttu-id="9f33c-113">Örnek 1: yönetilen HSM 'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="9f33c-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="9f33c-114">Bu komut myhsm adındaki yönetilen HSM 'yi geçerli aboneliğinizden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="9f33c-115">Örnek 2: belirtilen kaynak grubundan yönetilen bir HSM 'yi kaldırma</span><span class="sxs-lookup"><span data-stu-id="9f33c-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="9f33c-116">Bu komut, myhsm adlı yönetilen HSM 'yi myrg1 adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9f33c-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="9f33c-117">Kaynak grubu adını belirtmezseniz, cmdlet geçerli aboneliğinizde silmek için adlandırılmış yönetilen HSM 'yi arar.</span><span class="sxs-lookup"><span data-stu-id="9f33c-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="9f33c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f33c-118">PARAMETERS</span></span>

### <span data-ttu-id="9f33c-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="9f33c-119">-AsJob</span></span>
<span data-ttu-id="9f33c-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9f33c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f33c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f33c-121">-DefaultProfile</span></span>
<span data-ttu-id="9f33c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f33c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f33c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9f33c-123">-Force</span></span>
<span data-ttu-id="9f33c-124">Cmdlet 'in sizden onay istemez olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="9f33c-125">Varsayılan olarak, bu cmdlet yönetilen HSM 'yi silmek istediğinizi onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f33c-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="9f33c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f33c-126">-InputObject</span></span>
<span data-ttu-id="9f33c-127">Silinecek yönetilen HSM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9f33c-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f33c-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f33c-128">-Name</span></span>
<span data-ttu-id="9f33c-129">Kaldırılacak olan yönetilen HSM 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f33c-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9f33c-130">-PassThru</span></span>
<span data-ttu-id="9f33c-131">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9f33c-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9f33c-132">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="9f33c-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="9f33c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f33c-133">-ResourceGroupName</span></span>
<span data-ttu-id="9f33c-134">Kaldırılacak Azure yönetilen HSM kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f33c-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f33c-135">-ResourceId</span></span>
<span data-ttu-id="9f33c-136">ManagedHsm kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9f33c-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f33c-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f33c-137">-Confirm</span></span>
<span data-ttu-id="9f33c-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f33c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f33c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f33c-139">-WhatIf</span></span>
<span data-ttu-id="9f33c-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f33c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f33c-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9f33c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f33c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f33c-142">CommonParameters</span></span>
<span data-ttu-id="9f33c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f33c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f33c-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9f33c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f33c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f33c-145">INPUTS</span></span>

### <span data-ttu-id="9f33c-146">Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f33c-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="9f33c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9f33c-147">System.String</span></span>

## <span data-ttu-id="9f33c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f33c-148">OUTPUTS</span></span>

### <span data-ttu-id="9f33c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f33c-149">System.Boolean</span></span>

## <span data-ttu-id="9f33c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f33c-150">NOTES</span></span>

## <span data-ttu-id="9f33c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f33c-151">RELATED LINKS</span></span>

[<span data-ttu-id="9f33c-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f33c-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="9f33c-153">Yeni-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f33c-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="9f33c-154">Güncelleştirme-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="9f33c-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)