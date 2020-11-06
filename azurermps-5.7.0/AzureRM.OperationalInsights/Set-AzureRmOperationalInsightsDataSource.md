---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 3992E6B5-F794-4C7A-BB59-C8D60E2CD7BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: e45dcbfad9b4b92695f310d7d2c56fc46fc57bd7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586677"
---
# <span data-ttu-id="81217-101">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="81217-101">Set-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="81217-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81217-102">SYNOPSIS</span></span>
<span data-ttu-id="81217-103">Veri kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="81217-103">Updates a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81217-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81217-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsDataSource [-DataSource] <PSDataSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81217-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="81217-105">DESCRIPTION</span></span>
<span data-ttu-id="81217-106">**Set-Azurermoperationalınsightsdatasource** cmdlet 'i bir veri kaynağını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="81217-106">The **Set-AzureRmOperationalInsightsDataSource** cmdlet updates a data source.</span></span>

## <span data-ttu-id="81217-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81217-107">EXAMPLES</span></span>

## <span data-ttu-id="81217-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81217-108">PARAMETERS</span></span>

### <span data-ttu-id="81217-109">-DataSource</span><span class="sxs-lookup"><span data-stu-id="81217-109">-DataSource</span></span>
<span data-ttu-id="81217-110">Bu cmdlet 'in güncelleştirdiği veri kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81217-110">Specifies the data source that this cmdlet updates.</span></span>

```yaml
Type: PSDataSource
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81217-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81217-111">-DefaultProfile</span></span>
<span data-ttu-id="81217-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="81217-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81217-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81217-113">CommonParameters</span></span>
<span data-ttu-id="81217-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81217-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81217-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81217-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81217-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81217-116">INPUTS</span></span>

### <span data-ttu-id="81217-117">PSDataSource</span><span class="sxs-lookup"><span data-stu-id="81217-117">PSDataSource</span></span>
<span data-ttu-id="81217-118">' DataSource ' parametresi ardışık düzenin ' PSDataSource ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="81217-118">Parameter 'DataSource' accepts value of type 'PSDataSource' from the pipeline</span></span>

## <span data-ttu-id="81217-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81217-119">OUTPUTS</span></span>

### <span data-ttu-id="81217-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="81217-120">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="81217-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81217-121">NOTES</span></span>
* <span data-ttu-id="81217-122">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, işletim, Öngörüler</span><span class="sxs-lookup"><span data-stu-id="81217-122">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="81217-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81217-123">RELATED LINKS</span></span>

[<span data-ttu-id="81217-124">Get-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="81217-124">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="81217-125">Remove-Azurermoperationalınsightsdatasource</span><span class="sxs-lookup"><span data-stu-id="81217-125">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)


