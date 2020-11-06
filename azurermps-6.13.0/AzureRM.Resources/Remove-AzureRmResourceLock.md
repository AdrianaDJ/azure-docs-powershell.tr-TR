---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c719eee4800b404d691d478a989fdfdb3e7be09d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593905"
---
# <span data-ttu-id="00326-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="00326-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="00326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00326-102">SYNOPSIS</span></span>
<span data-ttu-id="00326-103">Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00326-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00326-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00326-104">SYNTAX</span></span>

### <span data-ttu-id="00326-105">Bylockıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00326-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00326-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00326-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00326-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="00326-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00326-108">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="00326-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00326-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="00326-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00326-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="00326-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00326-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="00326-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00326-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="00326-112">DESCRIPTION</span></span>
<span data-ttu-id="00326-113">**Remove-AzureRmResourceLock** cmdlet 'ı bir Azure Kaynak kilidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00326-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="00326-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00326-114">EXAMPLES</span></span>

### <span data-ttu-id="00326-115">Örnek 1: kilidi kaldırma</span><span class="sxs-lookup"><span data-stu-id="00326-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="00326-116">Bu komut, ContosoSiteLock adındaki kilidi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00326-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="00326-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00326-117">PARAMETERS</span></span>

### <span data-ttu-id="00326-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="00326-118">-ApiVersion</span></span>
<span data-ttu-id="00326-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="00326-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="00326-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="00326-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00326-121">-DefaultProfile</span></span>
<span data-ttu-id="00326-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="00326-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00326-123">-Force</span><span class="sxs-lookup"><span data-stu-id="00326-123">-Force</span></span>
<span data-ttu-id="00326-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="00326-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00326-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="00326-125">-InformationAction</span></span>
<span data-ttu-id="00326-126">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="00326-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="00326-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="00326-128">'A</span><span class="sxs-lookup"><span data-stu-id="00326-128">Continue</span></span>
- <span data-ttu-id="00326-129">Manıza</span><span class="sxs-lookup"><span data-stu-id="00326-129">Ignore</span></span>
- <span data-ttu-id="00326-130">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="00326-130">Inquire</span></span>
- <span data-ttu-id="00326-131">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="00326-131">SilentlyContinue</span></span>
- <span data-ttu-id="00326-132">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="00326-132">Stop</span></span>
- <span data-ttu-id="00326-133">Biliriz</span><span class="sxs-lookup"><span data-stu-id="00326-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00326-134">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="00326-134">-InformationVariable</span></span>
<span data-ttu-id="00326-135">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00326-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="00326-136">-LockId</span></span>
<span data-ttu-id="00326-137">Bu cmdlet 'in kaldırıldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-138">-LockName</span><span class="sxs-lookup"><span data-stu-id="00326-138">-LockName</span></span>
<span data-ttu-id="00326-139">Bu cmdlet 'in kaldırıldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-140">-Pre-</span><span class="sxs-lookup"><span data-stu-id="00326-140">-Pre</span></span>
<span data-ttu-id="00326-141">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="00326-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="00326-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00326-142">-ResourceGroupName</span></span>
<span data-ttu-id="00326-143">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="00326-144">-ResourceName</span></span>
<span data-ttu-id="00326-145">Kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="00326-146">Örneğin, bir veritabanı belirtmek için şu biçimi kullanın: sunucu `/` veritabanı</span><span class="sxs-lookup"><span data-stu-id="00326-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="00326-147">-ResourceType</span></span>
<span data-ttu-id="00326-148">Kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-148">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-149">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="00326-149">-Scope</span></span>
<span data-ttu-id="00326-150">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00326-150">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00326-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="00326-151">-TenantLevel</span></span>
<span data-ttu-id="00326-152">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="00326-152">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00326-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="00326-153">-Confirm</span></span>
<span data-ttu-id="00326-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00326-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00326-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00326-155">-WhatIf</span></span>
<span data-ttu-id="00326-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00326-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00326-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00326-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00326-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00326-158">CommonParameters</span></span>
<span data-ttu-id="00326-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00326-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00326-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00326-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00326-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00326-161">INPUTS</span></span>

## <span data-ttu-id="00326-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00326-162">OUTPUTS</span></span>

## <span data-ttu-id="00326-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00326-163">NOTES</span></span>

## <span data-ttu-id="00326-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00326-164">RELATED LINKS</span></span>

[<span data-ttu-id="00326-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="00326-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="00326-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="00326-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="00326-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="00326-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


