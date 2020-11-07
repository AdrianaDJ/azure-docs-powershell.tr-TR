---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 8c0df920b8619760cf4a80d9ef6502e82de9a31f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753666"
---
# <span data-ttu-id="b7f1e-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="b7f1e-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="b7f1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f1e-103">Uyarı geçmişi bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="b7f1e-103">Gets Alert History information</span></span>

## <span data-ttu-id="b7f1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7f1e-104">SYNTAX</span></span>

### <span data-ttu-id="b7f1e-105">ByAlertId (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7f1e-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7f1e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b7f1e-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7f1e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7f1e-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f1e-108">**Get-AzAlertObjectHistory** cmdlet 'inin geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="b7f1e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7f1e-109">EXAMPLES</span></span>

### <span data-ttu-id="b7f1e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7f1e-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="b7f1e-111">Uyarı geçmişi ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-111">Gets alert history details.</span></span> 

## <span data-ttu-id="b7f1e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7f1e-112">PARAMETERS</span></span>

### <span data-ttu-id="b7f1e-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="b7f1e-113">-AlertId</span></span>
<span data-ttu-id="b7f1e-114">Uyarının/RESOURCEID için benzersiz tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="b7f1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f1e-115">-DefaultProfile</span></span>
<span data-ttu-id="b7f1e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f1e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7f1e-117">-InputObject</span></span>
<span data-ttu-id="b7f1e-118">Ardışık düzenin giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="b7f1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f1e-119">CommonParameters</span></span>
<span data-ttu-id="b7f1e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f1e-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7f1e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f1e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7f1e-122">INPUTS</span></span>

### <span data-ttu-id="b7f1e-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b7f1e-123">None</span></span>

## <span data-ttu-id="b7f1e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7f1e-124">OUTPUTS</span></span>

### <span data-ttu-id="b7f1e-125">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. Psalcertdeğişimi</span><span class="sxs-lookup"><span data-stu-id="b7f1e-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="b7f1e-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7f1e-126">NOTES</span></span>

## <span data-ttu-id="b7f1e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7f1e-127">RELATED LINKS</span></span>
