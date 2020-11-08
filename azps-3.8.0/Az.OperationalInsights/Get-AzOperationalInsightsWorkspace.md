---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: c217a34bb89dcaa67dfc0794871e5d105ded6df1
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107201"
---
# <span data-ttu-id="4f965-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f965-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="4f965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f965-102">SYNOPSIS</span></span>
<span data-ttu-id="4f965-103">Çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="4f965-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f965-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f965-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f965-105">DESCRIPTION</span></span>
<span data-ttu-id="4f965-106">**Get-Azoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="4f965-107">Bir çalışma alanı adı belirtirseniz, bu cmdlet bu çalışma alanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="4f965-108">Bir ad belirtmezseniz, bu cmdlet kaynak grubundaki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="4f965-109">Bir ad ve kaynak grubu belirtmezseniz, bu cmdlet abonelikteki tüm çalışma alanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="4f965-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f965-110">EXAMPLES</span></span>

### <span data-ttu-id="4f965-111">Örnek 1: ada göre çalışma alanı alma</span><span class="sxs-lookup"><span data-stu-id="4f965-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4f965-112">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı bir çalışma alanını alır.</span><span class="sxs-lookup"><span data-stu-id="4f965-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="4f965-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f965-113">PARAMETERS</span></span>

### <span data-ttu-id="4f965-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f965-114">-DefaultProfile</span></span>
<span data-ttu-id="4f965-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f965-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f965-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f965-116">-Name</span></span>
<span data-ttu-id="4f965-117">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f965-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f965-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f965-118">-ResourceGroupName</span></span>
<span data-ttu-id="4f965-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f965-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f965-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f965-120">CommonParameters</span></span>
<span data-ttu-id="4f965-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f965-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f965-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f965-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f965-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f965-123">INPUTS</span></span>

### <span data-ttu-id="4f965-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4f965-124">System.String</span></span>

## <span data-ttu-id="4f965-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f965-125">OUTPUTS</span></span>

### <span data-ttu-id="4f965-126">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f965-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="4f965-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f965-127">NOTES</span></span>

## <span data-ttu-id="4f965-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f965-128">RELATED LINKS</span></span>

[<span data-ttu-id="4f965-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="4f965-129">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


