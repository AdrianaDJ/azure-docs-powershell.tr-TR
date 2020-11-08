---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: 232f8de58bb6026a2932631ac2f9e3ed77c71b91
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936339"
---
# <span data-ttu-id="36861-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36861-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="36861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36861-102">SYNOPSIS</span></span>
<span data-ttu-id="36861-103">Kaynak grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36861-103">Removes a resource group.</span></span>

## <span data-ttu-id="36861-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36861-104">SYNTAX</span></span>

### <span data-ttu-id="36861-105">RemoveByResourceGroupName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="36861-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36861-106">Removebyresourcegroupıd</span><span class="sxs-lookup"><span data-stu-id="36861-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36861-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36861-107">DESCRIPTION</span></span>
<span data-ttu-id="36861-108">**Remove-AzResourceGroup** cmdlet 'i, bir Azure kaynak grubunu ve kaynaklarını geçerli abonelikten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36861-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="36861-109">Kaynak grubundan çıkmak için Remove-AzResource cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="36861-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="36861-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36861-110">EXAMPLES</span></span>

### <span data-ttu-id="36861-111">Örnek 1: kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="36861-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="36861-112">Bu komut, ContosoRG01 kaynak grubunu abonelikten çıkarır.</span><span class="sxs-lookup"><span data-stu-id="36861-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="36861-113">Cmdlet sizden onay ister ve çıkış döndürmez.</span><span class="sxs-lookup"><span data-stu-id="36861-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="36861-114">Örnek 2: onaysız kaynak grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="36861-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Verbose -Force
```

<span data-ttu-id="36861-115">Bu komut, ContosoRG01 kaynak grubunu almak için Get-AzResourceGroup cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak bunu **kaldırmak için-AzResourceGroup** 'ı geçirir.</span><span class="sxs-lookup"><span data-stu-id="36861-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="36861-116">*Ayrıntılı* ortak parametre işlemle ilgili durum bilgilerini alır ve *Force* parametresi onay istemini bastırır.</span><span class="sxs-lookup"><span data-stu-id="36861-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="36861-117">Örnek 3: tüm kaynak gruplarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="36861-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="36861-118">Bu komut **Get-azresourcegroup** cmdlet 'ini kullanarak tüm kaynak gruplarını alır ve ardından bunları ardışık düzen Işlecini kullanarak **Remove-azresourcegroup** öğesine geçirir.</span><span class="sxs-lookup"><span data-stu-id="36861-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="36861-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36861-119">PARAMETERS</span></span>

### <span data-ttu-id="36861-120">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="36861-120">-ApiVersion</span></span>
<span data-ttu-id="36861-121">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="36861-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="36861-122">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36861-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="36861-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="36861-123">-AsJob</span></span>
<span data-ttu-id="36861-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="36861-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36861-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36861-125">-DefaultProfile</span></span>
<span data-ttu-id="36861-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="36861-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36861-127">-Force</span><span class="sxs-lookup"><span data-stu-id="36861-127">-Force</span></span>
<span data-ttu-id="36861-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="36861-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36861-129">-ID</span><span class="sxs-lookup"><span data-stu-id="36861-129">-Id</span></span>
<span data-ttu-id="36861-130">Kaldırılacak kaynak grubu KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="36861-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="36861-131">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="36861-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36861-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="36861-132">-Name</span></span>
<span data-ttu-id="36861-133">Kaldırılacak kaynak gruplarının adlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36861-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="36861-134">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="36861-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="36861-135">-Pre-</span><span class="sxs-lookup"><span data-stu-id="36861-135">-Pre</span></span>
<span data-ttu-id="36861-136">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36861-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36861-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="36861-137">-Confirm</span></span>
<span data-ttu-id="36861-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36861-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36861-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36861-139">-WhatIf</span></span>
<span data-ttu-id="36861-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36861-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36861-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36861-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36861-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36861-142">CommonParameters</span></span>
<span data-ttu-id="36861-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36861-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36861-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36861-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36861-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36861-145">INPUTS</span></span>

## <span data-ttu-id="36861-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36861-146">OUTPUTS</span></span>

## <span data-ttu-id="36861-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36861-147">NOTES</span></span>

## <span data-ttu-id="36861-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36861-148">RELATED LINKS</span></span>

[<span data-ttu-id="36861-149">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36861-149">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="36861-150">Yeni-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36861-150">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="36861-151">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36861-151">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)

