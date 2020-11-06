---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: b0d3baaa1e41e6f0df74e1b6bf39bdc858777a92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572689"
---
# <span data-ttu-id="873d8-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="873d8-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="873d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="873d8-102">SYNOPSIS</span></span>
<span data-ttu-id="873d8-103">Bir depolama anlayış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="873d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="873d8-104">SYNTAX</span></span>

### <span data-ttu-id="873d8-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="873d8-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="873d8-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="873d8-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="873d8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="873d8-107">DESCRIPTION</span></span>
<span data-ttu-id="873d8-108">**Get-Azurermoperationalınsightsstorageınsight** cmdlet 'i var olan bir depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="873d8-109">Bir depolama Insight adı belirtilmişse, bu cmdlet bu depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="873d8-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm depolama bilgileri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="873d8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="873d8-111">EXAMPLES</span></span>

### <span data-ttu-id="873d8-112">Örnek 1: ada göre bir depolama anlayış alın</span><span class="sxs-lookup"><span data-stu-id="873d8-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="873d8-113">Bu komut, ContosoWorkspace adlı çalışma alanından Mystorageınsight adlı depolama kavramı 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="873d8-114">Örnek 2: çalışma alanı nesnesi kullanarak bir depolama anlayış alma</span><span class="sxs-lookup"><span data-stu-id="873d8-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="873d8-115">İlk komut **Get-Azurermoperationalınsightsworkspace** cmdlet 'ini kullanarak bir işlemsel Öngörüler çalışma alanını alır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="873d8-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="873d8-116">İkinci komut, $Workspace çalışma alanı için Mystorageınsight adlı depolama kavraisini alır.</span><span class="sxs-lookup"><span data-stu-id="873d8-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="873d8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="873d8-117">PARAMETERS</span></span>

### <span data-ttu-id="873d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="873d8-118">-DefaultProfile</span></span>
<span data-ttu-id="873d8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="873d8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="873d8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="873d8-120">-Name</span></span>
<span data-ttu-id="873d8-121">Depolama Insight adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="873d8-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="873d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="873d8-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="873d8-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873d8-124">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="873d8-124">-Workspace</span></span>
<span data-ttu-id="873d8-125">Depolama öngörülerini içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="873d8-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="873d8-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="873d8-126">-WorkspaceName</span></span>
<span data-ttu-id="873d8-127">Depolama öngörülerini içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="873d8-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="873d8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="873d8-128">CommonParameters</span></span>
<span data-ttu-id="873d8-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="873d8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="873d8-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="873d8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="873d8-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="873d8-131">INPUTS</span></span>

### <span data-ttu-id="873d8-132">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="873d8-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="873d8-133">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="873d8-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="873d8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="873d8-134">System.String</span></span>

## <span data-ttu-id="873d8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="873d8-135">OUTPUTS</span></span>

### <span data-ttu-id="873d8-136">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="873d8-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="873d8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="873d8-137">NOTES</span></span>

## <span data-ttu-id="873d8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="873d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="873d8-139">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="873d8-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


