---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 808c92e987d30e97ee0ad2ed56b24be9b0f92a1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762254"
---
# <span data-ttu-id="c54e1-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="c54e1-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="c54e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c54e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c54e1-103">Çalışma alanına bağlı yönetim gruplarının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c54e1-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c54e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c54e1-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c54e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c54e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c54e1-106">**Get-Azurermoperationalınsightsever** yönetimi, bir çalışma alanına bağlı Yönetim gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c54e1-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="c54e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c54e1-107">EXAMPLES</span></span>

### <span data-ttu-id="c54e1-108">Örnek 1: Yönetim gruplarını çalışma alanı adına göre alma</span><span class="sxs-lookup"><span data-stu-id="c54e1-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="c54e1-109">Bu komut, ContosoResourceGroup adlı kaynak grubunda MyWorkspace adlı çalışma alanının Yönetim gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="c54e1-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c54e1-110">Örnek 2: ardışık düzeni kullanarak Yönetim gruplarını alma</span><span class="sxs-lookup"><span data-stu-id="c54e1-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="c54e1-111">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve çalışma alanını o çalışma alanının Yönetim gruplarını alan geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c54e1-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="c54e1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c54e1-112">PARAMETERS</span></span>

### <span data-ttu-id="c54e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54e1-113">-DefaultProfile</span></span>
<span data-ttu-id="c54e1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c54e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c54e1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c54e1-115">-Name</span></span>
<span data-ttu-id="c54e1-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c54e1-116">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c54e1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c54e1-117">-ResourceGroupName</span></span>
<span data-ttu-id="c54e1-118">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c54e1-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c54e1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54e1-119">CommonParameters</span></span>
<span data-ttu-id="c54e1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c54e1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54e1-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54e1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54e1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c54e1-122">INPUTS</span></span>

### <span data-ttu-id="c54e1-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c54e1-123">None</span></span>
<span data-ttu-id="c54e1-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c54e1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c54e1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c54e1-125">OUTPUTS</span></span>

### <span data-ttu-id="c54e1-126">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. PSManagementGroup]</span><span class="sxs-lookup"><span data-stu-id="c54e1-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup]</span></span>

## <span data-ttu-id="c54e1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c54e1-127">NOTES</span></span>

## <span data-ttu-id="c54e1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c54e1-128">RELATED LINKS</span></span>

[<span data-ttu-id="c54e1-129">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c54e1-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="c54e1-130">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="c54e1-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


