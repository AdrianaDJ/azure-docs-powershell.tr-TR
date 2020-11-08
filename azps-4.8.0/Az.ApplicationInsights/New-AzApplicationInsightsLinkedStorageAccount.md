---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266134"
---
# <span data-ttu-id="5b9da-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5b9da-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5b9da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9da-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9da-103">Application Insights bağlantılı depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b9da-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="5b9da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b9da-104">SYNTAX</span></span>

### <span data-ttu-id="5b9da-105">ByResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5b9da-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b9da-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b9da-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b9da-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="5b9da-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b9da-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b9da-108">DESCRIPTION</span></span>
<span data-ttu-id="5b9da-109">Application Insights bağlantılı depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b9da-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="5b9da-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b9da-110">EXAMPLES</span></span>

### <span data-ttu-id="5b9da-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5b9da-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="5b9da-112">"ComponentName" bileşeni altında bağlı depolama hesabı $account oluştur</span><span class="sxs-lookup"><span data-stu-id="5b9da-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="5b9da-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b9da-113">PARAMETERS</span></span>

### <span data-ttu-id="5b9da-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5b9da-114">-ComponentName</span></span>
<span data-ttu-id="5b9da-115">Bileşen adı</span><span class="sxs-lookup"><span data-stu-id="5b9da-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9da-116">-DefaultProfile</span></span>
<span data-ttu-id="5b9da-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b9da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b9da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b9da-118">-InputObject</span></span>
<span data-ttu-id="5b9da-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5b9da-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b9da-120">-Linkedstorageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="5b9da-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="5b9da-121">Depolama hesabı RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5b9da-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="5b9da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b9da-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b9da-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="5b9da-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9da-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5b9da-124">-ResourceId</span></span>
<span data-ttu-id="5b9da-125">Bileşen RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5b9da-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b9da-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b9da-126">-Confirm</span></span>
<span data-ttu-id="5b9da-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b9da-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b9da-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b9da-128">-WhatIf</span></span>
<span data-ttu-id="5b9da-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b9da-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b9da-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b9da-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b9da-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9da-131">CommonParameters</span></span>
<span data-ttu-id="5b9da-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b9da-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9da-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5b9da-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9da-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b9da-134">INPUTS</span></span>

### <span data-ttu-id="5b9da-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5b9da-135">System.String</span></span>

### <span data-ttu-id="5b9da-136">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5b9da-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5b9da-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b9da-137">OUTPUTS</span></span>

### <span data-ttu-id="5b9da-138">Microsoft. Azure. Commands. ApplicationInsights. model. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5b9da-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="5b9da-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b9da-139">NOTES</span></span>

## <span data-ttu-id="5b9da-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b9da-140">RELATED LINKS</span></span>
