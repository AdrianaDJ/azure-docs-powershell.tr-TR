---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762842"
---
# <span data-ttu-id="47bc5-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="47bc5-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="47bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="47bc5-103">Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47bc5-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47bc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47bc5-104">SYNTAX</span></span>

### <span data-ttu-id="47bc5-105">Bylockıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47bc5-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bc5-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47bc5-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bc5-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="47bc5-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47bc5-108">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="47bc5-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bc5-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="47bc5-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47bc5-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="47bc5-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47bc5-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="47bc5-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47bc5-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="47bc5-112">DESCRIPTION</span></span>
<span data-ttu-id="47bc5-113">**Remove-AzureRmResourceLock** cmdlet 'ı bir Azure Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47bc5-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="47bc5-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47bc5-114">EXAMPLES</span></span>

### <span data-ttu-id="47bc5-115">Örnek 1: kilidi kaldırma</span><span class="sxs-lookup"><span data-stu-id="47bc5-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="47bc5-116">Bu komut, ContosoSiteLock adındaki kilidi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47bc5-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="47bc5-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47bc5-117">PARAMETERS</span></span>

### <span data-ttu-id="47bc5-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="47bc5-118">-ApiVersion</span></span>
<span data-ttu-id="47bc5-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="47bc5-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="47bc5-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47bc5-121">-DefaultProfile</span></span>
<span data-ttu-id="47bc5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47bc5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47bc5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="47bc5-123">-Force</span></span>
<span data-ttu-id="47bc5-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="47bc5-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47bc5-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="47bc5-125">-InformationAction</span></span>
<span data-ttu-id="47bc5-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="47bc5-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="47bc5-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47bc5-128">'A</span><span class="sxs-lookup"><span data-stu-id="47bc5-128">Continue</span></span>
- <span data-ttu-id="47bc5-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="47bc5-129">Ignore</span></span>
- <span data-ttu-id="47bc5-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="47bc5-130">Inquire</span></span>
- <span data-ttu-id="47bc5-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="47bc5-131">SilentlyContinue</span></span>
- <span data-ttu-id="47bc5-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="47bc5-132">Stop</span></span>
- <span data-ttu-id="47bc5-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="47bc5-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="47bc5-134">-InformationVariable</span></span>
<span data-ttu-id="47bc5-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="47bc5-136">-LockId</span></span>
<span data-ttu-id="47bc5-137">Bu cmdlet 'in kaldırıldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="47bc5-138">-LockName</span></span>
<span data-ttu-id="47bc5-139">Bu cmdlet 'in kaldırıldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="47bc5-140">-Pre</span></span>
<span data-ttu-id="47bc5-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="47bc5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47bc5-142">-ResourceGroupName</span></span>
<span data-ttu-id="47bc5-143">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47bc5-144">-ResourceName</span></span>
<span data-ttu-id="47bc5-145">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="47bc5-146">Örneğin, bir veritabanı belirtmek için aşağıdaki biçimi kullanın:</span><span class="sxs-lookup"><span data-stu-id="47bc5-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="47bc5-147">Sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="47bc5-147">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="47bc5-148">-ResourceType</span></span>
<span data-ttu-id="47bc5-149">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-149">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-150">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="47bc5-150">-Scope</span></span>
<span data-ttu-id="47bc5-151">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-151">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="47bc5-152">-TenantLevel</span></span>
<span data-ttu-id="47bc5-153">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-153">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47bc5-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="47bc5-154">-Confirm</span></span>
<span data-ttu-id="47bc5-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47bc5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47bc5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47bc5-156">-WhatIf</span></span>
<span data-ttu-id="47bc5-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47bc5-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47bc5-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47bc5-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47bc5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47bc5-159">CommonParameters</span></span>
<span data-ttu-id="47bc5-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47bc5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47bc5-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47bc5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47bc5-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47bc5-162">INPUTS</span></span>

### <span data-ttu-id="47bc5-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47bc5-163">None</span></span>
<span data-ttu-id="47bc5-164">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="47bc5-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47bc5-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47bc5-165">OUTPUTS</span></span>

### <span data-ttu-id="47bc5-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="47bc5-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="47bc5-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47bc5-167">NOTES</span></span>

## <span data-ttu-id="47bc5-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47bc5-168">RELATED LINKS</span></span>

[<span data-ttu-id="47bc5-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="47bc5-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="47bc5-170">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="47bc5-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="47bc5-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="47bc5-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


