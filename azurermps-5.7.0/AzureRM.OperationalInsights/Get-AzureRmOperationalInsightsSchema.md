---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 1e1e56a4cf0e31af3d64377df05b6057354dd534
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762362"
---
# <span data-ttu-id="02602-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="02602-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="02602-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02602-102">SYNOPSIS</span></span>
<span data-ttu-id="02602-103">Çalışma alanıyla ilişkili şemayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="02602-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02602-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02602-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02602-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="02602-105">DESCRIPTION</span></span>
<span data-ttu-id="02602-106">**Get-Azurermoperationalınsiizskema** cmdlet 'i, bu kaynak grubu içinde belirtilen çalışma alanıyla ilişkilendirilmiş şemayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="02602-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="02602-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02602-107">EXAMPLES</span></span>

### <span data-ttu-id="02602-108">Örnek 1: çalışma alanının şemalarını alma</span><span class="sxs-lookup"><span data-stu-id="02602-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="02602-109">Bu komut, çalışma alanıyla ilişkilendirilmiş şemaları alır.</span><span class="sxs-lookup"><span data-stu-id="02602-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="02602-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02602-110">PARAMETERS</span></span>

### <span data-ttu-id="02602-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02602-111">-DefaultProfile</span></span>
<span data-ttu-id="02602-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="02602-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02602-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02602-113">-ResourceGroupName</span></span>
<span data-ttu-id="02602-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="02602-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02602-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="02602-115">-WorkspaceName</span></span>
<span data-ttu-id="02602-116">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="02602-116">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02602-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02602-117">CommonParameters</span></span>
<span data-ttu-id="02602-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02602-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02602-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02602-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02602-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02602-120">INPUTS</span></span>

### <span data-ttu-id="02602-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="02602-121">None</span></span>
<span data-ttu-id="02602-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="02602-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02602-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02602-123">OUTPUTS</span></span>

### <span data-ttu-id="02602-124">Microsoft. Azure. Commands. Operationalınsights. modeller. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="02602-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="02602-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02602-125">NOTES</span></span>

## <span data-ttu-id="02602-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02602-126">RELATED LINKS</span></span>

[<span data-ttu-id="02602-127">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="02602-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


