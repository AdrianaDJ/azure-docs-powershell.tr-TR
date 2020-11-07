---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: e51325a18f8a880131e9037473a60e8a56ea488f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765217"
---
# <span data-ttu-id="7c43a-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7c43a-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="7c43a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c43a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c43a-103">Bir depolama anlayış hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c43a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c43a-104">SYNTAX</span></span>

### <span data-ttu-id="7c43a-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c43a-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c43a-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c43a-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c43a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c43a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c43a-108">**Get-Azurermoperationalınsightsstorageınsight** cmdlet 'i var olan bir depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="7c43a-109">Bir depolama Insight adı belirtilmişse, bu cmdlet bu depolama Insight hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="7c43a-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm depolama bilgileri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="7c43a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c43a-111">EXAMPLES</span></span>

### <span data-ttu-id="7c43a-112">Örnek 1: ada göre bir depolama anlayış alın</span><span class="sxs-lookup"><span data-stu-id="7c43a-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7c43a-113">Bu komut, ContosoWorkspace adlı çalışma alanından Mystorageınsight adlı depolama kavramı 'ni alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7c43a-114">Örnek 2: çalışma alanı nesnesi kullanarak bir depolama anlayış alma</span><span class="sxs-lookup"><span data-stu-id="7c43a-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="7c43a-115">İlk komut **Get-Azurermoperationalınsightsworkspace** cmdlet 'ini kullanarak bir işlemsel Öngörüler çalışma alanını alır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7c43a-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="7c43a-116">İkinci komut, $Workspace çalışma alanı için Mystorageınsight adlı depolama kavraisini alır.</span><span class="sxs-lookup"><span data-stu-id="7c43a-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="7c43a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c43a-117">PARAMETERS</span></span>

### <span data-ttu-id="7c43a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c43a-118">-DefaultProfile</span></span>
<span data-ttu-id="7c43a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7c43a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c43a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c43a-120">-Name</span></span>
<span data-ttu-id="7c43a-121">Depolama Insight adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c43a-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c43a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c43a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7c43a-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c43a-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c43a-124">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="7c43a-124">-Workspace</span></span>
<span data-ttu-id="7c43a-125">Depolama öngörülerini içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c43a-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c43a-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="7c43a-126">-WorkspaceName</span></span>
<span data-ttu-id="7c43a-127">Depolama öngörülerini içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c43a-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c43a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c43a-128">CommonParameters</span></span>
<span data-ttu-id="7c43a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c43a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c43a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c43a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c43a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c43a-131">INPUTS</span></span>

### <span data-ttu-id="7c43a-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c43a-132">PSWorkspace</span></span>
<span data-ttu-id="7c43a-133">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7c43a-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="7c43a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c43a-134">OUTPUTS</span></span>

### <span data-ttu-id="7c43a-135">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Operationalınsights. model. Psstorageınsight]</span><span class="sxs-lookup"><span data-stu-id="7c43a-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="7c43a-136">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="7c43a-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="7c43a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c43a-137">NOTES</span></span>

## <span data-ttu-id="7c43a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c43a-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c43a-139">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="7c43a-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


