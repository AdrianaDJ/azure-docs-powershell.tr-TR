---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265861"
---
# <span data-ttu-id="44218-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span><span class="sxs-lookup"><span data-stu-id="44218-101">Get-AzOperationalInsightsWorkspaceManagementGroup</span></span>

## <span data-ttu-id="44218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44218-102">SYNOPSIS</span></span>
<span data-ttu-id="44218-103">Çalışma alanına bağlı yönetim gruplarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="44218-103">Gets details of management groups connected to a workspace.</span></span>

## <span data-ttu-id="44218-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44218-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44218-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44218-105">DESCRIPTION</span></span>
<span data-ttu-id="44218-106">**Get-Azişlemkimliği (Get-Azoperationalınsightsın**</span><span class="sxs-lookup"><span data-stu-id="44218-106">The **Get-AzOperationalInsightsWorkspaceManagementGroup** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="44218-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44218-107">EXAMPLES</span></span>

### <span data-ttu-id="44218-108">Örnek 1: Yönetim gruplarını çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="44218-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="44218-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanının Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="44218-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="44218-110">Örnek 2: ardışık düzeni kullanarak Yönetim gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="44218-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

<span data-ttu-id="44218-111">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve çalışma alanını o çalışma alanının Yönetim gruplarını alan geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="44218-111">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="44218-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44218-112">PARAMETERS</span></span>

### <span data-ttu-id="44218-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44218-113">-DefaultProfile</span></span>
<span data-ttu-id="44218-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="44218-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44218-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="44218-115">-Name</span></span>
<span data-ttu-id="44218-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44218-116">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44218-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44218-117">-ResourceGroupName</span></span>
<span data-ttu-id="44218-118">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="44218-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="44218-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44218-119">CommonParameters</span></span>
<span data-ttu-id="44218-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44218-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44218-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44218-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44218-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44218-122">INPUTS</span></span>

### <span data-ttu-id="44218-123">System. String</span><span class="sxs-lookup"><span data-stu-id="44218-123">System.String</span></span>

## <span data-ttu-id="44218-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44218-124">OUTPUTS</span></span>

### <span data-ttu-id="44218-125">Microsoft. Azure. Commands. Operationalınsights. model. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="44218-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="44218-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44218-126">NOTES</span></span>

## <span data-ttu-id="44218-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44218-127">RELATED LINKS</span></span>

[<span data-ttu-id="44218-128">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="44218-128">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="44218-129">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="44218-129">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


