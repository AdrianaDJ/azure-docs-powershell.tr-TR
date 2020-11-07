---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 607da2e6478d72915497f1476e04ae11f9a69b9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759838"
---
# <span data-ttu-id="8abda-101">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="8abda-101">Set-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="8abda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8abda-102">SYNOPSIS</span></span>
<span data-ttu-id="8abda-103">Veri kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8abda-103">Updates a data source.</span></span>

## <span data-ttu-id="8abda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8abda-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsDataSource [-DataSource] <PSDataSource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8abda-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8abda-105">DESCRIPTION</span></span>
<span data-ttu-id="8abda-106">**Set-Azoperationalınsightsdatasource** cmdlet 'i bir veri kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="8abda-106">The **Set-AzOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="8abda-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8abda-107">EXAMPLES</span></span>

## <span data-ttu-id="8abda-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8abda-108">PARAMETERS</span></span>

### <span data-ttu-id="8abda-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="8abda-109">-DataSource</span></span>
<span data-ttu-id="8abda-110">Bu cmdlet 'in güncelleştirdiği veri kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8abda-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8abda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abda-111">-DefaultProfile</span></span>
<span data-ttu-id="8abda-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8abda-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8abda-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abda-113">CommonParameters</span></span>
<span data-ttu-id="8abda-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8abda-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abda-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8abda-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abda-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8abda-116">INPUTS</span></span>

### <span data-ttu-id="8abda-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="8abda-117">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8abda-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8abda-118">OUTPUTS</span></span>

### <span data-ttu-id="8abda-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="8abda-119">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8abda-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8abda-120">NOTES</span></span>
* <span data-ttu-id="8abda-121">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="8abda-121">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="8abda-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8abda-122">RELATED LINKS</span></span>

[<span data-ttu-id="8abda-123">Get-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="8abda-123">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="8abda-124">Remove-Azoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="8abda-124">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)


