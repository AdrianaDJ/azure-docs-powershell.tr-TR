---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azsmartgrouphistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzSmartGroupHistory.md
ms.openlocfilehash: a8e827d678c7ac3b917ee7be09d030b193ffda24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276288"
---
# <span data-ttu-id="7de23-101">Get-AzSmartGroupHistory</span><span class="sxs-lookup"><span data-stu-id="7de23-101">Get-AzSmartGroupHistory</span></span>

## <span data-ttu-id="7de23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7de23-102">SYNOPSIS</span></span>
<span data-ttu-id="7de23-103">Akıllı grup geçmişini alır</span><span class="sxs-lookup"><span data-stu-id="7de23-103">Gets smart group history</span></span>

## <span data-ttu-id="7de23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7de23-104">SYNTAX</span></span>

### <span data-ttu-id="7de23-105">Bysmartgroupıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7de23-105">BySmartGroupId (Default)</span></span>
```
Get-AzSmartGroupHistory -SmartGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7de23-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7de23-106">ByInputObject</span></span>
```
Get-AzSmartGroupHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7de23-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7de23-107">DESCRIPTION</span></span>
<span data-ttu-id="7de23-108">**Get-AzSmartGroupHistory** cmdlet 'i, akıllı grup geçmişi 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="7de23-108">**Get-AzSmartGroupHistory** cmdlet gets smart group history.</span></span>

## <span data-ttu-id="7de23-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7de23-109">EXAMPLES</span></span>

### <span data-ttu-id="7de23-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7de23-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSmartGroupHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="7de23-111">Akıllı grup geçmişi ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7de23-111">Gets smart group history details.</span></span>

## <span data-ttu-id="7de23-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7de23-112">PARAMETERS</span></span>

### <span data-ttu-id="7de23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de23-113">-DefaultProfile</span></span>
<span data-ttu-id="7de23-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7de23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de23-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7de23-115">-InputObject</span></span>
<span data-ttu-id="7de23-116">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7de23-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7de23-117">-Smartgroupıd</span><span class="sxs-lookup"><span data-stu-id="7de23-117">-SmartGroupId</span></span>
<span data-ttu-id="7de23-118">Akıllı grup/RESOURCEID 'nin benzersiz tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="7de23-118">Unique Identifier of SmartGroup / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de23-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de23-119">CommonParameters</span></span>
<span data-ttu-id="7de23-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7de23-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de23-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7de23-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de23-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7de23-122">INPUTS</span></span>

### <span data-ttu-id="7de23-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7de23-123">None</span></span>

## <span data-ttu-id="7de23-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7de23-124">OUTPUTS</span></span>

### <span data-ttu-id="7de23-125">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. Pssmartgroupdeğişimi</span><span class="sxs-lookup"><span data-stu-id="7de23-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroupModification</span></span>

## <span data-ttu-id="7de23-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7de23-126">NOTES</span></span>

## <span data-ttu-id="7de23-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7de23-127">RELATED LINKS</span></span>
