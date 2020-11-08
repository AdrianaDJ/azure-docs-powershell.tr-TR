---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267126"
---
# <span data-ttu-id="aabe3-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="aabe3-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="aabe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aabe3-102">SYNOPSIS</span></span>
<span data-ttu-id="aabe3-103">Kaynağın yapılandırmasını kaydettirme.</span><span class="sxs-lookup"><span data-stu-id="aabe3-103">Register configuration for resource.</span></span>

## <span data-ttu-id="aabe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aabe3-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aabe3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aabe3-105">DESCRIPTION</span></span>
<span data-ttu-id="aabe3-106">Kaynağın bakım yapılandırmasını kaydettirme.</span><span class="sxs-lookup"><span data-stu-id="aabe3-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="aabe3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aabe3-107">EXAMPLES</span></span>

### <span data-ttu-id="aabe3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aabe3-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="aabe3-109">Adanmış ana bilgisayar için bakım yapılandırmasını kaydettirme.</span><span class="sxs-lookup"><span data-stu-id="aabe3-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="aabe3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aabe3-110">PARAMETERS</span></span>

### <span data-ttu-id="aabe3-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="aabe3-111">-AsJob</span></span>
<span data-ttu-id="aabe3-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="aabe3-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aabe3-113">-Configurationatamaadı</span><span class="sxs-lookup"><span data-stu-id="aabe3-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="aabe3-114">Yapılandırma atama adı, MaintenanceConfigurationName eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="aabe3-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="aabe3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabe3-115">-DefaultProfile</span></span>
<span data-ttu-id="aabe3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aabe3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aabe3-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="aabe3-117">-Location</span></span>
<span data-ttu-id="aabe3-118">Kaynak için boşluksuz konum.</span><span class="sxs-lookup"><span data-stu-id="aabe3-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabe3-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="aabe3-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="aabe3-120">Tam nitelikli MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aabe3-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabe3-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="aabe3-121">-ProviderName</span></span>
<span data-ttu-id="aabe3-122">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="aabe3-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="aabe3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabe3-123">-ResourceGroupName</span></span>
<span data-ttu-id="aabe3-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="aabe3-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="aabe3-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aabe3-125">-ResourceId</span></span>
<span data-ttu-id="aabe3-126">Yapılandırma atama adı, MaintenanceConfigurationName eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="aabe3-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="aabe3-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aabe3-127">-ResourceName</span></span>
<span data-ttu-id="aabe3-128">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="aabe3-128">The resource name.</span></span>

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

### <span data-ttu-id="aabe3-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="aabe3-129">-ResourceParentName</span></span>
<span data-ttu-id="aabe3-130">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="aabe3-130">The parent resource name.</span></span>

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

### <span data-ttu-id="aabe3-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="aabe3-131">-ResourceParentType</span></span>
<span data-ttu-id="aabe3-132">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="aabe3-132">The parent resource type.</span></span>

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

### <span data-ttu-id="aabe3-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aabe3-133">-ResourceType</span></span>
<span data-ttu-id="aabe3-134">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="aabe3-134">The resource type.</span></span>

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

### <span data-ttu-id="aabe3-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="aabe3-135">-Confirm</span></span>
<span data-ttu-id="aabe3-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aabe3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aabe3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabe3-137">-WhatIf</span></span>
<span data-ttu-id="aabe3-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aabe3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabe3-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aabe3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aabe3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabe3-140">CommonParameters</span></span>
<span data-ttu-id="aabe3-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aabe3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabe3-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aabe3-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabe3-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aabe3-143">INPUTS</span></span>

### <span data-ttu-id="aabe3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="aabe3-144">System.String</span></span>

## <span data-ttu-id="aabe3-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aabe3-145">OUTPUTS</span></span>

### <span data-ttu-id="aabe3-146">Microsoft. Azure. Commands. Maintenance. modeller. Psconfigurationödev</span><span class="sxs-lookup"><span data-stu-id="aabe3-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="aabe3-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aabe3-147">NOTES</span></span>

## <span data-ttu-id="aabe3-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aabe3-148">RELATED LINKS</span></span>
