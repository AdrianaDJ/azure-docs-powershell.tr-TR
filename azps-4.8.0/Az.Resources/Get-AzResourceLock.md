---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 2dbbb41ce1ad2ee6fc2279e711722090f4f1a6cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267652"
---
# <span data-ttu-id="c765f-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c765f-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="c765f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c765f-102">SYNOPSIS</span></span>
<span data-ttu-id="c765f-103">Kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-103">Gets a resource lock.</span></span>

## <span data-ttu-id="c765f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c765f-104">SYNTAX</span></span>

### <span data-ttu-id="c765f-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c765f-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c765f-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c765f-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c765f-107">Bybelirtildiedscope</span><span class="sxs-lookup"><span data-stu-id="c765f-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c765f-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c765f-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c765f-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c765f-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c765f-110">Bylockıd</span><span class="sxs-lookup"><span data-stu-id="c765f-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c765f-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c765f-111">DESCRIPTION</span></span>
<span data-ttu-id="c765f-112">**Get-AzResourceLock** cmdlet 'i Azure kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="c765f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c765f-113">EXAMPLES</span></span>

### <span data-ttu-id="c765f-114">Örnek 1: kilit alma</span><span class="sxs-lookup"><span data-stu-id="c765f-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="c765f-115">Bu komut, ContosoSiteLock adındaki kaynak kilidini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="c765f-116">Örnek 2: Kaynak Grup düzeyindeki veya üzeri kilitleri alma</span><span class="sxs-lookup"><span data-stu-id="c765f-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="c765f-117">Bu komut, kaynak grubundaki veya abonelikteki kaynak kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="c765f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c765f-118">PARAMETERS</span></span>

### <span data-ttu-id="c765f-119">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="c765f-119">-ApiVersion</span></span>
<span data-ttu-id="c765f-120">Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c765f-121">Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.</span><span class="sxs-lookup"><span data-stu-id="c765f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c765f-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="c765f-122">-AtScope</span></span>
<span data-ttu-id="c765f-123">Bu cmdlet 'in belirtilen kapsamda veya yukarısındaki tüm kilitleri döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="c765f-124">Bu parametreyi belirtmezseniz, cmdlet, kapsamın üstünde veya altında tüm kilitleri döndürür.</span><span class="sxs-lookup"><span data-stu-id="c765f-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="c765f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c765f-125">-DefaultProfile</span></span>
<span data-ttu-id="c765f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c765f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c765f-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="c765f-127">-LockId</span></span>
<span data-ttu-id="c765f-128">Bu cmdlet 'in aldığı kilidin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c765f-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="c765f-129">-LockName</span></span>
<span data-ttu-id="c765f-130">Bu cmdlet 'in aldığı kilidin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c765f-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="c765f-131">-Pre</span></span>
<span data-ttu-id="c765f-132">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c765f-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c765f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c765f-133">-ResourceGroupName</span></span>
<span data-ttu-id="c765f-134">Kilidin uygulandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="c765f-135">Bu cmdlet bu kaynak grubunun kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="c765f-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c765f-136">-ResourceName</span></span>
<span data-ttu-id="c765f-137">Bu kilidin uygulandığı kaynağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="c765f-138">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-138">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c765f-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c765f-139">-ResourceType</span></span>
<span data-ttu-id="c765f-140">Bu kilidin uygulandığı kaynağın kaynak türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="c765f-141">Bu cmdlet bu kaynağın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-141">This cmdlet gets locks for this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c765f-142">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c765f-142">-Scope</span></span>
<span data-ttu-id="c765f-143">Kilidin hangi kapsamda uygulanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c765f-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="c765f-144">Cmdlet bu kapsamın kilitlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c765f-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="c765f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c765f-145">CommonParameters</span></span>
<span data-ttu-id="c765f-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c765f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c765f-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c765f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c765f-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c765f-148">INPUTS</span></span>

### <span data-ttu-id="c765f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c765f-149">System.String</span></span>

## <span data-ttu-id="c765f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c765f-150">OUTPUTS</span></span>

### <span data-ttu-id="c765f-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c765f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c765f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c765f-152">NOTES</span></span>

## <span data-ttu-id="c765f-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c765f-153">RELATED LINKS</span></span>

[<span data-ttu-id="c765f-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c765f-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c765f-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c765f-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="c765f-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c765f-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


