---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104213"
---
# <span data-ttu-id="178cc-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="178cc-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="178cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="178cc-102">SYNOPSIS</span></span>
<span data-ttu-id="178cc-103">Yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="178cc-103">Delete Configuration record</span></span>

## <span data-ttu-id="178cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="178cc-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="178cc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="178cc-105">DESCRIPTION</span></span>
<span data-ttu-id="178cc-106">Bakım yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="178cc-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="178cc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="178cc-107">EXAMPLES</span></span>

### <span data-ttu-id="178cc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="178cc-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="178cc-109">Bakım yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="178cc-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="178cc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="178cc-110">PARAMETERS</span></span>

### <span data-ttu-id="178cc-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="178cc-111">-AsJob</span></span>
<span data-ttu-id="178cc-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="178cc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="178cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178cc-113">-DefaultProfile</span></span>
<span data-ttu-id="178cc-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="178cc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="178cc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="178cc-115">-Force</span></span>
<span data-ttu-id="178cc-116">Onaysız kaldırmayı zorunlu kılın.</span><span class="sxs-lookup"><span data-stu-id="178cc-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="178cc-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="178cc-117">-Name</span></span>
<span data-ttu-id="178cc-118">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="178cc-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="178cc-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="178cc-119">-PassThru</span></span>
<span data-ttu-id="178cc-120">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="178cc-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="178cc-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="178cc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="178cc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178cc-122">-ResourceGroupName</span></span>
<span data-ttu-id="178cc-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="178cc-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="178cc-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="178cc-124">-Confirm</span></span>
<span data-ttu-id="178cc-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="178cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="178cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178cc-126">-WhatIf</span></span>
<span data-ttu-id="178cc-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="178cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178cc-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="178cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="178cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178cc-129">CommonParameters</span></span>
<span data-ttu-id="178cc-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="178cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178cc-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="178cc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178cc-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="178cc-132">INPUTS</span></span>

### <span data-ttu-id="178cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="178cc-133">System.String</span></span>

## <span data-ttu-id="178cc-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="178cc-134">OUTPUTS</span></span>

### <span data-ttu-id="178cc-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="178cc-135">System.Boolean</span></span>

## <span data-ttu-id="178cc-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="178cc-136">NOTES</span></span>

## <span data-ttu-id="178cc-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="178cc-137">RELATED LINKS</span></span>
