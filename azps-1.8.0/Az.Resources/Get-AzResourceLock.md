---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759417"
---
# <span data-ttu-id="97269-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97269-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="97269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97269-102">SYNOPSIS</span></span>
<span data-ttu-id="97269-103">Kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-103">Gets a resource lock.</span></span>

## <span data-ttu-id="97269-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97269-104">SYNTAX</span></span>

### <span data-ttu-id="97269-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97269-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97269-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="97269-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97269-107">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="97269-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97269-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="97269-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97269-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="97269-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97269-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="97269-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97269-111">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="97269-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97269-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="97269-112">DESCRIPTION</span></span>
<span data-ttu-id="97269-113">**Get-AzResourceLock** cmdlet 'i Azure kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="97269-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97269-114">EXAMPLES</span></span>

### <span data-ttu-id="97269-115">Örnek 1: kilit alma</span><span class="sxs-lookup"><span data-stu-id="97269-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="97269-116">Bu komut, ContosoSiteLock adındaki kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="97269-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97269-117">PARAMETERS</span></span>

### <span data-ttu-id="97269-118">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="97269-118">-ApiVersion</span></span>
<span data-ttu-id="97269-119">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="97269-120">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="97269-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="97269-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="97269-121">-AtScope</span></span>
<span data-ttu-id="97269-122">Bu cmdlet 'in belirtilen kapsamda veya yukarısındaki tüm kilitleri döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="97269-123">Bu parametreyi belirtmezseniz, cmdlet, kapsamın üstünde veya altında tüm kilitleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="97269-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="97269-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97269-124">-DefaultProfile</span></span>
<span data-ttu-id="97269-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="97269-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97269-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="97269-126">-LockId</span></span>
<span data-ttu-id="97269-127">Bu cmdlet 'in aldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="97269-128">-LockName</span><span class="sxs-lookup"><span data-stu-id="97269-128">-LockName</span></span>
<span data-ttu-id="97269-129">Bu cmdlet 'in aldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-129">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97269-130">-Pre-</span><span class="sxs-lookup"><span data-stu-id="97269-130">-Pre</span></span>
<span data-ttu-id="97269-131">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="97269-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="97269-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97269-132">-ResourceGroupName</span></span>
<span data-ttu-id="97269-133">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="97269-134">Bu cmdlet bu kaynak grubunun kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="97269-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="97269-135">-ResourceName</span></span>
<span data-ttu-id="97269-136">Bu kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="97269-137">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="97269-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="97269-138">-ResourceType</span></span>
<span data-ttu-id="97269-139">Bu kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="97269-140">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="97269-141">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="97269-141">-Scope</span></span>
<span data-ttu-id="97269-142">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="97269-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="97269-143">Cmdlet bu kapsamın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="97269-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="97269-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="97269-144">-TenantLevel</span></span>
<span data-ttu-id="97269-145">Bu cmdlet 'in kiracı düzeyinde çalışır olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="97269-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="97269-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97269-146">CommonParameters</span></span>
<span data-ttu-id="97269-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97269-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97269-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97269-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97269-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97269-149">INPUTS</span></span>

### <span data-ttu-id="97269-150">System. String</span><span class="sxs-lookup"><span data-stu-id="97269-150">System.String</span></span>

## <span data-ttu-id="97269-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97269-151">OUTPUTS</span></span>

### <span data-ttu-id="97269-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="97269-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="97269-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97269-153">NOTES</span></span>

## <span data-ttu-id="97269-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97269-154">RELATED LINKS</span></span>

[<span data-ttu-id="97269-155">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97269-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="97269-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97269-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="97269-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="97269-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


