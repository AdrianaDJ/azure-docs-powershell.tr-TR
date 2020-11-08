---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278864"
---
# <span data-ttu-id="ca300-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="ca300-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="ca300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca300-102">SYNOPSIS</span></span>
<span data-ttu-id="ca300-103">Yeni bir geçiş projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca300-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="ca300-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca300-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ca300-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca300-105">DESCRIPTION</span></span>
<span data-ttu-id="ca300-106">Yeni bir geçiş projesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca300-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="ca300-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca300-107">EXAMPLES</span></span>

### <span data-ttu-id="ca300-108">Örnek 1: oluşturma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ca300-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="ca300-109">Yeni bir geçiş projesi oluşturma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="ca300-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="ca300-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca300-110">PARAMETERS</span></span>

### <span data-ttu-id="ca300-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="ca300-111">-ETag</span></span>
<span data-ttu-id="ca300-112">VMware makine adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="ca300-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="ca300-113">-Location</span></span>
<span data-ttu-id="ca300-114">VMware makine adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="ca300-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca300-115">-Name</span></span>
<span data-ttu-id="ca300-116">Proje adını geçir 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="ca300-117">-Özellik</span><span class="sxs-lookup"><span data-stu-id="ca300-117">-Property</span></span>
<span data-ttu-id="ca300-118">Proje özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-118">Specifies the project properties.</span></span>
<span data-ttu-id="ca300-119">Oluşturmak için, ÖZELLIK özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca300-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca300-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca300-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca300-121">Kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="ca300-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ca300-122">-SubscriptionId</span></span>
<span data-ttu-id="ca300-123">Abonelik kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-123">Specifies the subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca300-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca300-124">-Confirm</span></span>
<span data-ttu-id="ca300-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca300-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca300-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca300-126">-WhatIf</span></span>
<span data-ttu-id="ca300-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca300-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca300-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca300-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca300-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca300-129">CommonParameters</span></span>
<span data-ttu-id="ca300-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca300-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca300-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ca300-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca300-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca300-132">INPUTS</span></span>

## <span data-ttu-id="ca300-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca300-133">OUTPUTS</span></span>

## <span data-ttu-id="ca300-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca300-134">NOTES</span></span>

<span data-ttu-id="ca300-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ca300-135">ALIASES</span></span>

<span data-ttu-id="ca300-136">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="ca300-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca300-137">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ca300-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca300-138">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca300-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca300-139">ÖZELLIK <IMigrateProjectProperties> : proje özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca300-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="ca300-140">`[ProvisioningState <ProvisioningState?>]`: Projeyi geçir hazırlama durumu.</span><span class="sxs-lookup"><span data-stu-id="ca300-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="ca300-141">`[RegisteredTool <String[]>]`: Geçirme projesi ile kaydedilen araçların listesini alır veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ca300-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="ca300-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca300-142">RELATED LINKS</span></span>

