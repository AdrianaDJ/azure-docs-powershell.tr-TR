---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096682"
---
# <span data-ttu-id="23782-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="23782-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="23782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23782-102">SYNOPSIS</span></span>
<span data-ttu-id="23782-103">Uyarı geçmişi bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="23782-103">Gets Alert History information</span></span>

## <span data-ttu-id="23782-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23782-104">SYNTAX</span></span>

### <span data-ttu-id="23782-105">ByAlertId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23782-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23782-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="23782-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23782-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="23782-107">DESCRIPTION</span></span>
<span data-ttu-id="23782-108">**Get-AzAlertObjectHistory** cmdlet 'inin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="23782-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="23782-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23782-109">EXAMPLES</span></span>

### <span data-ttu-id="23782-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23782-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="23782-111">Uyarı geçmişi ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="23782-111">Gets alert history details.</span></span> 

## <span data-ttu-id="23782-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23782-112">PARAMETERS</span></span>

### <span data-ttu-id="23782-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="23782-113">-AlertId</span></span>
<span data-ttu-id="23782-114">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="23782-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="23782-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23782-115">-DefaultProfile</span></span>
<span data-ttu-id="23782-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23782-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23782-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23782-117">-InputObject</span></span>
<span data-ttu-id="23782-118">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="23782-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="23782-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23782-119">CommonParameters</span></span>
<span data-ttu-id="23782-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23782-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23782-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23782-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23782-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23782-122">INPUTS</span></span>

### <span data-ttu-id="23782-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="23782-123">None</span></span>

## <span data-ttu-id="23782-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23782-124">OUTPUTS</span></span>

### <span data-ttu-id="23782-125">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. Psalcertdeğişimi</span><span class="sxs-lookup"><span data-stu-id="23782-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="23782-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23782-126">NOTES</span></span>

## <span data-ttu-id="23782-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23782-127">RELATED LINKS</span></span>
