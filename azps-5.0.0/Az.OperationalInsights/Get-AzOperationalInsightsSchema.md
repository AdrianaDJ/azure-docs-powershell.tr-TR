---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325105"
---
# <span data-ttu-id="a6d46-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="a6d46-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="a6d46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6d46-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d46-103">Çalışma alanıyla ilişkili şemayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="a6d46-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="a6d46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6d46-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6d46-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d46-106">**Get-Azoperationalınsiizsschema** cmdlet 'i, bu kaynak grubu içinde belirtilen çalışma alanıyla ilişkilendirilmiş şemayı döndürür.</span><span class="sxs-lookup"><span data-stu-id="a6d46-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="a6d46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6d46-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d46-108">Örnek 1: çalışma alanının şemalarını alma</span><span class="sxs-lookup"><span data-stu-id="a6d46-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="a6d46-109">Bu komut, çalışma alanıyla ilişkilendirilmiş şemaları alır.</span><span class="sxs-lookup"><span data-stu-id="a6d46-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="a6d46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6d46-110">PARAMETERS</span></span>

### <span data-ttu-id="a6d46-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d46-111">-DefaultProfile</span></span>
<span data-ttu-id="a6d46-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a6d46-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6d46-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6d46-113">-ResourceGroupName</span></span>
<span data-ttu-id="a6d46-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d46-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="a6d46-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="a6d46-115">-WorkspaceName</span></span>
<span data-ttu-id="a6d46-116">Bir çalışma alanı adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6d46-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6d46-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d46-117">CommonParameters</span></span>
<span data-ttu-id="a6d46-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6d46-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d46-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6d46-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d46-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6d46-120">INPUTS</span></span>

### <span data-ttu-id="a6d46-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a6d46-121">System.String</span></span>

## <span data-ttu-id="a6d46-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6d46-122">OUTPUTS</span></span>

### <span data-ttu-id="a6d46-123">Microsoft. Azure. Commands. Operationalınsights. modeller. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="a6d46-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="a6d46-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6d46-124">NOTES</span></span>

## <span data-ttu-id="a6d46-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6d46-125">RELATED LINKS</span></span>

[<span data-ttu-id="a6d46-126">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a6d46-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


