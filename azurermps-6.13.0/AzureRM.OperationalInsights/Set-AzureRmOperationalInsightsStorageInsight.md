---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762462"
---
# <span data-ttu-id="6208b-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6208b-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="6208b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6208b-102">SYNOPSIS</span></span>
<span data-ttu-id="6208b-103">Bir depolama Insight güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6208b-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6208b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6208b-104">SYNTAX</span></span>

### <span data-ttu-id="6208b-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6208b-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6208b-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="6208b-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6208b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6208b-107">DESCRIPTION</span></span>
<span data-ttu-id="6208b-108">**Set-Azurermoperationalınsightsstorageınsight** cmdlet 'ı bir depolama Insight yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6208b-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="6208b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6208b-109">EXAMPLES</span></span>

### <span data-ttu-id="6208b-110">Örnek 1: adla bir depolama kavramı değiştirme</span><span class="sxs-lookup"><span data-stu-id="6208b-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="6208b-111">Bu komut Mystorageınsight adındaki depolama kavramasındaki tabloları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6208b-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="6208b-112">Örnek 2: çalışma alanı nesnesi kullanarak bir depolama anlayış değiştirme</span><span class="sxs-lookup"><span data-stu-id="6208b-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="6208b-113">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6208b-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="6208b-114">İkinci komut Mystorageınsight adındaki depolama kavramasındaki kapsayıcıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6208b-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="6208b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6208b-115">PARAMETERS</span></span>

### <span data-ttu-id="6208b-116">-Kapsayıcılar</span><span class="sxs-lookup"><span data-stu-id="6208b-116">-Containers</span></span>
<span data-ttu-id="6208b-117">Verileri sağlayan kapsayıcıların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6208b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6208b-118">-DefaultProfile</span></span>
<span data-ttu-id="6208b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6208b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6208b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6208b-120">-Name</span></span>
<span data-ttu-id="6208b-121">Bir depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6208b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6208b-122">-ResourceGroupName</span></span>
<span data-ttu-id="6208b-123">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="6208b-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6208b-124">-StorageAccountKey</span></span>
<span data-ttu-id="6208b-125">Depolama hesabı için erişim anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6208b-126">-Tablolar</span><span class="sxs-lookup"><span data-stu-id="6208b-126">-Tables</span></span>
<span data-ttu-id="6208b-127">Verileri içeren tabloların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6208b-128">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="6208b-128">-Workspace</span></span>
<span data-ttu-id="6208b-129">Depolama kavramı içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="6208b-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6208b-130">-WorkspaceName</span></span>
<span data-ttu-id="6208b-131">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6208b-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="6208b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6208b-132">CommonParameters</span></span>
<span data-ttu-id="6208b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6208b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6208b-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6208b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6208b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6208b-135">INPUTS</span></span>

### <span data-ttu-id="6208b-136">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6208b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="6208b-137">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6208b-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="6208b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6208b-138">System.String</span></span>

### <span data-ttu-id="6208b-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="6208b-139">System.String[]</span></span>

## <span data-ttu-id="6208b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6208b-140">OUTPUTS</span></span>

### <span data-ttu-id="6208b-141">Microsoft. Azure. Commands. Operationalınsights. modeller. Psstorageınsight</span><span class="sxs-lookup"><span data-stu-id="6208b-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="6208b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6208b-142">NOTES</span></span>

## <span data-ttu-id="6208b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6208b-143">RELATED LINKS</span></span>

[<span data-ttu-id="6208b-144">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6208b-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="6208b-145">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="6208b-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


