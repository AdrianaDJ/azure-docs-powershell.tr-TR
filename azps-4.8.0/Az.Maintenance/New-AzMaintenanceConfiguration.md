---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzMaintenanceConfiguration.md
ms.openlocfilehash: bc2932f91bd2f7361d98ebbe6516ae8bec1513cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267118"
---
# <span data-ttu-id="94a9d-101">New-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="94a9d-101">New-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="94a9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94a9d-102">SYNOPSIS</span></span>
<span data-ttu-id="94a9d-103">Yapılandırma kaydı oluştur veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="94a9d-103">Create or Update configuration record</span></span>

## <span data-ttu-id="94a9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94a9d-104">SYNTAX</span></span>

```
New-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-ExtensionProperty <Hashtable>] [-MaintenanceScope <String>] [-StartDateTime <String>]
 [-ExpirationDateTime <String>] [-Timezone <String>] [-Duration <TimeSpan>] [-Visibility <String>]
 [-RecurEvery <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94a9d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94a9d-105">DESCRIPTION</span></span>
<span data-ttu-id="94a9d-106">Yapılandırma kaydı oluştur veya güncelleştir</span><span class="sxs-lookup"><span data-stu-id="94a9d-106">Create or Update configuration record</span></span>

## <span data-ttu-id="94a9d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94a9d-107">EXAMPLES</span></span>

### <span data-ttu-id="94a9d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="94a9d-108">Example 1</span></span>
```powershell
PS C:\> New-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus -MaintenanceScope Host -Location centralus -StartDateTime 2020-08-01 00:00 -ExpirationDateTime 2021-08-04 00:00 -TimeZone Pacific Standard Time -Duration 05:00 -RecurEvery Day


Location            : centralus
Tags                : {}
ExtensionProperties : {}
MaintenanceScope    : Host
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : Host
Visibility          : Custom
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="94a9d-109">Kapsam ana bilgisayarıyla bakım yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="94a9d-109">Create a maintenance configuration with scope Host</span></span>

## <span data-ttu-id="94a9d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94a9d-110">PARAMETERS</span></span>

### <span data-ttu-id="94a9d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="94a9d-111">-AsJob</span></span>
<span data-ttu-id="94a9d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="94a9d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94a9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a9d-113">-DefaultProfile</span></span>
<span data-ttu-id="94a9d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94a9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94a9d-115">-Süre</span><span class="sxs-lookup"><span data-stu-id="94a9d-115">-Duration</span></span>
<span data-ttu-id="94a9d-116">Süre</span><span class="sxs-lookup"><span data-stu-id="94a9d-116">The duration</span></span>


```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94a9d-117">-ExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="94a9d-117">-ExpirationDateTime</span></span>
<span data-ttu-id="94a9d-118">Zamanlamanın saat biçimi: YYYY-AA-GG SS: dd biçiminde</span><span class="sxs-lookup"><span data-stu-id="94a9d-118">The expirationDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="94a9d-119">-ExtensionProperty</span><span class="sxs-lookup"><span data-stu-id="94a9d-119">-ExtensionProperty</span></span>
<span data-ttu-id="94a9d-120">Kaynak başına uzantı özellikleri.</span><span class="sxs-lookup"><span data-stu-id="94a9d-120">The Extension properties per resource.</span></span>

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

### <span data-ttu-id="94a9d-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="94a9d-121">-Location</span></span>
<span data-ttu-id="94a9d-122">Bakım yapılandırma konumu.</span><span class="sxs-lookup"><span data-stu-id="94a9d-122">The maintenance configuration location.</span></span>

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

### <span data-ttu-id="94a9d-123">-MaintenanceScope</span><span class="sxs-lookup"><span data-stu-id="94a9d-123">-MaintenanceScope</span></span>
<span data-ttu-id="94a9d-124">Bakım kapsamı.</span><span class="sxs-lookup"><span data-stu-id="94a9d-124">The Maintenance Scope.</span></span>

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

### <span data-ttu-id="94a9d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="94a9d-125">-Name</span></span>
<span data-ttu-id="94a9d-126">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="94a9d-126">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="94a9d-127">-RecurEvery</span><span class="sxs-lookup"><span data-stu-id="94a9d-127">-RecurEvery</span></span>
<span data-ttu-id="94a9d-128">Zamanlama yinelemesi</span><span class="sxs-lookup"><span data-stu-id="94a9d-128">The schedule recurrence</span></span>

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

### <span data-ttu-id="94a9d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a9d-129">-ResourceGroupName</span></span>
<span data-ttu-id="94a9d-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="94a9d-130">The resource Group Name.</span></span>

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

### <span data-ttu-id="94a9d-131">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="94a9d-131">-StartDateTime</span></span>
<span data-ttu-id="94a9d-132">Zamanlamanın Startdatetıme değeri YYYY-AA-GG SS: dd biçiminde</span><span class="sxs-lookup"><span data-stu-id="94a9d-132">The StartDateTime of the schedule in format YYYY-MM-DD hh:mm</span></span>

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

### <span data-ttu-id="94a9d-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="94a9d-133">-Tag</span></span>
<span data-ttu-id="94a9d-134">ARM etiketleri.</span><span class="sxs-lookup"><span data-stu-id="94a9d-134">The ARM Tags.</span></span>

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

### <span data-ttu-id="94a9d-135">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="94a9d-135">-Timezone</span></span>
<span data-ttu-id="94a9d-136">Saat dilimi</span><span class="sxs-lookup"><span data-stu-id="94a9d-136">The timezone</span></span>

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

### <span data-ttu-id="94a9d-137">-Görünürlük</span><span class="sxs-lookup"><span data-stu-id="94a9d-137">-Visibility</span></span>
<span data-ttu-id="94a9d-138">Kapsamın görünürlüğü</span><span class="sxs-lookup"><span data-stu-id="94a9d-138">The visibility of the scope</span></span>

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

### <span data-ttu-id="94a9d-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="94a9d-139">-Confirm</span></span>
<span data-ttu-id="94a9d-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="94a9d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a9d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a9d-141">-WhatIf</span></span>
<span data-ttu-id="94a9d-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="94a9d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a9d-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="94a9d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a9d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a9d-144">CommonParameters</span></span>
<span data-ttu-id="94a9d-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94a9d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a9d-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="94a9d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a9d-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94a9d-147">INPUTS</span></span>

### <span data-ttu-id="94a9d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="94a9d-148">System.String</span></span>

## <span data-ttu-id="94a9d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94a9d-149">OUTPUTS</span></span>

### <span data-ttu-id="94a9d-150">Microsoft. Azure. Commands. Maintenance. modeller. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="94a9d-150">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="94a9d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94a9d-151">NOTES</span></span>

## <span data-ttu-id="94a9d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94a9d-152">RELATED LINKS</span></span>
