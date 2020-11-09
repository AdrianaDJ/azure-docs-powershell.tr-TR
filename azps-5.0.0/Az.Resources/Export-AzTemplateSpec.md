---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322411"
---
# <span data-ttu-id="4ce07-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="4ce07-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="4ce07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ce07-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce07-103">Yerel FileSystem 'a şablon belirtimi dışarı aktarır</span><span class="sxs-lookup"><span data-stu-id="4ce07-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="4ce07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ce07-104">SYNTAX</span></span>

### <span data-ttu-id="4ce07-105">ExportByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ce07-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ce07-106">Exportbyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4ce07-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ce07-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ce07-107">DESCRIPTION</span></span>
<span data-ttu-id="4ce07-108">Belirli bir şablon spec sürümünü yerel FileSystem 'a aktarır.</span><span class="sxs-lookup"><span data-stu-id="4ce07-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="4ce07-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ce07-109">EXAMPLES</span></span>

### <span data-ttu-id="4ce07-110">Örnek 1: ada göre dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="4ce07-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="4ce07-111">' MyTemplateSpec ' adlı şablon belirtiminin ' v 1.0 ' sürümünü, ' myRG ' kaynak grubunun içinde "v1" yerel çıkış klasörüne dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="4ce07-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="4ce07-112">Örnek 2: kaynak kimliğiyle dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="4ce07-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="4ce07-113">Abonelik alt kimliğindeki ' MyTemplateSpec ' adlı şablon belirtiminin ' v 1.0 ' sürümünü \{ \} "v1" yerel çıkış klasörüne dışarı aktarır.</span><span class="sxs-lookup"><span data-stu-id="4ce07-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="4ce07-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ce07-114">PARAMETERS</span></span>

### <span data-ttu-id="4ce07-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ce07-115">-DefaultProfile</span></span>
<span data-ttu-id="4ce07-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ce07-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ce07-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ce07-117">-Name</span></span>
<span data-ttu-id="4ce07-118">Şablon belirtiminin adı.</span><span class="sxs-lookup"><span data-stu-id="4ce07-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce07-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="4ce07-119">-OutputFolder</span></span>
<span data-ttu-id="4ce07-120">Şablon belirtiminin sürümünün çıktı edileceği klasörün yolu.</span><span class="sxs-lookup"><span data-stu-id="4ce07-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce07-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ce07-122">Şablon belirtiminin kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4ce07-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce07-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4ce07-123">-ResourceId</span></span>
<span data-ttu-id="4ce07-124">Şablon belirtiminin tam kaynak kimliği. örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="4ce07-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce07-125">-Version</span><span class="sxs-lookup"><span data-stu-id="4ce07-125">-Version</span></span>
<span data-ttu-id="4ce07-126">Dışarı aktarılacak şablon belirtiminin sürümü.</span><span class="sxs-lookup"><span data-stu-id="4ce07-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce07-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ce07-127">-Confirm</span></span>
<span data-ttu-id="4ce07-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ce07-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce07-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce07-129">-WhatIf</span></span>
<span data-ttu-id="4ce07-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ce07-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ce07-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ce07-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ce07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ce07-132">CommonParameters</span></span>
<span data-ttu-id="4ce07-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ce07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ce07-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ce07-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ce07-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ce07-135">INPUTS</span></span>

### <span data-ttu-id="4ce07-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce07-136">System.String</span></span>

## <span data-ttu-id="4ce07-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ce07-137">OUTPUTS</span></span>

### <span data-ttu-id="4ce07-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4ce07-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4ce07-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ce07-139">NOTES</span></span>

## <span data-ttu-id="4ce07-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ce07-140">RELATED LINKS</span></span>
