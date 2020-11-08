---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276485"
---
# <span data-ttu-id="1f3ab-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="1f3ab-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="1f3ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3ab-103">Uyarı geçmişi bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="1f3ab-103">Gets Alert History information</span></span>

## <span data-ttu-id="1f3ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f3ab-104">SYNTAX</span></span>

### <span data-ttu-id="1f3ab-105">ByAlertId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f3ab-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f3ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f3ab-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f3ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f3ab-107">DESCRIPTION</span></span>
<span data-ttu-id="1f3ab-108">**Get-AzAlertObjectHistory** cmdlet 'inin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="1f3ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f3ab-109">EXAMPLES</span></span>

### <span data-ttu-id="1f3ab-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f3ab-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="1f3ab-111">Uyarı geçmişi ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-111">Gets alert history details.</span></span> 

## <span data-ttu-id="1f3ab-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f3ab-112">PARAMETERS</span></span>

### <span data-ttu-id="1f3ab-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="1f3ab-113">-AlertId</span></span>
<span data-ttu-id="1f3ab-114">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="1f3ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3ab-115">-DefaultProfile</span></span>
<span data-ttu-id="1f3ab-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f3ab-117">-InputObject</span></span>
<span data-ttu-id="1f3ab-118">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="1f3ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3ab-119">CommonParameters</span></span>
<span data-ttu-id="1f3ab-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3ab-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1f3ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3ab-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f3ab-122">INPUTS</span></span>

### <span data-ttu-id="1f3ab-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1f3ab-123">None</span></span>

## <span data-ttu-id="1f3ab-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f3ab-124">OUTPUTS</span></span>

### <span data-ttu-id="1f3ab-125">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. Psalcertdeğişimi</span><span class="sxs-lookup"><span data-stu-id="1f3ab-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="1f3ab-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f3ab-126">NOTES</span></span>

## <span data-ttu-id="1f3ab-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f3ab-127">RELATED LINKS</span></span>
