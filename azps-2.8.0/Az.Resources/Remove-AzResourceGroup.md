---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 7878932b0e7a2aad6e171c39e546ad86b2ea0a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932542"
---
# <span data-ttu-id="72528-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72528-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="72528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72528-102">SYNOPSIS</span></span>
<span data-ttu-id="72528-103">Kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72528-103">Removes a resource group.</span></span>

## <span data-ttu-id="72528-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72528-104">SYNTAX</span></span>

### <span data-ttu-id="72528-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72528-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72528-106">Removebyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="72528-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72528-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72528-107">DESCRIPTION</span></span>
<span data-ttu-id="72528-108">**Remove-AzResourceGroup** cmdlet 'i, bir Azure kaynak grubunu ve kaynaklarını geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72528-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="72528-109">Kaynak grubundan çıkmak için Remove-AzResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72528-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="72528-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72528-110">EXAMPLES</span></span>

### <span data-ttu-id="72528-111">Örnek 1: kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="72528-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="72528-112">Bu komut, ContosoRG01 kaynak grubunu abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="72528-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="72528-113">Cmdlet sizden onay ister ve çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="72528-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="72528-114">Örnek 2: onaysız kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="72528-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="72528-115">Bu komut, ContosoRG01 kaynak grubunu almak için Get-AzResourceGroup cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak bunu **kaldırmak için-AzResourceGroup** 'ı geçirir.</span><span class="sxs-lookup"><span data-stu-id="72528-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="72528-116">*Ayrıntılı* ortak parametre işlemle ilgili durum bilgilerini alır ve *Force* parametresi onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="72528-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="72528-117">Örnek 3: tüm kaynak gruplarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="72528-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="72528-118">Bu komut **Get-azresourcegroup** cmdlet 'ini kullanarak tüm kaynak gruplarını alır ve ardından bunları ardışık düzen Işlecini kullanarak **Remove-azresourcegroup** öğesine geçirir.</span><span class="sxs-lookup"><span data-stu-id="72528-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="72528-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72528-119">PARAMETERS</span></span>

### <span data-ttu-id="72528-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="72528-120">-ApiVersion</span></span>
<span data-ttu-id="72528-121">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="72528-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="72528-122">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72528-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72528-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="72528-123">-AsJob</span></span>
<span data-ttu-id="72528-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="72528-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="72528-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72528-125">-DefaultProfile</span></span>
<span data-ttu-id="72528-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72528-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72528-127">-Force</span><span class="sxs-lookup"><span data-stu-id="72528-127">-Force</span></span>
<span data-ttu-id="72528-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="72528-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="72528-129">-ID</span><span class="sxs-lookup"><span data-stu-id="72528-129">-Id</span></span>
<span data-ttu-id="72528-130">Kaldırılacak kaynak grubu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72528-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="72528-131">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="72528-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72528-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="72528-132">-Name</span></span>
<span data-ttu-id="72528-133">Kaldırılacak kaynak gruplarının adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72528-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="72528-134">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="72528-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72528-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="72528-135">-Pre</span></span>
<span data-ttu-id="72528-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="72528-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="72528-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="72528-137">-Confirm</span></span>
<span data-ttu-id="72528-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72528-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72528-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72528-139">-WhatIf</span></span>
<span data-ttu-id="72528-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72528-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72528-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72528-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72528-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72528-142">CommonParameters</span></span>
<span data-ttu-id="72528-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72528-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72528-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72528-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72528-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72528-145">INPUTS</span></span>

### <span data-ttu-id="72528-146">System. String</span><span class="sxs-lookup"><span data-stu-id="72528-146">System.String</span></span>

## <span data-ttu-id="72528-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72528-147">OUTPUTS</span></span>

### <span data-ttu-id="72528-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72528-148">System.Boolean</span></span>

## <span data-ttu-id="72528-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72528-149">NOTES</span></span>

## <span data-ttu-id="72528-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72528-150">RELATED LINKS</span></span>

[<span data-ttu-id="72528-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72528-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="72528-152">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72528-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="72528-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72528-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


