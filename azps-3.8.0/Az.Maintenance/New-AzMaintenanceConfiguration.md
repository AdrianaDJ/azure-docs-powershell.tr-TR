---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: eb51fe99a1dbfdd5838fcd4fd5de93a5d7fb36e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104220"
---
# <span data-ttu-id="01310-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="01310-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="01310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01310-102">SYNOPSIS</span></span>
<span data-ttu-id="01310-103">Yapılandırma kaydı oluştur veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="01310-103">Create or Update configuration record</span></span>

## <span data-ttu-id="01310-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01310-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01310-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01310-105">DESCRIPTION</span></span>
<span data-ttu-id="01310-106">Yapılandırma kaydı oluştur veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="01310-106">Create or Update configuration record</span></span>

## <span data-ttu-id="01310-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01310-107">EXAMPLES</span></span>

### <span data-ttu-id="01310-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01310-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="01310-109">Kapsam ana bilgisayarıyla bakım yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="01310-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="01310-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01310-110">PARAMETERS</span></span>

### <span data-ttu-id="01310-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="01310-111">-AsJob</span></span>
<span data-ttu-id="01310-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="01310-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01310-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01310-113">-DefaultProfile</span></span>
<span data-ttu-id="01310-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01310-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01310-115">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="01310-115">-ExtensionProperty</span></span>
<span data-ttu-id="01310-116">Kaynak başına uzantı özellikleri.</span><span class="sxs-lookup"><span data-stu-id="01310-116">The Extension properties per resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01310-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="01310-117">-Location</span></span>
<span data-ttu-id="01310-118">Bakım yapılandırma konumu.</span><span class="sxs-lookup"><span data-stu-id="01310-118">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="01310-119">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="01310-119">-MaintenanceScope</span></span>
<span data-ttu-id="01310-120">Bakım kapsamı.</span><span class="sxs-lookup"><span data-stu-id="01310-120">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="01310-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="01310-121">-Name</span></span>
<span data-ttu-id="01310-122">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="01310-122">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="01310-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01310-123">-ResourceGroupName</span></span>
<span data-ttu-id="01310-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="01310-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="01310-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01310-125">-Tag</span></span>
<span data-ttu-id="01310-126">ARM etiketleri.</span><span class="sxs-lookup"><span data-stu-id="01310-126">The ARM Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01310-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="01310-127">-Confirm</span></span>
<span data-ttu-id="01310-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01310-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01310-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01310-129">-WhatIf</span></span>
<span data-ttu-id="01310-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01310-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01310-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01310-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01310-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01310-132">CommonParameters</span></span>
<span data-ttu-id="01310-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01310-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01310-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="01310-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01310-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01310-135">INPUTS</span></span>

### <span data-ttu-id="01310-136">System. String</span><span class="sxs-lookup"><span data-stu-id="01310-136">System.String</span></span>

## <span data-ttu-id="01310-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01310-137">OUTPUTS</span></span>

### <span data-ttu-id="01310-138">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="01310-138">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="01310-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01310-139">NOTES</span></span>

## <span data-ttu-id="01310-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01310-140">RELATED LINKS</span></span>
