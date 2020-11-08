---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096668"
---
# <span data-ttu-id="af9ad-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="af9ad-101">Update-AzAlertState</span></span>

## <span data-ttu-id="af9ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="af9ad-103">Durum güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="af9ad-103">Updates alert state</span></span>

## <span data-ttu-id="af9ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af9ad-104">SYNTAX</span></span>

### <span data-ttu-id="af9ad-105">ByAlertId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af9ad-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9ad-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af9ad-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af9ad-107">DESCRIPTION</span></span>
<span data-ttu-id="af9ad-108">**Update-AzAlertState** cmdlet güncelleştirmeleri uyarı durumunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af9ad-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="af9ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af9ad-109">EXAMPLES</span></span>

### <span data-ttu-id="af9ad-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="af9ad-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="af9ad-111">Bu cmdlet, uyarı durumunu kapalıya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="af9ad-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="af9ad-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af9ad-112">PARAMETERS</span></span>

### <span data-ttu-id="af9ad-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="af9ad-113">-AlertId</span></span>
<span data-ttu-id="af9ad-114">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="af9ad-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9ad-115">-DefaultProfile</span></span>
<span data-ttu-id="af9ad-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af9ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9ad-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9ad-117">-InputObject</span></span>
<span data-ttu-id="af9ad-118">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="af9ad-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af9ad-119">Durumlu</span><span class="sxs-lookup"><span data-stu-id="af9ad-119">-State</span></span>
<span data-ttu-id="af9ad-120">Güncelleştirilmiş uyarı durumu</span><span class="sxs-lookup"><span data-stu-id="af9ad-120">Updated Alert State</span></span>

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

### <span data-ttu-id="af9ad-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="af9ad-121">-Confirm</span></span>
<span data-ttu-id="af9ad-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af9ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9ad-123">-WhatIf</span></span>
<span data-ttu-id="af9ad-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af9ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9ad-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af9ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9ad-126">CommonParameters</span></span>
<span data-ttu-id="af9ad-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af9ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9ad-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="af9ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9ad-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af9ad-129">INPUTS</span></span>

### <span data-ttu-id="af9ad-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af9ad-130">None</span></span>

## <span data-ttu-id="af9ad-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af9ad-131">OUTPUTS</span></span>

### <span data-ttu-id="af9ad-132">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. PSAlert</span><span class="sxs-lookup"><span data-stu-id="af9ad-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="af9ad-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af9ad-133">NOTES</span></span>

## <span data-ttu-id="af9ad-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af9ad-134">RELATED LINKS</span></span>
