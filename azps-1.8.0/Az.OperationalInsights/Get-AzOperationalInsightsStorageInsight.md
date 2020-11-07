---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 589b6012a1819eac638f6197d0569972e4727fba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761935"
---
# <span data-ttu-id="39ea6-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="39ea6-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="39ea6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="39ea6-103">Bir depolama anlayış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="39ea6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39ea6-104">SYNTAX</span></span>

### <span data-ttu-id="39ea6-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39ea6-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39ea6-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="39ea6-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39ea6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39ea6-107">DESCRIPTION</span></span>
<span data-ttu-id="39ea6-108">**Get-Azişlemkimliği** , var olan bir depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="39ea6-109">Bir depolama Insight adı belirtilmişse, bu cmdlet bu depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="39ea6-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm depolama bilgileri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="39ea6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39ea6-111">EXAMPLES</span></span>

### <span data-ttu-id="39ea6-112">Örnek 1: ada göre bir depolama anlayış alın</span><span class="sxs-lookup"><span data-stu-id="39ea6-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="39ea6-113">Bu komut, ContosoWorkspace adlı çalışma alanından Mystorageınsight adlı depolama kavramı 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="39ea6-114">Örnek 2: çalışma alanı nesnesi kullanarak bir depolama anlayış alma</span><span class="sxs-lookup"><span data-stu-id="39ea6-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="39ea6-115">İlk komut, bir Işlemsel Öngörüler çalışma alanını almak için **Get-Azoperationalınsightsworkspace** cmdlet 'ini kullanır ve sonra bunu $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="39ea6-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="39ea6-116">İkinci komut, $Workspace çalışma alanı için Mystorageınsight adlı depolama kavraisini alır.</span><span class="sxs-lookup"><span data-stu-id="39ea6-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="39ea6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39ea6-117">PARAMETERS</span></span>

### <span data-ttu-id="39ea6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ea6-118">-DefaultProfile</span></span>
<span data-ttu-id="39ea6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="39ea6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39ea6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="39ea6-120">-Name</span></span>
<span data-ttu-id="39ea6-121">Depolama Insight adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39ea6-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="39ea6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ea6-122">-ResourceGroupName</span></span>
<span data-ttu-id="39ea6-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39ea6-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="39ea6-124">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="39ea6-124">-Workspace</span></span>
<span data-ttu-id="39ea6-125">Depolama öngörülerini içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39ea6-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="39ea6-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="39ea6-126">-WorkspaceName</span></span>
<span data-ttu-id="39ea6-127">Depolama öngörülerini içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39ea6-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="39ea6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ea6-128">CommonParameters</span></span>
<span data-ttu-id="39ea6-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39ea6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ea6-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ea6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ea6-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39ea6-131">INPUTS</span></span>

### <span data-ttu-id="39ea6-132">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="39ea6-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="39ea6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="39ea6-133">System.String</span></span>

## <span data-ttu-id="39ea6-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39ea6-134">OUTPUTS</span></span>

### <span data-ttu-id="39ea6-135">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="39ea6-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="39ea6-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39ea6-136">NOTES</span></span>

## <span data-ttu-id="39ea6-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39ea6-137">RELATED LINKS</span></span>

[<span data-ttu-id="39ea6-138">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="39ea6-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


