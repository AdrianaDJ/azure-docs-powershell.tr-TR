---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: bba48b31158226d1ea63f70ceafe3355990fea6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104526"
---
# <span data-ttu-id="74427-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="74427-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="74427-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74427-102">SYNOPSIS</span></span>
<span data-ttu-id="74427-103">Veri kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="74427-103">Deletes a data source.</span></span>

## <span data-ttu-id="74427-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74427-104">SYNTAX</span></span>

### <span data-ttu-id="74427-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74427-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74427-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="74427-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74427-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="74427-107">DESCRIPTION</span></span>
<span data-ttu-id="74427-108">**Remove-Azoperationalınsightsdatasource** cmdlet 'i bir veri kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="74427-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="74427-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74427-109">EXAMPLES</span></span>

## <span data-ttu-id="74427-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74427-110">PARAMETERS</span></span>

### <span data-ttu-id="74427-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74427-111">-DefaultProfile</span></span>
<span data-ttu-id="74427-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="74427-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74427-113">-Force</span><span class="sxs-lookup"><span data-stu-id="74427-113">-Force</span></span>
<span data-ttu-id="74427-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="74427-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="74427-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="74427-115">-Name</span></span>
<span data-ttu-id="74427-116">Silinecek veri kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74427-116">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="74427-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74427-117">-ResourceGroupName</span></span>
<span data-ttu-id="74427-118">Bilgisayarları içeren bir kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74427-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74427-119">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="74427-119">-Workspace</span></span>
<span data-ttu-id="74427-120">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74427-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74427-121">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="74427-121">-WorkspaceName</span></span>
<span data-ttu-id="74427-122">Bu cmdlet 'in üzerinde çalıştırıldığı çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="74427-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74427-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="74427-123">-Confirm</span></span>
<span data-ttu-id="74427-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74427-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74427-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74427-125">-WhatIf</span></span>
<span data-ttu-id="74427-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74427-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74427-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74427-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74427-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74427-128">CommonParameters</span></span>
<span data-ttu-id="74427-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74427-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74427-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74427-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74427-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74427-131">INPUTS</span></span>

### <span data-ttu-id="74427-132">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="74427-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="74427-133">System. String</span><span class="sxs-lookup"><span data-stu-id="74427-133">System.String</span></span>

## <span data-ttu-id="74427-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74427-134">OUTPUTS</span></span>

### <span data-ttu-id="74427-135">System. void</span><span class="sxs-lookup"><span data-stu-id="74427-135">System.Void</span></span>

## <span data-ttu-id="74427-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74427-136">NOTES</span></span>
* <span data-ttu-id="74427-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="74427-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="74427-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74427-138">RELATED LINKS</span></span>

[<span data-ttu-id="74427-139">Get-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="74427-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="74427-140">Set-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="74427-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


