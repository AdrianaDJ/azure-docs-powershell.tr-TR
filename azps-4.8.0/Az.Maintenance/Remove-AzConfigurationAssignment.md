---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267121"
---
# <span data-ttu-id="8719a-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="8719a-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="8719a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8719a-102">SYNOPSIS</span></span>
<span data-ttu-id="8719a-103">Kaynağın yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="8719a-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8719a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8719a-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8719a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8719a-105">DESCRIPTION</span></span>
<span data-ttu-id="8719a-106">Kaynağın yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="8719a-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8719a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8719a-107">EXAMPLES</span></span>

### <span data-ttu-id="8719a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8719a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="8719a-109">Kaynağın yapılandırmasını silme.</span><span class="sxs-lookup"><span data-stu-id="8719a-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="8719a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8719a-110">PARAMETERS</span></span>

### <span data-ttu-id="8719a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="8719a-111">-AsJob</span></span>
<span data-ttu-id="8719a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8719a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8719a-113">-Configurationatamaadı</span><span class="sxs-lookup"><span data-stu-id="8719a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="8719a-114">Yapılandırma atama adı.</span><span class="sxs-lookup"><span data-stu-id="8719a-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="8719a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8719a-115">-DefaultProfile</span></span>
<span data-ttu-id="8719a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8719a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8719a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8719a-117">-Force</span></span>
<span data-ttu-id="8719a-118">Onaysız kaldırmayı zorunlu kılın.</span><span class="sxs-lookup"><span data-stu-id="8719a-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="8719a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8719a-119">-PassThru</span></span>
<span data-ttu-id="8719a-120">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="8719a-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8719a-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8719a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8719a-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="8719a-122">-ProviderName</span></span>
<span data-ttu-id="8719a-123">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="8719a-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8719a-124">-ResourceGroupName</span></span>
<span data-ttu-id="8719a-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8719a-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8719a-126">-ResourceName</span></span>
<span data-ttu-id="8719a-127">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8719a-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="8719a-128">-ResourceParentName</span></span>
<span data-ttu-id="8719a-129">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="8719a-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="8719a-130">-ResourceParentType</span></span>
<span data-ttu-id="8719a-131">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="8719a-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8719a-132">-ResourceType</span></span>
<span data-ttu-id="8719a-133">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="8719a-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8719a-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="8719a-134">-Confirm</span></span>
<span data-ttu-id="8719a-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8719a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8719a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8719a-136">-WhatIf</span></span>
<span data-ttu-id="8719a-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8719a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8719a-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8719a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8719a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8719a-139">CommonParameters</span></span>
<span data-ttu-id="8719a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8719a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8719a-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8719a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8719a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8719a-142">INPUTS</span></span>

### <span data-ttu-id="8719a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8719a-143">System.String</span></span>

## <span data-ttu-id="8719a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8719a-144">OUTPUTS</span></span>

### <span data-ttu-id="8719a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8719a-145">System.Boolean</span></span>

## <span data-ttu-id="8719a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8719a-146">NOTES</span></span>

## <span data-ttu-id="8719a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8719a-147">RELATED LINKS</span></span>
