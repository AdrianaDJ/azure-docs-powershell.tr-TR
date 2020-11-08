---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278916"
---
# <span data-ttu-id="42602-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="42602-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="42602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42602-102">SYNOPSIS</span></span>
<span data-ttu-id="42602-103">Kaynak için bakım güncelleştirmelerini izleme</span><span class="sxs-lookup"><span data-stu-id="42602-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="42602-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42602-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42602-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42602-105">DESCRIPTION</span></span>
<span data-ttu-id="42602-106">Kaynak için bakım güncelleştirmelerini izleme</span><span class="sxs-lookup"><span data-stu-id="42602-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="42602-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42602-107">EXAMPLES</span></span>

### <span data-ttu-id="42602-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42602-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="42602-109">Kaynak için bakım güncelleştirmelerini izleme</span><span class="sxs-lookup"><span data-stu-id="42602-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="42602-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42602-110">PARAMETERS</span></span>

### <span data-ttu-id="42602-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="42602-111">-ApplyUpdateName</span></span>
<span data-ttu-id="42602-112">Güncelleştirme kaynağı adı.</span><span class="sxs-lookup"><span data-stu-id="42602-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="42602-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42602-113">-DefaultProfile</span></span>
<span data-ttu-id="42602-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42602-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42602-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="42602-115">-ProviderName</span></span>
<span data-ttu-id="42602-116">Kaynak sağlayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="42602-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="42602-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42602-117">-ResourceGroupName</span></span>
<span data-ttu-id="42602-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42602-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="42602-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="42602-119">-ResourceName</span></span>
<span data-ttu-id="42602-120">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="42602-120">The resource name.</span></span>

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

### <span data-ttu-id="42602-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="42602-121">-ResourceParentName</span></span>
<span data-ttu-id="42602-122">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="42602-122">The parent resource name.</span></span>

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

### <span data-ttu-id="42602-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="42602-123">-ResourceParentType</span></span>
<span data-ttu-id="42602-124">Üst kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="42602-124">The parent resource type.</span></span>

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

### <span data-ttu-id="42602-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="42602-125">-ResourceType</span></span>
<span data-ttu-id="42602-126">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="42602-126">The resource type.</span></span>

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

### <span data-ttu-id="42602-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42602-127">CommonParameters</span></span>
<span data-ttu-id="42602-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42602-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42602-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42602-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42602-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42602-130">INPUTS</span></span>

### <span data-ttu-id="42602-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42602-131">System.String</span></span>

## <span data-ttu-id="42602-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42602-132">OUTPUTS</span></span>

### <span data-ttu-id="42602-133">Microsoft. Azure. Commands. Maintenance. modeller. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="42602-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="42602-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42602-134">NOTES</span></span>

## <span data-ttu-id="42602-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42602-135">RELATED LINKS</span></span>
