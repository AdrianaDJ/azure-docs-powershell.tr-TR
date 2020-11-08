---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267117"
---
# <span data-ttu-id="1b76a-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b76a-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="1b76a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b76a-102">SYNOPSIS</span></span>
<span data-ttu-id="1b76a-103">Yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="1b76a-103">Delete Configuration record</span></span>

## <span data-ttu-id="1b76a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b76a-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b76a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b76a-105">DESCRIPTION</span></span>
<span data-ttu-id="1b76a-106">Bakım yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="1b76a-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="1b76a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b76a-107">EXAMPLES</span></span>

### <span data-ttu-id="1b76a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b76a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="1b76a-109">Bakım yapılandırma kaydını silme</span><span class="sxs-lookup"><span data-stu-id="1b76a-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="1b76a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b76a-110">PARAMETERS</span></span>

### <span data-ttu-id="1b76a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1b76a-111">-AsJob</span></span>
<span data-ttu-id="1b76a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1b76a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b76a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b76a-113">-DefaultProfile</span></span>
<span data-ttu-id="1b76a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b76a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b76a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1b76a-115">-Force</span></span>
<span data-ttu-id="1b76a-116">Onaysız kaldırmayı zorunlu kılın.</span><span class="sxs-lookup"><span data-stu-id="1b76a-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="1b76a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b76a-117">-Name</span></span>
<span data-ttu-id="1b76a-118">Bakım yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="1b76a-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="1b76a-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1b76a-119">-PassThru</span></span>
<span data-ttu-id="1b76a-120">Kaldırma işleminin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="1b76a-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="1b76a-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="1b76a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b76a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b76a-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b76a-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b76a-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="1b76a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b76a-124">-Confirm</span></span>
<span data-ttu-id="1b76a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b76a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b76a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b76a-126">-WhatIf</span></span>
<span data-ttu-id="1b76a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b76a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b76a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b76a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b76a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b76a-129">CommonParameters</span></span>
<span data-ttu-id="1b76a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b76a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b76a-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b76a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b76a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b76a-132">INPUTS</span></span>

### <span data-ttu-id="1b76a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1b76a-133">System.String</span></span>

## <span data-ttu-id="1b76a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b76a-134">OUTPUTS</span></span>

### <span data-ttu-id="1b76a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b76a-135">System.Boolean</span></span>

## <span data-ttu-id="1b76a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b76a-136">NOTES</span></span>

## <span data-ttu-id="1b76a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b76a-137">RELATED LINKS</span></span>
