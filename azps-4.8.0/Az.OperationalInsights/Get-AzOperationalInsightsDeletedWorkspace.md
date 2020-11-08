---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdeletedworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDeletedWorkspace.md
ms.openlocfilehash: ce40458262d095f0e1fe58def1cf3d4508a6c6b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274040"
---
# <span data-ttu-id="9adbf-101">Get-AzOperationalInsightsDeletedWorkspace</span><span class="sxs-lookup"><span data-stu-id="9adbf-101">Get-AzOperationalInsightsDeletedWorkspace</span></span>

## <span data-ttu-id="9adbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9adbf-102">SYNOPSIS</span></span>
<span data-ttu-id="9adbf-103">Silinmiş çalışma alanlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="9adbf-103">List deleted workspaces.</span></span>

## <span data-ttu-id="9adbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9adbf-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsDeletedWorkspace [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9adbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9adbf-105">DESCRIPTION</span></span>
<span data-ttu-id="9adbf-106">Silinmiş çalışma alanlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="9adbf-106">List deleted workspaces.</span></span>

## <span data-ttu-id="9adbf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9adbf-107">EXAMPLES</span></span>

### <span data-ttu-id="9adbf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9adbf-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> Get-AzOperationalInsightsDeletedWorkspace -ResourceGroupName $rgname
```

<span data-ttu-id="9adbf-109">Silinmiş çalışma alanlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="9adbf-109">List deleted workspaces.</span></span>

## <span data-ttu-id="9adbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9adbf-110">PARAMETERS</span></span>

### <span data-ttu-id="9adbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adbf-111">-DefaultProfile</span></span>
<span data-ttu-id="9adbf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9adbf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9adbf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9adbf-113">-ResourceGroupName</span></span>
<span data-ttu-id="9adbf-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9adbf-114">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adbf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adbf-115">CommonParameters</span></span>
<span data-ttu-id="9adbf-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9adbf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adbf-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9adbf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adbf-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9adbf-118">INPUTS</span></span>

### <span data-ttu-id="9adbf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="9adbf-119">System.String</span></span>

## <span data-ttu-id="9adbf-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9adbf-120">OUTPUTS</span></span>

### <span data-ttu-id="9adbf-121">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9adbf-121">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9adbf-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9adbf-122">NOTES</span></span>

## <span data-ttu-id="9adbf-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9adbf-123">RELATED LINKS</span></span>
