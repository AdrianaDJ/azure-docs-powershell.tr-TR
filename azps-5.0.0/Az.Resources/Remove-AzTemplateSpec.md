---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279824"
---
# <span data-ttu-id="c01fd-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="c01fd-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="c01fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c01fd-102">SYNOPSIS</span></span>
<span data-ttu-id="c01fd-103">Şablon açıklamasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c01fd-103">Removes a Template Spec</span></span>

## <span data-ttu-id="c01fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c01fd-104">SYNTAX</span></span>

### <span data-ttu-id="c01fd-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c01fd-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c01fd-106">Removebyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c01fd-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c01fd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c01fd-107">DESCRIPTION</span></span>
<span data-ttu-id="c01fd-108">Belirtilen bir şablon açıklamasını kaldırır. Sürüm **sürümü** parametresi sağlanmışsa, yalnızca belirtilen sürüm kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c01fd-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="c01fd-109">Belirli bir sürüm sağlanmazsa, şablon belirtimi ve tüm sürümleri kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c01fd-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="c01fd-110">**-Force** bayrağı varsa, kaldırılmak üzere onay istemi olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="c01fd-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="c01fd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c01fd-111">EXAMPLES</span></span>

### <span data-ttu-id="c01fd-112">Örnek 1: ada göre belirli bir sürümü çıkarma</span><span class="sxs-lookup"><span data-stu-id="c01fd-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="c01fd-113">' MyTemplateSpec ' adlı şablon belirtiminin ' myRG ' kaynak grubunda sürümünü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c01fd-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="c01fd-114">Örnek 2: kaynak kimliğiyle belirli bir sürümü kaldırmak</span><span class="sxs-lookup"><span data-stu-id="c01fd-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="c01fd-115">Abonelik alt kimliğindeki ' myRG ' kaynak grubunun içinde ' MyTemplateSpec ' adlı şablon belirtiminin sürümünü kaldırır \{ \} .</span><span class="sxs-lookup"><span data-stu-id="c01fd-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="c01fd-116">Örnek 3: şablon belirtiminin ve tüm sürümlerin adına göre kaldırılması</span><span class="sxs-lookup"><span data-stu-id="c01fd-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="c01fd-117">' MyTemplateSpec ' adlı şablon spec 'i ve kaynak grubundaki tüm sürümlerini ' myRG ' olarak kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c01fd-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="c01fd-118">Örnek 3: kaynak kimliğine göre şablon belirtiminin ve tüm sürümlerinin kaldırılması</span><span class="sxs-lookup"><span data-stu-id="c01fd-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="c01fd-119">' MyTemplateSpec ' adlı şablon belirtiminin ve abonelik alt kimliğindeki ' myRG ' kaynak grubundaki tüm sürümlerini kaldırır \{ \} .</span><span class="sxs-lookup"><span data-stu-id="c01fd-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="c01fd-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c01fd-120">PARAMETERS</span></span>

### <span data-ttu-id="c01fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c01fd-121">-DefaultProfile</span></span>
<span data-ttu-id="c01fd-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c01fd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c01fd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c01fd-123">-Force</span></span>
<span data-ttu-id="c01fd-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="c01fd-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c01fd-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="c01fd-125">-Name</span></span>
<span data-ttu-id="c01fd-126">Şablon belirtiminin adı.</span><span class="sxs-lookup"><span data-stu-id="c01fd-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c01fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="c01fd-128">Şablon belirtiminin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c01fd-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01fd-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c01fd-129">-ResourceId</span></span>
<span data-ttu-id="c01fd-130">Şablon belirtiminin tam kaynak kimliği. örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="c01fd-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01fd-131">-Version</span><span class="sxs-lookup"><span data-stu-id="c01fd-131">-Version</span></span>
<span data-ttu-id="c01fd-132">Silinecek şablon belirtiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="c01fd-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c01fd-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="c01fd-133">-Confirm</span></span>
<span data-ttu-id="c01fd-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c01fd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c01fd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c01fd-135">-WhatIf</span></span>
<span data-ttu-id="c01fd-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c01fd-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c01fd-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c01fd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c01fd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c01fd-138">CommonParameters</span></span>
<span data-ttu-id="c01fd-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c01fd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c01fd-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c01fd-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c01fd-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c01fd-141">INPUTS</span></span>

### <span data-ttu-id="c01fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c01fd-142">System.String</span></span>

## <span data-ttu-id="c01fd-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c01fd-143">OUTPUTS</span></span>

### <span data-ttu-id="c01fd-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c01fd-144">System.Boolean</span></span>

## <span data-ttu-id="c01fd-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c01fd-145">NOTES</span></span>

## <span data-ttu-id="c01fd-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c01fd-146">RELATED LINKS</span></span>
