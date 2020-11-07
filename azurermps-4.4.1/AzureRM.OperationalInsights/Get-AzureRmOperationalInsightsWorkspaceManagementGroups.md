---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 55fe1a82d0e54606c04954167aef2c2b90086655
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763665"
---
# <span data-ttu-id="0fbd5-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="0fbd5-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="0fbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbd5-103">Çalışma alanına bağlı yönetim gruplarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbd5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fbd5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fbd5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbd5-106">**Get-Azurermoperationalınsightsever** yönetimi, bir çalışma alanına bağlı Yönetim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="0fbd5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbd5-108">Örnek 1: Yönetim gruplarını çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="0fbd5-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0fbd5-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanının Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0fbd5-110">Örnek 2: ardışık düzeni kullanarak Yönetim gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="0fbd5-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="0fbd5-111">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve çalışma alanını o çalışma alanının Yönetim gruplarını alan geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="0fbd5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fbd5-112">PARAMETERS</span></span>

### <span data-ttu-id="0fbd5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fbd5-113">-Name</span></span>
<span data-ttu-id="0fbd5-114">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0fbd5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbd5-115">-ResourceGroupName</span></span>
<span data-ttu-id="0fbd5-116">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-116">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0fbd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbd5-117">-DefaultProfile</span></span>
<span data-ttu-id="0fbd5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fbd5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbd5-119">CommonParameters</span></span>
<span data-ttu-id="0fbd5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fbd5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbd5-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbd5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbd5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fbd5-122">INPUTS</span></span>

## <span data-ttu-id="0fbd5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fbd5-123">OUTPUTS</span></span>

### <span data-ttu-id="0fbd5-124">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="0fbd5-124">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="0fbd5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fbd5-125">NOTES</span></span>

## <span data-ttu-id="0fbd5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fbd5-126">RELATED LINKS</span></span>

[<span data-ttu-id="0fbd5-127">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="0fbd5-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0fbd5-128">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="0fbd5-128">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


