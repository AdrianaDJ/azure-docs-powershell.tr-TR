---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/update-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Update-AzMaintenanceConfiguration.md
ms.openlocfilehash: ed6f94944f00cd138d3140c2bd69029a98ea9f15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104215"
---
# <span data-ttu-id="68dd9-101">Update-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="68dd9-101">Update-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="68dd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="68dd9-103">Düzeltme Eki yapılandırma kaydı</span><span class="sxs-lookup"><span data-stu-id="68dd9-103">Patch configuration record</span></span>

## <span data-ttu-id="68dd9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68dd9-104">SYNTAX</span></span>

```
Update-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String>
 [-Configuration] <PSMaintenanceConfiguration> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68dd9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="68dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="68dd9-106">Düzeltme Eki bakım kaydı</span><span class="sxs-lookup"><span data-stu-id="68dd9-106">Patch maintenance configuration record</span></span>

## <span data-ttu-id="68dd9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68dd9-107">EXAMPLES</span></span>

### <span data-ttu-id="68dd9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68dd9-108">Example 1</span></span>
```powershell
PS C:\> Update-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -Configuration $configuration


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="68dd9-109">Düzeltme Eki bakım kaydı</span><span class="sxs-lookup"><span data-stu-id="68dd9-109">Patch maintenance configuration record</span></span>

## <span data-ttu-id="68dd9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68dd9-110">PARAMETERS</span></span>

### <span data-ttu-id="68dd9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="68dd9-111">-AsJob</span></span>
<span data-ttu-id="68dd9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="68dd9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68dd9-113">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="68dd9-113">-Configuration</span></span>
<span data-ttu-id="68dd9-114">Güncelleştirilecek bakım yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="68dd9-114">The maintenance configuration to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68dd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68dd9-115">-DefaultProfile</span></span>
<span data-ttu-id="68dd9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68dd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68dd9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="68dd9-117">-Name</span></span>
<span data-ttu-id="68dd9-118">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="68dd9-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="68dd9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68dd9-119">-ResourceGroupName</span></span>
<span data-ttu-id="68dd9-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="68dd9-120">The resource Group Name.</span></span>

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

### <span data-ttu-id="68dd9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="68dd9-121">-Confirm</span></span>
<span data-ttu-id="68dd9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68dd9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68dd9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68dd9-123">-WhatIf</span></span>
<span data-ttu-id="68dd9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68dd9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68dd9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68dd9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68dd9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68dd9-126">CommonParameters</span></span>
<span data-ttu-id="68dd9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68dd9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68dd9-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68dd9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68dd9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68dd9-129">INPUTS</span></span>

### <span data-ttu-id="68dd9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="68dd9-130">System.String</span></span>

### <span data-ttu-id="68dd9-131">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="68dd9-131">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="68dd9-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68dd9-132">OUTPUTS</span></span>

### <span data-ttu-id="68dd9-133">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="68dd9-133">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="68dd9-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68dd9-134">NOTES</span></span>

## <span data-ttu-id="68dd9-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68dd9-135">RELATED LINKS</span></span>
